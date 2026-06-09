# Event Contracts

## Canonical events
- `MarketEvent`
  - symbol
  - timestamp
  - open/high/low/close/volume
- `SignalEvent`
  - symbol
  - timestamp
  - side
  - confidence or strength
- `OrderEvent`
  - symbol
  - timestamp
  - side
  - quantity
  - order type
- `FillEvent`
  - symbol
  - timestamp
  - side
  - quantity
  - fill price
  - fee
  - slippage

## Rules
- Every event must carry a timestamp.
- Fill timestamps must not precede order timestamps.
- Strategy decisions may only use information available at or before the current event timestamp.
- Event payloads must be serializable for logs and tests.

## Output contracts
The engine must emit:
- trades
- fills
- portfolio snapshots
- performance metrics