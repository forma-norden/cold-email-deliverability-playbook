# Ecosystem: cold-email-deliverability-playbook

How this repo connects to the rest of the Forma Norden GTM library.

## Works With

| Repo | Relationship | When to use together |
|------|-------------|---------------------|
| `cold-email-copy-playbook` | Parallel | Copy structure affects deliverability, run both before launch |
| `n8n-gtm-workflow-pack` | Downstream | n8n automates deliverability monitoring alerts |
| `clay-claude-code-skill-pack` | Upstream | Email verification in Clay connects to deliverability checks |

## Suggested Skill Chains

1. Pre-launch: `cold-email-copy-playbook` (write) > deliverability-copy-campaign-structure (check copy) > deliverability-monitoring-diagnostics (test placement)
2. Recovery: deliverability-monitoring-diagnostics (diagnose) > deliverability-recovery-runbook (fix) > deliverability-infrastructure-baseline (rebuild)
