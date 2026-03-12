# CLAUDE.md - cold-email-deliverability-playbook

This repo defines operator workflows for cold-email deliverability.

## Skills in This Repo

| Skill | When to use it |
|-------|---------------|
| `deliverability-infrastructure-baseline` | preparing domain and DNS authentication before launch |
| `deliverability-provider-strategy` | selecting mailbox-provider strategy and ramp policy |
| `deliverability-copy-campaign-structure` | enforcing low-risk copy and sequence structure |
| `deliverability-monitoring-diagnostics` | diagnosing performance drops with metric-led analysis |
| `deliverability-recovery-runbook` | recovering from inbox-placement or reputation degradation |

## Output Rule

Every output must include:

- metric thresholds
- go/no-go decision logic
- containment actions
- recovery checkpoints

## Testing Rule

Run tests from the `tests/` folder before production use.

