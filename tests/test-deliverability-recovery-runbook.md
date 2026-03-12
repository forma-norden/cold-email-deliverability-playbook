# Test: deliverability-recovery-runbook

Load skill: `.claude/skills/deliverability-recovery-runbook.md`

## Prompt

```text
Read .claude/skills/deliverability-recovery-runbook.md

Inputs:
- incident id: DELIV-2026-03-11-01
- containment already applied: volume reduced by 50%
- unresolved issue: complaint rate still above internal threshold
- owner: revops-lead
- recovery objective: stable performance in 14 days

Return phased recovery plan and exit criteria.
```

## Must Pass Checklist

- [ ] Includes contain, correct, rebuild phases
- [ ] Includes clear exit criteria
- [ ] Includes ownership and review checkpoint
- [ ] Includes no-panic-rotation behavior
- [ ] Includes fail conditions

## Failure Indicators

- No phased plan
- No exit criteria
- No ownership model

