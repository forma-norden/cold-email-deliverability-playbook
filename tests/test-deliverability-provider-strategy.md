# Test: deliverability-provider-strategy

Load skill: `.claude/skills/deliverability-provider-strategy.md`

## Prompt

```text
Read .claude/skills/deliverability-provider-strategy.md

Inputs:
- provider mix: Google Workspace and Microsoft 365
- target volume: 4,000 emails per week
- warm-up stage: week 3
- risk tolerance: medium-low

Return provider strategy and ramp policy.
```

## Must Pass Checklist

- [ ] Includes controlled ramp policy
- [ ] Includes hold and rollback conditions
- [ ] Includes provider-specific cap fields
- [ ] Includes warning signals for adjustment
- [ ] Includes fail conditions

## Failure Indicators

- Suggests aggressive ramp without controls
- No rollback logic
- No provider strategy output structure

