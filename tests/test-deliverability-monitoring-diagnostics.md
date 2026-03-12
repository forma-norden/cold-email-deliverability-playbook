# Test: deliverability-monitoring-diagnostics

Load skill: `.claude/skills/deliverability-monitoring-diagnostics.md`

## Prompt

```text
Read .claude/skills/deliverability-monitoring-diagnostics.md

Inputs:
- reply trend: down 35% over 2 weeks
- bounce rate: 2.8%
- complaint rate: 0.14%
- placement check: mixed inbox and spam
- recent changes: volume increased by 60% in one week

Return ranked root causes and containment actions.
```

## Must Pass Checklist

- [ ] Includes metric-led diagnostic sequence
- [ ] Includes ranked root-cause output
- [ ] Includes containment actions
- [ ] Includes stabilization plan and recheck date
- [ ] Includes fail conditions for missing data

## Failure Indicators

- No ranking of root causes
- No containment actions
- No data-quality validation step

