# Conviction Engine

## Overview

This project investigates whether VIX-based volatility regime signals can improve capital deployment decisions relative to traditional Dollar-Cost Averaging (DCA) in passive equity investing. The long-term goal is to develop a behaviorally-optimized passive investment model that preserves index-tracking performance and index return while reducing volatility, and thereby reduce emotional execution burden for retail investors.

## Current Findings (v4)

- Cash management remains difficult to justify for long-term DCA investors (CE v3).
- Both methods will result in an improvement in IRR but deterioration of Sharpe Ratio. 
- Timing leverage may be more important than maintaining leverage continuously. Increasing exposure selectively during periods of elevated volatility appears more promising than delaying investment.
- Synthetic leverage (v4a) provides a theoretically grounded framework that remains profitable even after financing costs.
- Leveraged ETF implementation (v4b) offers a practical alternative for retail investors, though its historical performance is heavily influenced by major market recoveries and therefore requires continued robustness testing.


## Research Roadmap

- v1: Initial VIX/SPY data exploration: complete
- v2: Four-tier binary deployment backtest: complete
- v3: Continuous VIX-scaled deployment mechanism: complete
- v4a: Conditional leverage with cash borrowing: complete
- v4b: Conditional leverage with leveraged ETF vehicles: complete
- White paper: The Conviction Engine: A Behaviorally-Motivated Volatility-Conditional DCA Framework


## Motivation

DCA is theoretically optimal for long-term passive investors. But humans aren't theoretical. This project starts from a personal observation — that emotional responses to volatility cause real investors to underperform their own strategies — and works toward a systematic vehicle that removes that friction.
