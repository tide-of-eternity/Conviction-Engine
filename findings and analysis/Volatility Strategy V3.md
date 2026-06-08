## V3: Continuous Cash-Constrained Volatility Allocation

### Hypothesis
A continuously-scaled volatility-conditioned allocation framework that builds and deploys cash reserves may improve the behavioral sustainability of DCA without sacrificing long-term performance.

---

### Methodology
Monthly budget: $100
Benchmark: Standard flat DCA ($100/month, no regime conditioning)
Regime rules (continuous scaling):
VIX <20: Invest = $100, Save = S0
20 ≤ VIX < 28: Invest = $95, Save = $5
VIX ≥ 28: Invest = $100 + all saved capital deployed, Save = $0
- Benchmark: Standard DCA

---

### Visulization

![VIX Regime 3.0](https://github.com/tide-of-eternity/Conviction-Engine/blob/main/outputs/VIX%20Regime%20vontinuous%20tier%20v3.pdf)

---

### Interpretation

- V3 underperforms DCA on every primary metric. The IRR deficit of 0.46pp compounds to a ~$19,746 gap in terminal value over 32 years — a material drag, not a rounding error.
- Structural underinvestment is the root cause. The strategy deployed an average of only $88.35/month against DCA's $100, spending 344 of 390 months in saving mode with an avg VIX scale factor of just 0.21.
- The deployment trigger was too infrequent. VIX ≥ 28 fired in only 46 months across 32 years, providing too few windows to recover the compounding lost during accumulation phases.
- The reserve was never unwound. The cash buffer reached a peak of $4,542 and remained there at period-end — a meaningful block of capital sitting idle in perpetuity, earning zero return.
- Risk reduction is real but insufficient. Max drawdown improved by 4.4pp and annualised volatility fell 0.8pp, but Sharpe still favours the baseline (0.313 vs 0.306), confirming the return sacrifice exceeds the risk reduction.
- V3 is structurally conservative, not tactically superior. It is not a better strategy than DCA — it is a more cautious one that pays a measurable and persistent performance cost for its regime structure.

---

### Key Insight

- Idle cash is the fatal flaw. Regime-conditional saving without a yield-bearing reserve is structurally equivalent to systematic underinvestment — the behavioral benefit of a rules-based deployment mechanism cannot justify idle cash drag over a full market cycle.
- The mechanism is sound; the implementation is not. The regime-detection logic correctly identifies stress periods and responds with increased capital deployment. The failure is that the reserve earns nothing between triggers.
- V3 defines the ceiling of the savings-based approach. No further tuning of VIX thresholds or scaling functions can solve the fundamental problem: cash not in the market is cash not compounding.

---

### Limitation

- The reserve was never fully deployed, revealing that the VIX ≥ 28 trigger is too infrequent to recycle capital at a pace that offsets accumulation drag
- Cash reserves earn zero return, making every month of saving a compounding penalty relative to the benchmark
- The continuous VIX scaling formula (avg scale factor 0.21) kept most months in mild-saving territory, producing structural underinvestment rather than genuine tactical timing
- Results are sensitive to the VIX scaling bounds and trigger thresholds, which were not formally optimised
- No transaction costs or tax friction modelled; real-world implementation would widen the performance gap further

---



### Future Direction
V4 will replace idle cash reserves with conditional leverage at VIX ≥ 28 and ≥ 35, eliminating drag while preserving the regime-responsive deployment structure.
