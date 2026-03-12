# deliverability-monitoring-diagnostics

## Purpose

Diagnose deliverability performance drops using metrics first, then produce a
ranked root-cause model and immediate containment actions.

## Inputs Required

- reply trend
- bounce rate
- complaint rate
- inbox placement checks
- recent campaign and infra changes

## Diagnostic Sequence

1. validate data quality and period consistency
2. assess delivery vs inbox placement
3. inspect engagement trends
4. inspect bounce and complaint behavior
5. compare current sending behavior to baseline
6. rank probable root causes

## Root-Cause Categories

- infrastructure and authentication issues
- list quality and targeting issues
- behavior and volume-pattern issues
- copy and campaign-structure issues

## Output Format

- `diagnostic_period`
- `metric_snapshot`
- `root_cause_ranked`
- `containment_actions`
- `stabilization_plan`
- `go_no_go_recheck_date`

## Fail Conditions

Stop and request correction if:

- critical metrics are missing
- data periods are inconsistent
- recent-change log is unavailable

