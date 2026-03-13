# Cold Email Deliverability Playbook

Operational deliverability playbook for B2B outbound teams running cold email at
scale. This package turns infrastructure, sending behavior, copy constraints, and
diagnostics into reproducible workflows.

## What's Inside

| File | What it does |
|------|-------------|
| .agents/skills/SKILL.md | Orchestrator and routing logic |
| .agents/skills/deliverability-infrastructure-baseline.md | Defines domain and authentication baseline before campaign launch. |
| .agents/skills/deliverability-provider-strategy.md | Selects and runs provider-specific strategy with mailbox mix and ramp policy. |
| .agents/skills/deliverability-copy-campaign-structure.md | Applies copy and campaign structure rules that reduce filter risk. |
| .agents/skills/deliverability-monitoring-diagnostics.md | Monitors core deliverability metrics and identifies likely failure causes. |
| .agents/skills/deliverability-recovery-runbook.md | Executes staged recovery when inbox placement degrades. |
| .agents/skills/deliverability-infrastructure-setup.md | Technical guide for DMARC, DKIM, SPF, and custom tracking domains. |
| esources/benchmarks/deliverability-benchmarks.md | Bounce rate, spam complaint, and placement targets to monitor. |
| ECOSYSTEM.md | Cross-repo connectivity map |

## Prerequisites

- [ ] Sending domains and inboxes configured
- [ ] Access to DNS and sender-authentication records
- [ ] Sequencer and mailbox provider access
- [ ] Reply, bounce, and complaint telemetry available
- [ ] Ownership model for deliverability incidents

## Installation

### Cursor, Windsurf, or Generic AI IDE
1. Clone the repo: `git clone https://github.com/forma-norden/cold-email-deliverability-playbook`
2. Copy the `.agents/skills/` directory into your project's `.agents/skills/` folder.

### Claude Code
1. Clone the repo: `git clone https://github.com/forma-norden/cold-email-deliverability-playbook`
2. Copy the `.agents/skills/` directory into your project's `.claude/skills/` folder.

## Usage

```text
Read .agents/skills/deliverability-monitoring-diagnostics.md

Inputs:
- weekly reply trend: down 42%
- bounce rate: 3.4%
- complaint rate: 0.18%
- inbox placement checks: mostly spam
- recent changes: send volume doubled in 5 days

Return:
1) likely root causes ranked
2) immediate containment actions
3) 14-day stabilization plan
4) go/no-go criteria for scale-up
```

Expected output:

- structured diagnosis
- ranked root-cause hypotheses
- stepwise stabilization actions with thresholds

## Who This Is For

GTM engineers, RevOps leads, VP Sales, and founders at B2B companies with 50 to
500 employees who are building or consolidating their outbound infrastructure and
want to reduce tool sprawl through better-engineered GTM systems.

---

## From the Forma Nôrden GTM Library

This is a free resource from the Forma Nôrden open-source GTM library, built by
[Yananai A. Chiwuta](https://yananaichiwuta.com/), GTM engineer and founder of
[Forma Nôrden](https://formanorden.com/).

- [Open-source GTM systems](https://github.com/forma-norden) - all repos in the library  
- [GTM engineering blog](https://formanorden.com/blog/) - strategy, systems, and outbound deep-dives  
- [All resources](https://formanorden.com/resources/) - guides, frameworks, and templates  

If this saves you time, star the repo and follow
[Forma Nôrden on LinkedIn](https://www.linkedin.com/company/formanorden/).

Built by [Forma Nôrden](https://formanorden.com/) - GTM engineering for B2B companies.


