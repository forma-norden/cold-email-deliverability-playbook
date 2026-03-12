# Test: deliverability-copy-campaign-structure

Load skill: `.claude/skills/deliverability-copy-campaign-structure.md`

## Prompt

```text
Read .claude/skills/deliverability-copy-campaign-structure.md

Inputs:
- segment: VP Sales at B2B SaaS companies
- sequence length: 4 steps
- first-touch CTA: reply with interest
- policy: no links in first touch

Return copy and campaign structure compliance framework.
```

## Must Pass Checklist

- [ ] Includes first-touch copy safety rules
- [ ] Includes sequence spacing and suppression requirements
- [ ] Includes CTA policy enforcement
- [ ] Includes send-ready output fields
- [ ] Includes fail conditions

## Failure Indicators

- No first-touch safety controls
- No suppression policy
- No compliance output structure

