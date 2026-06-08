# SmartLens — Risk Register

| # | Risk | Likelihood | Impact | Score | Mitigation |
|---|---|---|---|---|---|
| R1 | Scope creep — adding features mid-project | High | High | 9 | Strict adherence to scope doc; new ideas deferred to v2 |
| R2 | Power BI forecasting limited on free tier | Low | Medium | 2 | Fallback: Python script visual or Excel FORECAST.ETS |
| R3 | LLM API rate limits or latency | Medium | Low | 2 | Pre-generate static summaries for demo if needed |
| R4 | Simulated data not credible enough | Low | Medium | 2 | Base simulation on SME financial benchmarks |
| R5 | Unstable internet delays publishing | Medium | Medium | 4 | Batch uploads; keep local .pbix as offline backup |
| R6 | Time underestimate — tasks take longer than planned | Medium | High | 6 | 1-day buffer per week; AI layer scoped as stretch goal |

## Scoring
- Likelihood × Impact (each rated 1=Low, 2=Medium, 3=High)
- Score 6–9: High priority — immediate action required
- Score 3–4: Medium — monitor closely
- Score 1–2: Low — accept and watch
