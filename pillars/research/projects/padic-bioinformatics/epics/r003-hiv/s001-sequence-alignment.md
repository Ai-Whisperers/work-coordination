# Story s001: HIV Sequence Alignment

**Epic:** [r003-hiv](_epic.md)  
**Status:** 📋 Ready  
**Effort:** 8 hours

## User Story
As a researcher, I want to align HIV sequences so I can analyze evolutionary patterns.

## Acceptance Criteria
- [ ] Download HIV sequences from databases
- [ ] Multiple sequence alignment
- [ ] Alignment visualization
- [ ] Conservation scoring
- [ ] Export for downstream analysis

## Tasks

| ID | Task | Est | Status | Assignee |
|----|------|-----|--------|----------|
| T001 | Set up sequence data pipeline | 1h | ⏳ | Erebus 🔥 |
| T002 | Download from Los Alamos DB | 1h | ⬜ | — |
| T003 | Implement MAFFT wrapper | 1h | ⬜ | — |
| T004 | Create alignment viewer | 2h | ⬜ | — |
| T005 | Calculate conservation scores | 1h | ⬜ | — |
| T006 | Add FASTA/Clustal export | 1h | ⬜ | — |
| T007 | Document workflow | 1h | ⬜ | — |

## Technical Notes
- Data: HIV-1 pol/env sequences
- Use Biopython for parsing
- Visualization: Plotly or bokeh
