# Change Proposal: Refine DietSense IEEE Conference Paper (`refine-ieee-paper`)

## Why
Draft V1 (`paper/before/main.tex`) establishes the initial IEEEtran conference proposal for DietSense based on the DIC3 source repository. However, to meet publication-grade IEEE conference standards, the manuscript requires systematic refinement across ten dimensions: academic writing precision, abstract/introduction alignment, explicit research motivation and bounded research gap, related-work synthesis and citation completeness, eight-module architecture and data-contract consistency, formal algorithm completeness (including clarification resumption and terminal states), statistical rigor in the prospective experimental design, comprehensive research limitations and governance boundaries, strict IEEE two-column formatting, and clean LaTeX/BibTeX compilation with zero unresolved references.

## What Changes
- **Abstract & Introduction:** Tighten scope-bounded wording (avoiding overbroad claims), align public-health context with the testable workflow gap, and clarify prospective contributions without implying completed implementation.
- **Related Work & Citations:** Expand synthesis of recent 2025--2026 nutrition LLM studies (DietAI24, FoodMapper, NutriRAG, FoodyLLM, Lawabni et al., Cao et al., Diabot-GPT-4o) alongside food NER/NEL, portion estimation, and safety literature; verify all BibTeX entries against authoritative records and add Taiwan HPA DRIs and FDA/CFIA labeling references.
- **Proposed Methodology & Algorithms:** Add explicit clarification-resume state transition (`Algorithm 2`), strengthen equations for deterministic scaling, multi-ingredient aggregation, evidence-bounded plausible ranges, and Mifflin--St Jeor REE/TDEE eligibility, and ensure 100% consistency with `DESIGN.md` and `docs/design/algorithms.md`.
- **System Architecture:** Add a dedicated clarification/degradation state-transition diagram (`Fig. 2`) complementing the eight-module trust-bounded architecture (`Fig. 1`), and verify alignment between modules M1--M8, data contracts, and terminal states.
- **Experimental Design:** Formalize primary vs.\ secondary outcomes, cluster-aware statistical analysis (paired differences, bootstrap CI, Cohen's $\kappa$, ICC, Bland--Altman), and protocol preregistration checklist while keeping all candidate thresholds explicitly unvalidated.
- **Discussion, Limitations & IEEE Formatting:** Expand governance, safety, observability, and material DIC3 discrepancy records; verify all figures, tables, equations, and algorithms fit IEEE two-column layout with zero unresolved references/citations.

## Impact
- **Preserved Artifact:** `paper/before/` (Draft V1) remains unmodified as the baseline.
- **Revised Artifact:** `paper/after/` (Draft V2) implements all specification requirements and passes LaTeX/BibTeX compilation.
- **Overleaf MCP Note:** Overleaf MCP server is unavailable/unconfigured in the current environment; local LaTeX compilation and OpenSpec validation are executed transparently without fabricating MCP logs.
