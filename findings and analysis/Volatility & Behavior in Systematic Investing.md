## Conviction Engine — Volatility & Behavior in Systematic Investing

### Objective
To evaluate whether volatility-based allocation rules can improve upon Dollar-Cost Averaging (DCA), and to explore how systematic frameworks can address behavioral challenges in long-term investing.

---

### Hypothesis
Increasing allocation to equities during periods of high volatility (VIX > 28) may enhance long-term returns by capturing market stress opportunities.

---

### Data & Methodology
- Assets: SPY, VIX, VVIX  
- Frequency: Daily  
- Period: ~30 years  
- Strategy:
  - Baseline: Standard DCA
  - Test: Increase allocation when VIX > 28  

---

# Visualization
![DCA vs VIX Regime Strategy](outputs/VIX Regime Backtest.pdf)

---

# Key Result
The volatility-triggered strategy (buy more when VIX > 28) does **not outperform** standard DCA over the full sample period.

---

# Interpretation
This result suggests:

- Volatility spikes are not sufficient as standalone entry signals  
- Market drawdowns can persist beyond initial volatility increases  
- Increasing exposure during stress without additional structure may amplify risk  

Additionally, VVIX appears largely **contemporaneous** with VIX, rather than predictive, limiting its usefulness as a leading signal.

---

# Insight
Simple “buy-the-fear” rules do not reliably improve systematic investment outcomes.

This highlights a deeper issue:

> The challenge of investing is not only identifying opportunities, but designing systems that remain robust under stress.

---

# Next Direction (V2)
Rather than attempting to outperform DCA, the next phase focuses on:

- Designing a **volatility-conditioned allocation framework**
- Maintaining **DCA-like returns**
- Improving **behavioral sustainability during high-stress regimes**

Planned approach:
- Scale allocation (instead of binary decisions)
- Incorporate simple regime structure (e.g., volatility bands)

---

# Key Question
If DCA is already efficient, can we design a system that:

> Preserves its performance while making it easier for investors to stay consistent?
