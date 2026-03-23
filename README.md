# Conviction Engine

## Overview

This project explores whether volatility regimes (VIX / VVIX) can improve allocation decisions compared to traditional Dollar-Cost Averaging (DCA).

## Motivation

Passive investing strategies like DCA assume consistent investor behavior across time. However, market volatility introduces stress regimes where investors may deviate from systematic allocation.

This project investigates whether volatility indicators can provide a structural framework for improving allocation decisions.

## Current Progress

- Initial data exploration (SPY, VIX)
- Observing relationship between market drawdowns and volatility spikes

## Next Steps

- Add VVIX data
- Define volatility regimes
- Build rule-based allocation strategy
- Backtest vs DCA baseline

## Repository Structure

- `data/` – raw and processed data  
- `notebooks/` – exploratory analysis  
- `src/` – core logic and models  
- `outputs/` – charts and results  
