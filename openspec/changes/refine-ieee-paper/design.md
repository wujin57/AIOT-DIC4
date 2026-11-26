# Design: OpenSpec-Driven IEEE Paper Refinement

## Context
The DietSense DIC3 source repository (`DESIGN.md`, `docs/design/architecture.md`, `docs/design/algorithms.md`, `docs/design/evaluation-plan.md`, `docs/final/DietSense-Final-Proposal.md`, and `docs/research/*`) serves as the single source of truth. Two material inconsistencies between earlier DIC3 documents and the detailed system design specification are resolved in favor of `DESIGN.md` and `docs/design/`:
1. **Eight Conceptual Modules:** M1 User/Application Layer, M2 Input Processing, M3 Planner/Reasoning, M4 Data Retrieval, M5 Analytics Engine, M6 Domain Knowledge, M7 Decision/Recommendation, and M8 Output/Interaction (with databases/registries as backing data stores rather than conceptual modules 7--8).
2. **Non-Blocking Clarification:** Cross-request state machine (`handle_request` + `resume_clarification`) with bounded `turn_index < max_turns`, explicit `skip`/`cancel`/`expired` terminal paths, and no blocking `while` loop.

## Goals / Non-Goals
- **Goals:**
  - Elevate Draft V1 to a rigorous, publication-ready IEEE conference proposal (Draft V2) while strictly maintaining prospective tone (zero fabricated experimental results or implementation claims).
  - Ensure every claim is traceable to verified DIC3 evidence ledgers or authoritative bibliographic sources.
  - Achieve zero unresolved LaTeX references, zero undefined citations, and clean two-column IEEEtran layout.
- **Non-Goals:**
  - Do not implement DietSense application code, collect dataset entries, or run human-subject experiments.
  - Do not fabricate Overleaf MCP logs or claim Overleaf MCP execution when no MCP server is configured.

## Key Design Decisions
- **Dual-Algorithm Formalization:** Present both `Algorithm 1` (Non-Blocking Multi-Intent Request Handling) and `Algorithm 2` (Bounded Clarification Resumption and Conflict Resolution) in Draft V2 so every state transition from `docs/design/algorithms.md` §10 is formally specified.
- **Visual Clarity in IEEE Two-Column Layout:** Use crisp vector TikZ diagrams for both `Fig. 1` (two-column eight-module trust-bounded architecture) and `Fig. 2` (single-column clarification and graceful-degradation state machine), avoiding bitmap scaling artifacts.
- **Strict Prospective Guardrails:** Every mention of the 500-item dataset, 20-participant 7-day study, and candidate thresholds ($>85\%$ within $\pm 20\%$, 60\% time reduction, SUS $>70$) must explicitly state that they are prospective/unvalidated.
