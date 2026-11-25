# Project Specification: DietSense — ICEIB IEEE Conference Paper

## 1. Project Goal
Transform the **DietSense (營養特工)** system design and research proposal into a submission-ready **IEEE Conference (ICEIB)** academic paper draft in Overleaf-compatible LaTeX plain-text format (`c:\DIC4\ICEIB\iceib_overleaf_draft.txt`), governed by OpenSpec Spec-Driven Development (SDD).

## 2. Core Design Philosophy
**LLM for Understanding & Orchestration; Domain Engine for Computation.**
- **Semantic Layer (LLM)**: Natural language understanding, intent classification (`log_food`, `query_nutrition`, `analyze`, `recommend`), named entity recognition (NER), multi-turn session state management, and tool orchestration via Function Calling.
- **Deterministic Domain Layer (Domain Engine)**: Calorie density calculation, portion-to-gram conversion, Mifflin-St Jeor / Katch-McArdle BMR & TDEE computation, uncertainty propagation (Confidence Interval), and clinical safety guardrails.

## 3. Six-Part Research Core (A–F Cores)
- **A. Attention Getter**: Global obesity exceeds 1 billion (WHO), diet-related chronic diseases account for 74% of global deaths; Taiwan's adult overweight/obesity prevalence reaches 47.9% with over NT$50 billion in annual healthcare costs. While dietary self-monitoring doubles weight-loss success, 85% of users abandon manual tracking within 30 days.
- **B. But (Research Gap)**: Existing apps (e.g., MyFitnessPal) suffer from high manual friction and poor coverage of Taiwanese local dishes; self-reported intake errors range from 18% to 54%. General LLMs lack auditable nutrition database anchoring and exhibit a 35.8% Mean Absolute Percentage Error (MAPE) with numerical hallucinations.
- **C. Cure**: **DietSense**, a conversational Domain AI Agent combining Taiwanese localized food understanding, multi-source authoritative data anchoring, uncertainty quantification, and clinical safety guardrails.
- **D. Development**: 8-Module Architecture integrating OpenAI Whisper, multi-source parallel retrieval (USDA FoodData Central, Taiwan TFDA Food Composition Database, and a custom Taiwanese dish RAG vector store), single-turn optimal clarification loop (confidence threshold `< 0.80`), Mifflin-St Jeor TDEE engine, and hard clinical guardrails (`< 1,200 kcal` female / `< 1,500 kcal` male).
- **E. Experiments**: 500-item annotated Taiwanese local dish benchmark dataset; baselines comparing MyFitnessPal and zero-shot GPT-4o; 7-day real-world user study with 20 participants (ages 20–50); metrics covering MAPE, ±20% accuracy attainment rate, logging time (seconds), and System Usability Scale (SUS).
- **F. Findings (Expected Targets — No Fabricated Data)**: Maintain strict academic integrity by reporting expected targets only: >85% within ±20% calorie error, 60% logging time reduction (85s to <35s), SUS > 70, plus open-source deliverables (GitHub repository, 500-dish dataset, `DESIGN.md`).

## 4. Eight-Module Architecture & Tech Stack
1. **User Scenario**: Unstructured voice/text daily dietary input.
2. **Input Processing**: OpenAI Whisper ASR, Traditional/Simplified Chinese normalization, intent classification.
3. **Planner & Reasoning**: LLM central orchestrator, multi-turn context, Clarification Loop (`confidence < 0.80`).
4. **Data Retrieval**: Parallel pipeline querying USDA FoodData Central API, Taiwan TFDA database, and local Taiwanese cuisine RAG vector database.
5. **Analytics Engine**: Energy density formula, Mifflin-St Jeor & Katch-McArdle BMR/TDEE, uncertainty propagation CI.
6. **Domain Knowledge**: Taiwan Daily Dietary Guidelines, 6-food-group exchange standards, clinical safety rules.
7. **Decision & Advice**: TDEE gap analysis, guilt-free positive reframing, next-meal substitution guidance.
8. **Output & Interaction**: Structured Markdown cards, macronutrient charts, data provenance citations, and regulatory disclaimers.
