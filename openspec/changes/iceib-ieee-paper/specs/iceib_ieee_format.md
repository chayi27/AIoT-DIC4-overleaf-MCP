# Specification: ICEIB IEEE Conference Overleaf Format (`iceib_ieee_format`)

## 1. Output Artifact
- **File Path**: `c:\DIC4\ICEIB\iceib_overleaf_draft.txt`
- **Encoding**: UTF-8 plain text containing complete, self-contained LaTeX source code ready to be pasted into Overleaf.

## 2. LaTeX Document Class & Required Packages
- Document class: `\documentclass[conference]{IEEEtran}`
- Required packages:
  - `cite`
  - `amsmath,amssymb,amsfonts`
  - `graphicx`
  - `booktabs`
  - `algorithm`
  - `algpseudocode`
  - `url` (or `hyperref` if compatible with IEEEtran, prefer `url` for clean IEEE compilation)

## 3. Mandatory Sections & Content Rules
1. **Title & Author Block**: Use `\title{...}` and `\author{\IEEEauthorblockN{...}\IEEEauthorblockA{...}}` with clear placeholders for author names, affiliations, and emails.
2. **Abstract**: 150–250 words summarizing motivation, research gap, DietSense architecture, evaluation plan, and expected targets.
3. **Index Terms**: `\begin{IEEEkeywords} ... \end{IEEEkeywords}` (4–5 concise terms).
4. **I. Introduction**: Grounded in A–C cores from `DESIGN.md` and `DietSense 營養特工.pdf`.
5. **II. Related Work**: Covers manual tracking apps, image-based food volume estimation, general-purpose LLMs, and domain-specific AI agents.
6. **III. System Architecture and Methodology**:
   - 8-Module Architecture table or structured description.
   - Core mathematical formulas: Energy density $E$, Mifflin-St Jeor $\text{BMR}_{\text{male/female}}$, $\text{TDEE}$, Katch-McArdle BMR, Yield Factor conversion, and Uncertainty Propagation $\sigma_{\text{total}}$ with confidence interval.
   - **Algorithm 1**: `DietSense` pseudocode formatted cleanly with `algorithm` and `algpseudocode`.
   - Three Architectural Trade-offs (Accuracy vs. UX, Quantity vs. Quality, General Guidelines vs. Personalization) and core edge-case mechanisms (Clarification Loop, Geographical Proximity Weighting, Oil Absorption, Graceful Degradation, Clinical Safety Guardrails, Guilt-free Reframing, Data Provenance).
7. **IV. Experimental Setup and Evaluation Plan**:
   - Faithfully reflects the 500-dish Taiwanese benchmark, MyFitnessPal & GPT-4o baselines, 20-participant 7-day study, and metrics (MAPE, ±20% attainment, logging time, SUS).
   - **Strict Academic Integrity**: No fabricated experimental results; clearly state expected targets (>85% within ±20%, 60% time reduction from 85s to <35s, SUS > 70).
8. **V. Conclusion**: Summarizes contributions, open-source handover artifacts, and future work.
9. **References**: `\begin{thebibliography}{00} ... \end{thebibliography}` formatted in standard IEEE style.

## 4. Overleaf Zero-Error Compilation Rules
- Escape all special LaTeX characters in prose: `\_`, `\%`, `\&`, `\#`, `\$`.
- Ensure all math symbols (`\sigma`, `\Delta`, `\ge`, `\le`, `\times`, `\approx`) are enclosed in `$...$` or `$$...$$` / `equation` environments.
- Avoid undefined macros or missing `.png` file inclusions that would fail compilation if the image is not uploaded (or comment out `\includegraphics` with a clear Overleaf instruction note if referenced, using `booktabs` tables and `algorithm` blocks that compile natively without external assets).
