# deliverability-provider-strategy

## Purpose

Define provider-specific strategy for mailbox mix, sending cadence, and ramp-up
behavior.

## Inputs Required

- provider mix
- target send volume
- warm-up stage
- risk tolerance

## Strategy Rules

1. choose conservative volume during early trust period
2. scale only when engagement and complaint metrics are stable
3. avoid abrupt behavior changes
4. separate high-risk experiments from core sending pool

## Ramp Policy

- start low
- increase gradually
- hold or reduce volume on warning signals

Warning signals:

- rising complaints
- rising bounces
- falling reply rates with unchanged targeting quality

## Output Format

- `provider`
- `inbox_pool_size`
- `daily_cap_per_inbox`
- `ramp_step`
- `hold_conditions`
- `rollback_conditions`

## Fail Conditions

Stop and request correction if:

- send volume target is undefined
- warm-up state is unknown
- no rollback conditions are defined

