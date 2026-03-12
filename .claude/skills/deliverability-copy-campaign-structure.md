# deliverability-copy-campaign-structure

## Purpose

Apply copy and campaign structure rules that reduce deliverability risk while
keeping reply potential.

## Inputs Required

- target segment definition
- campaign objective
- sequence length
- CTA policy

## Copy Safety Rules

1. keep first touch short and single-purpose
2. avoid heavy formatting in initial emails
3. avoid unnecessary links or attachments in first touch
4. use one low-friction CTA
5. align message with segment pain and context

## Campaign Structure Rules

1. enforce sequence spacing policy
2. cap simultaneous launches from one mailbox pool
3. vary templates responsibly without random incoherence
4. suppress non-responsive contacts after policy threshold

## Output Format

- `sequence_id`
- `email_step`
- `copy_goal`
- `cta_type`
- `format_risk`
- `send_ready`

## Fail Conditions

Stop and request correction if:

- first-touch template violates safety rules
- CTA policy is missing
- suppression policy is undefined

