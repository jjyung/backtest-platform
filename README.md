# backtest-platform

A research-first, event-driven backtesting platform.

## Goal
Provide a small but trustworthy foundation for strategy research, with explicit event contracts, reproducible assumptions, and testable results.

## Scope
- ingest cleaned market data
- convert data into events
- simulate orders and fills
- compute performance metrics
- support walk-forward style research

## MVP
1. Define the event contracts
2. Implement a minimal event loop
3. Add a single strategy example
4. Emit trades, fills, and metrics

## Repo layout
- `docs/` — architecture and contract docs
- `src/` — package code
- `tests/` — unit tests

## Status
This repo starts with contracts and a tiny runnable skeleton, not a full platform.