# Conviction Engine

## Overview

This project investigates whether VIX-based volatility regime signals can improve capital deployment decisions relative to traditional Dollar-Cost Averaging (DCA) in passive equity investing. The long-term goal is to develop a behaviorally-optimized passive investment model that preserves index-tracking performance and index return while reducing volatility, and thereby reduce emotional execution burden for retail investors.

## Current Findings (v2)

- Backtested a four-tier VIX regime strategy (Low/Calm/Stressed/Panic) against flat DCA across 387 monthly periods (1994–2026), $38,700 total invested
- Result: Strategy IRR 8.50% vs Baseline 8.50% — statistically indistinguishable
- Max drawdown and annualized volatility identical at -53.2% and 28.8% respectively
- Key structural finding: markets spent 88.4% of the period in Low or Calm regimes, severely limiting the strategy's opportunity to deploy tactical reserves
- Conclusion: binary threshold deployment rules do not improve on DCA, but the rarity of panic regimes, not the concept, may explain the null result


## Research Roadmap

- v1: Initial VIX/SPY data exploration: complete
- v2: Four-tier binary deployment backtest: complete
- v3: Continuous VIX-scaled deployment mechanism: in progress
- v4: VVIX second-order signal integration
- v5: Behavioral simulation — modeling investor dropout under volatility stress
- White paper: Behavioral return gap and the case for a volatility-aware passive vehicle


## Motivation

DCA is theoretically optimal for long-term passive investors. But humans aren't theoretical. This project starts from a personal observation — that emotional responses to volatility cause real investors to underperform their own strategies — and works toward a systematic vehicle that removes that friction.
