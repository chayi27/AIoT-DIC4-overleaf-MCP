# 004-simulation (`Q–V`)
- **[Q] Quality & Quantity**: MAPE, ±20% attainment rate, per-meal logging time (s), SUS score.
- **[R] Related Methods**: MyFitnessPal & zero-shot GPT-4o (35.8% MAPE).
- **[S] Simulation Setup**: 500-dish Taiwanese benchmark dataset + 20-participant (ages 20–50) 7-day real-world study.
- **[T] Tuning Parameters**: $\tau = 0.80$, max 1 clarification turn, weights `(0.5, 0.4, 0.1)`, $\sigma_{\text{total}} \in \{0.05, 0.15, 0.35\}$, clinical floors `1,200/1,500` kcal, 14-day EMA.
- **[U] Useful Results**: Expected targets only (>85% within ±20%, 60% time reduction to <35s, SUS >70).
- **[V] Verify Effectiveness**: Statistical significance & zero clinical guardrail bypasses across 140 participant-days.
