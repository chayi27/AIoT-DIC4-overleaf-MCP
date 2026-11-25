# Proposal: ICEIB IEEE Conference Paper Draft (`iceib-ieee-paper`)

## 1. Proposed Paper Title
**DietSense: A Conversational Domain AI Agent for Localized Calorie Tracking with Multi-Source Anchoring, Uncertainty Quantification, and Clinical Safety Guardrails**

## 2. Core Research Contributions
1. **Decoupled Agentic Architecture**: Enforces strict separation between LLM semantic orchestration and deterministic nutritional computation to eliminate LLM numerical hallucination (35.8% MAPE).
2. **Three-Tier Localized Food Anchoring**: Combines authoritative ground-truth databases (Taiwan TFDA, USDA FoodData Central), a 500-dish nutritionist-verified Taiwanese cuisine RAG vector store, and dynamic composite recipe decomposition for street food and bento meals.
3. **Single-Turn Optimal Clarification & Uncertainty Propagation**: Uses a sensitivity-prioritized clarification loop (`confidence < 0.80`) and reports honest calorie confidence intervals `[kcal_low, kcal_high]` instead of false-precision point estimates.
4. **Hard Clinical Safety Guardrails & Guilt-Free Guidance**: Enforces non-bypassable intake floors (1,200 kcal/day female, 1,500 kcal/day male), eating-disorder interception, and positive cross-meal reframing.

## 3. Planned Paper Structure (IEEEtran Two-Column)
- **Title & Author Block** (with placeholder affiliations/emails for Overleaf)
- **Abstract** (150–250 words) & **Index Terms**
- **I. Introduction** (A–C Cores: Global/Taiwanese health crisis, manual tracking abandonment, LLM numerical hallucination, DietSense positioning)
- **II. Related Work** (Traditional calorie trackers, vision-based estimation, general LLMs in nutrition, domain-specific AI agents)
- **III. System Architecture and Methodology** (8-Module Architecture, Algorithm 1 pseudocode, mathematical formulations, 3 architectural trade-offs, and key technical mechanisms: clarification loop, multi-source conflict resolution, cooking yield & oil absorption, uncertainty propagation, graceful degradation, clinical safety guardrails)
- **IV. Experimental Setup and Evaluation Plan** (500-dish Taiwanese benchmark, MyFitnessPal & GPT-4o baselines, 20-participant 7-day protocol, evaluation metrics, expected targets without fabricated data)
- **V. Conclusion** (Summary of contributions, deliverables, and future clinical validation)
- **References** (Standard IEEE `\begin{thebibliography}{00}`)

## 4. Target Output Path
- `c:\DIC4\ICEIB\iceib_overleaf_draft.txt`
