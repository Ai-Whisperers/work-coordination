# S002: Rate Limiting

**Epic:** [v003-security-devops](_epic.md)  
**Status:** 📋 Ready  
**Effort:** ~4 hours total

---

## User Story

**As a** system operator  
**I want** rate limiting on public API endpoints  
**So that** the API cannot be abused or DDoS'd

---

## Acceptance Criteria

- [ ] Rate limiter middleware implemented
- [ ] Configurable limits per endpoint type
- [ ] Returns 429 Too Many Requests when exceeded
- [ ] Rate limit headers in responses
- [ ] Logged for monitoring

---

## Tasks

| ID | Task | Effort | Status | Owner |
|----|------|--------|--------|-------|
| T001 | Research and select rate limiting solution | 1h | ✅ | Nyx 🌙 |
| T002 | Implement rate limiter middleware | 3h | ⬜ | — |

---

## Task Details

### T001: Research rate limiting options

**Options to evaluate:**

1. **@upstash/ratelimit** (recommended for Vercel/serverless)
   - Redis-based, distributed
   - Works with edge functions
   - Free tier available

2. **next-rate-limit**
   - In-memory, simple
   - Not distributed (single instance only)

3. **Custom with Supabase**
   - Use Supabase for storage
   - More complex but no external deps

**Decision criteria:**
- Must work with Next.js App Router
- Should be distributable (future multi-instance)
- Cost-effective

**Research Findings (Nyx 🌙):**

**1. @upstash/ratelimit:**
- ✅ **RECOMMENDED** - Excellent Next.js App Router support via middleware
- ✅ Specifically designed for serverless/edge environments (Vercel, Cloudflare, etc.)
- ✅ Redis-based = distributed across multiple instances 
- ✅ Built-in features: sliding window, fixed window, token bucket algorithms
- ✅ Proper HTTP headers (`X-RateLimit-Limit`, `X-RateLimit-Remaining`) 
- ✅ Analytics dashboard and traffic protection features
- ✅ Free tier: 10k requests/month, paid plans start ~$0.20/100k requests
- ✅ Works in Next.js middleware.ts for global rate limiting
- 📝 Requires Redis setup (Upstash provides free Redis instance)

**2. next-rate-limit:**
- ❌ **NOT RECOMMENDED** - Limited App Router compatibility  
- ❌ In-memory only = doesn't work with multiple instances/serverless
- ❌ Loses state on cold starts (problematic for Vercel/serverless)
- ❌ No built-in middleware integration for App Router
- ✅ Simple setup, no external dependencies
- ⚠️ Only suitable for single-instance deployments

**3. Custom with Supabase:**
- ✅ Leverages existing Supabase infrastructure 
- ✅ Distributed storage, works across instances
- ❌ Requires custom implementation (significant development time)
- ❌ Need to handle: sliding windows, cleanup, proper algorithms
- ❌ No built-in middleware integration
- ⚠️ Higher complexity = more bugs, maintenance overhead

**Recommendation:**
Use **@upstash/ratelimit** - it's purpose-built for Next.js App Router middleware, handles all edge cases, and provides enterprise features out of the box. The free tier covers initial usage, and pricing scales reasonably.

---

### T002: Implement rate limiter

**Suggested approach:**

```typescript
// middleware.ts
import { Ratelimit } from "@upstash/ratelimit";
import { Redis } from "@upstash/redis";

const ratelimit = new Ratelimit({
  redis: Redis.fromEnv(),
  limiter: Ratelimit.slidingWindow(10, "10 s"), // 10 requests per 10 seconds
});

export async function middleware(request: NextRequest) {
  const ip = request.ip ?? "127.0.0.1";
  const { success, limit, remaining } = await ratelimit.limit(ip);
  
  if (!success) {
    return new Response("Too Many Requests", { status: 429 });
  }
  
  // Add headers
  const response = NextResponse.next();
  response.headers.set("X-RateLimit-Limit", limit.toString());
  response.headers.set("X-RateLimit-Remaining", remaining.toString());
  return response;
}
```

**Endpoints to protect:**
- `/api/auth/*` — stricter limits (prevent brute force)
- `/api/*` — general limits

---

## Notes

- Start with T001 to pick the right solution
- If using Upstash, need to set up account and get credentials
- Consider different limits for authenticated vs anonymous
