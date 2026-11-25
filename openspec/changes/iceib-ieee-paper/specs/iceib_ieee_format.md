# Specification: ICEIB IEEE Conference Overleaf Format (`iceib_ieee_format`)

## 1. Output Artifact & Reference Sources
- **File Path**: `c:\DIC4\ICEIB\iceib_overleaf_draft.txt`
- **Encoding**: UTF-8 plain text containing complete, self-contained LaTeX source code ready to be pasted into Overleaf.
- **Authoritative Sources**:
  - `c:\DIC4\A2Z outline example.pdf` (2020 A-Z SOP structure)
  - `c:\DIC4\AIoT-DIC3-ProposalRefactor\DESIGN.md`
  - `c:\DIC4\AIoT-DIC3-ProposalRefactor\README.md`
  - `c:\DIC4\AIoT-DIC3-ProposalRefactor\DietSense 營養特工.pdf`
  - `c:\DIC4\AIoT-DIC3-ProposalRefactor\DietSense 營養特工研究提案.png`
  - `c:\DIC4\myRef\` corresponding backup files

## 2. LaTeX Document Class & Required Packages
- Document class: `\documentclass[conference]{IEEEtran}`
- Required packages: `cite`, `amsmath,amssymb,amsfonts`, `graphicx`, `booktabs`, `algorithm`, `algpseudocode`, `url`.

## 3. Mandatory 2020 A–Z SOP Section Mapping & Tagging
Every section must include explicit LaTeX comments (`% [TAG] ...`) corresponding to `A2Z outline example.pdf`:
1. **Abstract (`A–F`)**: `[A]` Attention Getter, `[B]` But, `[C]` Cure, `[D]` Development, `[E]` Experiments, `[F]` Findings (expected targets only).
2. **I. Introduction (`G–L`)**: `[G]` General, `[H]` However, `[I]` In literature (old to new, simple to complex), `[J]` Judgement (SWOT summary), `[K]` Keypoint (novelty & contribution summary), `[L]` List the organization.
3. **II. Related Work (`M–O`)**: `[M]` Methods (categorized old to new, simple to complex), `[N]` New proposed, `[O]` Organize (4x5 SWOT comparison `table*`).
4. **III. Proposed Scheme (`PA–PM`)**:
   - `[PA]` Aim / Statement, `[PB]` Based on / Background / Benefit, `[PC]` Cure / Cause, `[PD]` Design & Paradigm Shift, `[PE]` Paper Elements (8 modules table), `[PF]` Formulation / Foundation, `[PG]` Graph (architecture figure placeholder & flow description), `[PH]` How (clarification loop, degradation, safety net, guilt-free reframing), `[PI]` Implementation / Pseudocode (`Algorithm 1`), `[PJ]` Jump to an Example (beef noodle soup walkthrough), `[PK]` Key Points Contribution, `[PL]` Later how to do simulation, `[PM]` Math Proof (uncertainty monotonicity, convex weighting, clinical floor invariant).
5. **IV. Simulation (`Q–V`)**:
   - `[Q]` Quality and Quantity metrics, `[R]` Related methods to compare, `[S]` Simulation Setup, `[T]` Tuning parameters, `[U]` Useful results (strictly expected targets, no fabricated data), `[V]` Verify effectiveness criteria.
6. **V. Conclusion (`W–Z`)**:
   - `[W]` What proposed, `[X]` eXcel, `[Y]` Yields, `[Z]` Zen (future work & research contributions).
7. **References**: `\begin{thebibliography}{00}` with 100% 1-to-1 `\cite` / `\bibitem` consistency.

## 4. Overleaf Zero-Error Compilation & Academic Integrity Rules
- Escape all special LaTeX characters in prose (`\_`, `\%`, `\&`, `\#`, `\$`).
- Never fabricate experimental results; clearly mark `[E]`, `[F]`, `[U]`, `[V]`, `[Y]` as planned evaluation protocols and expected targets.
