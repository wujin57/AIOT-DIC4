# Tasks: Refine DietSense IEEE Conference Paper (`refine-ieee-paper`)

## 1. Academic Writing, Abstract, and Introduction
- [x] 1.1 Tighten Abstract and Introduction prose for IEEE conference conciseness and strictly prospective framing.
- [x] 1.2 Ensure WHO and Taiwan HPA prevalence statistics are explicitly decoupled from clinical efficacy claims.
- [x] 1.3 Sharpen the research gap statement to explicitly acknowledge DietAI24, FoodMapper, NutriRAG, FoodyLLM, Lawabni et al., Cao et al., and Diabot-GPT-4o.

## 2. Related Work and Citation Verification
- [x] 2.1 Expand Related Work synthesis and add official Taiwan HPA DRIs (8th ed.) and FDA/CFIA nutrition-labeling energy-factor references to `references.bib`.
- [x] 2.2 Verify all BibTeX entries against DIC3 evidence ledgers and authoritative publication records.

## 3. Methodology, Equations, and Algorithms
- [x] 3.1 Verify Equations (1)--(4) for deterministic scaling, multi-ingredient aggregation with null preservation, evidence-bounded plausible ranges, and Mifflin--St Jeor REE/TDEE eligibility.
- [x] 3.2 Add Algorithm 2 (Bounded Clarification Resumption and Conflict Resolution) to pair with Algorithm 1 and guarantee monotonic termination.

## 4. System Architecture and Visual Diagrams
- [x] 4.1 Verify eight-module architecture (M1--M8), trust boundary, and data-contract consistency against `DESIGN.md` and `docs/design/architecture.md`.
- [x] 4.2 Add Fig. 2 (Clarification and Graceful-Degradation State Machine) as a clean single-column TikZ diagram matching `docs/design/architecture.md` §4.

## 5. Experimental Design and Limitations
- [x] 5.1 Expand Experimental Design with formal primary/secondary outcome designation, cluster-aware statistical analysis (paired differences, bootstrap CI), and preregistration checklist.
- [x] 5.2 Strengthen Discussion and Limitations with explicit governance, safety-review status, observability boundaries, and DIC3 discrepancy resolutions.

## 6. IEEE Formatting, Compilation, and Verification
- [x] 6.1 Compile Draft V1 (`paper/before/main.tex`) and Draft V2 (`paper/after/main.tex`) to PDF and verify zero unresolved citations or cross-references.
- [x] 6.2 Validate OpenSpec artifacts using `openspec validate --all --strict` and record all evidence honestly in `verification.md` (including Overleaf MCP unavailability).
