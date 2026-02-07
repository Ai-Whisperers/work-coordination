# Story s001: Ternary Encoder

**Epic:** [r002-vaes](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 10 hours

## User Story
As a researcher, I want a ternary encoding scheme so I can represent biological sequences efficiently.

## Acceptance Criteria
- [ ] Base-3 (ternary) encoding for nucleotides
- [ ] Efficient Python implementation
- [ ] Support for DNA/RNA sequences
- [ ] Batch processing
- [ ] Reversible encoding
- [ ] Benchmark vs standard methods

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Design ternary encoding scheme | 2h | ⬜ | — |
| T002 | Implement TernaryEncoder class | 2h | ⬜ | — |
| T003 | Add batch processing | 1h | ⬜ | — |
| T004 | Create decode function | 1h | ⬜ | — |
| T005 | Write unit tests | 1h | ⬜ | — |
| T006 | Benchmark compression ratio | 1h | ⬜ | — |
| T007 | Compare with one-hot encoding | 1h | ⬜ | — |
| T008 | Document algorithm | 1h | ⬜ | — |

## Technical Notes
- Map: A→0, C→1, G→2, T→0 (or similar)
- Use numpy for vectorization
- Target: 1000x compression
