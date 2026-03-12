# Test: deliverability-infrastructure-baseline

Load skill: `.claude/skills/deliverability-infrastructure-baseline.md`

## Prompt

```text
Read .claude/skills/deliverability-infrastructure-baseline.md

Inputs:
- domains: send-alpha.com, send-beta.com
- provider: Google Workspace
- sequencer: Smartlead
- DNS owner: ops@company.com

Return pre-launch readiness checklist and launch decision.
```

## Must Pass Checklist

- [ ] Includes SPF, DKIM, DMARC checks
- [ ] Includes alignment and ownership checks
- [ ] Includes launch-ready decision logic
- [ ] Includes structured output fields
- [ ] Includes fail conditions

## Failure Indicators

- Authentication checks are incomplete
- No launch gate decision
- No owner accountability

