# deliverability-recovery-runbook

## Purpose

Run structured recovery when deliverability degrades, without panic rotations or
uncontrolled changes.

## Inputs Required

- diagnostic output
- active campaign inventory
- mailbox and domain inventory
- recovery time objective

## Recovery Phases

### Phase 1: Contain

- pause highest-risk campaigns
- reduce send volume to safe baseline
- stop new experiment launches

### Phase 2: Correct

- fix authentication or infra defects
- remove low-quality segments
- adjust sequence structure and cadence

### Phase 3: Rebuild

- resume with controlled ramp
- track metrics daily
- reintroduce complexity only after stabilization

## Exit Criteria

Recovery complete only when:

- complaint trend stabilizes
- bounce trend stabilizes
- inbox placement improves consistently
- reply performance no longer degrades

## Output Format

- `incident_id`
- `containment_actions`
- `correction_actions`
- `rebuild_plan`
- `exit_criteria_status`
- `next_review_date`

## Fail Conditions

Stop and request correction if:

- incident owner is missing
- no baseline metrics are available
- ramp plan is missing after containment

