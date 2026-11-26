# Paper Refinement Specification

## ADDED Requirements

### Requirement: Academic Writing Quality
The revised IEEE conference paper (Draft V2) SHALL maintain formal, concise, objective academic English and strictly prospective framing, with zero fabricated experimental results, implementation claims, or unsupported superlatives.

#### Scenario: Prospective framing audit
- **WHEN** the manuscript discusses DietSense's system, dataset, or user study
- **THEN** all descriptions use prospective language and explicitly state that no implementation or empirical evaluation has been completed

### Requirement: Abstract and Introduction Alignment
The Abstract and Introduction SHALL present public-health motivation, Taiwanese mixed-dish logging challenges, the trust-bounded conversational approach, planned evaluation, and prospective contributions in cohesive alignment.

#### Scenario: Scope-bounded public-health motivation
- **WHEN** WHO and Taiwan HPA prevalence statistics are cited in the Abstract and Introduction
- **THEN** the text explicitly notes that prevalence motivates dietary logging research without implying clinical efficacy of tracking tools alone

### Requirement: Research Motivation and Research Gap
The manuscript SHALL define a narrow, empirically testable research gap acknowledging prior LLM, RAG, Chinese food estimation, and Taiwan image-based dietary studies, without claiming global priority.

#### Scenario: Bounded novelty positioning
- **WHEN** the research gap is stated in the Introduction and Related Work
- **THEN** it acknowledges DietAI24, FoodMapper, NutriRAG, FoodyLLM, Cao et al., and Diabot-GPT-4o and scopes DietSense's contribution to Traditional Chinese mixed-dish multi-turn logging with provenance and deterministic calculation

### Requirement: Related Work and Citation Accuracy
All bibliographic references SHALL be managed via BibTeX, verified against authoritative publications or official records, and free of fabricated metadata or unverified claims.

#### Scenario: Complete and accurate BibTeX citations
- **WHEN** Draft V2 is compiled with BibTeX
- **THEN** every `\cite{...}` resolves to an authentic entry in `references.bib` with verified authors, venue, year, and DOI/URL where applicable

### Requirement: System Architecture Consistency
The System Architecture section SHALL consistently describe the eight conceptual modules (M1--M8), the LLM-to-deterministic trust boundary, versioned data contracts, and backing data stores per `DESIGN.md` and `docs/design/architecture.md`.

#### Scenario: Architecture diagram and prose alignment
- **WHEN** comparing Fig. 1, Table II, and Section IV prose
- **THEN** all eight module identifiers (M1--M8), trust boundaries, and terminal states (`confirmed`, `draft`, `text_only`, `incomplete`) match without contradiction

### Requirement: Algorithm Correctness
The Proposed Methodology SHALL formalize deterministic nutrient scaling, multi-ingredient aggregation, evidence-bounded plausible ranges, optional Mifflin--St Jeor REE/TDEE estimation, non-blocking multi-intent request handling, and bounded clarification resumption.

#### Scenario: Non-blocking bounded clarification guarantee
- **WHEN** reviewing Algorithm 1 and Algorithm 2
- **THEN** clarification uses cross-request state persistence, enforces monotonic `turn_index < max_turns`, supports `skip`/`cancel`/`expired` terminal paths, and preserves `null` vs.\ `0` distinction

### Requirement: Experimental Methodology Rigor
The Experimental Design section SHALL specify research questions (RQ1--RQ3), the 500-item stratified dataset, four-tier reference labeling (Tiers A--D), inter-annotator reliability metrics (Cohen's $\kappa$, ICC, Bland--Altman), group-aware splitting, fixed manual-search baseline, statistical analysis plan, and 20-adult 7-day feasibility study.

#### Scenario: Candidate thresholds marked unvalidated
- **WHEN** original proposal targets ($>85\%$ within $\pm 20\%$, 60\% time reduction, SUS $>70$) appear
- **THEN** they are explicitly labeled as unvalidated exploratory candidate thresholds pending pilot calibration and preregistration

### Requirement: Research Limitations and Governance
The Discussion and Limitations section SHALL transparently document scoping-search limits, unexecuted study status, text-only observability limits (hidden oil/sauces/leftovers), non-medical safety boundaries (`pending_professional_review`), privacy/IRB prerequisites, and material DIC3 discrepancy resolutions.

#### Scenario: Material discrepancy record
- **WHEN** reviewing Section VI
- **THEN** both DIC3 resolutions (eight conceptual modules vs.\ infrastructure modules; non-blocking state machine vs.\ blocking loop) are explicitly documented

### Requirement: IEEE Two-Column Formatting
Both Draft V1 and Draft V2 SHALL use `\documentclass[conference]{IEEEtran}` with properly sized vector figures, tables, equations, and algorithms that fit the IEEE two-column layout without severe overflow.

#### Scenario: Two-column visual fit
- **WHEN** inspecting compiled PDF pages and LaTeX logs
- **THEN** all tables, TikZ diagrams, equations, and algorithms render cleanly within IEEE column/page margins

### Requirement: Clean LaTeX Compilation
Both Draft V1 (`paper/before/main.tex`) and Draft V2 (`paper/after/main.tex`) SHALL compile cleanly to PDF with zero LaTeX errors, zero unresolved cross-references, and zero undefined citations.

#### Scenario: Zero unresolved references or citations
- **WHEN** compiling `main.tex` with Tectonic/LaTeX and inspecting `main.log`
- **THEN** exit code is 0 and no `Undefined control sequence`, `Citation ... undefined`, or `Reference ... undefined` warnings remain
