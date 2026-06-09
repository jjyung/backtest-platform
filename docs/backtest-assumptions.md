# Backtest Assumptions

## Mandatory assumptions to state explicitly
- bar frequency
- transaction fee model
- slippage model
- fill model
- portfolio rebalancing timing
- handling of missing data
- treatment of corporate actions

## Non-negotiables
- no look-ahead bias
- no future data in signals
- reproducible input order
- deterministic results for the same seed and input

## MVP assumptions
- use one bar frequency at first
- one simple fee model
- one simple slippage model
- one-symbol strategy example

## Validation
Each run should report:
- total return
- max drawdown
- win rate or hit rate if applicable
- trade count
- average trade cost