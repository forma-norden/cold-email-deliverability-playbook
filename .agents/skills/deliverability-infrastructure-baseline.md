# deliverability-infrastructure-baseline

## Purpose

Set the infrastructure baseline required before any cold-email campaign launch.

## Inputs Required

- sending domains and subdomains
- mailbox provider
- sequencer platform
- DNS access owner

## Baseline Checklist

1. SPF record configured and validated
2. DKIM signing enabled and validated
3. DMARC policy configured and monitored
4. return-path and mailbox alignment checked
5. domain and inbox inventory documented

## Launch Readiness Rules

- no sends until authentication checks pass
- no shared inbox credentials
- no sudden high-volume launch from fresh infrastructure

## Output Format

- `domain`
- `spf_status`
- `dkim_status`
- `dmarc_status`
- `alignment_status`
- `launch_ready`

## Fail Conditions

Stop and request correction if:

- SPF, DKIM, or DMARC is missing
- domain owner and DNS owner are unclear
- launch requested before baseline passes

