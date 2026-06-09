# Architecture

## Principles
- event-driven first
- reproducible by default
- no hidden data leakage
- assumptions must be explicit
- output must be inspectable and testable

## Pipeline
1. load cleaned market data
2. transform rows into market events
3. feed events into strategy logic
4. generate orders
5. simulate fills
6. update portfolio state
7. emit results and metrics

## Core modules
- `data` — adapters for cleaned datasets
- `events` — canonical event objects or dict contracts
- `engine` — event loop and orchestration
- `execution` — fills and cost model
- `portfolio` — positions and PnL
- `metrics` — summary statistics

## First milestone
A single-symbol daily-bar strategy should run end-to-end with deterministic output.