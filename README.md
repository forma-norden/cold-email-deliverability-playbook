# cold-email-deliverability-playbook

Operational deliverability playbook for B2B outbound teams running cold email at
scale. This package turns infrastructure, sending behavior, copy constraints, and
diagnostics into reproducible workflows.

## What's Inside

| File | What it does |
|------|-------------|
| `.claude/skills/deliverability-infrastructure-baseline.md` | Defines domain and authentication baseline before campaign launch. |
| `.claude/skills/deliverability-provider-strategy.md` | Selects and runs provider-specific strategy with mailbox mix and ramp policy. |
| `.claude/skills/deliverability-copy-campaign-structure.md` | Applies copy and campaign structure rules that reduce filter risk. |
| `.claude/skills/deliverability-monitoring-diagnostics.md` | Monitors core deliverability metrics and identifies likely failure causes. |
| `.claude/skills/deliverability-recovery-runbook.md` | Executes staged recovery when inbox placement degrades. |
| `tests/` | Prompt-based tests and validation checklists for all five skills. |

## Prerequisites

- [ ] Sending domains and inboxes configured
- [ ] Access to DNS and sender-authentication records
- [ ] Sequencer and mailbox provider access
- [ ] Reply, bounce, and complaint telemetry available
- [ ] Ownership model for deliverability incidents

## Installation

1. Clone the repo:
   ```bash
   git clone https://github.com/forma-norden/cold-email-deliverability-playbook.git
   ```
2. Copy `.claude/skills/` into your project:
   ```bash
   cp -r cold-email-deliverability-playbook/.claude/skills your-project/.claude/
   ```
3. Load the relevant skill before any campaign launch or incident response.

## Usage

```text
Read .claude/skills/deliverability-monitoring-diagnostics.md

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

GTM engineers, RevOps leads, VP Sales, and founders at B2B companies with 50 to 500 employees who are building or consolidating their
outbound infrastructure and want to reduce tool sprawl through
better-engineered GTM systems.

---

---

## From the Forma Nôrden GTM Library

This is a free resource from the Forma Nôrden open-source GTM library, built by 
[Yananai A. Chiwuta](https://yananaichiwuta.com/), GTM engineer and founder of 
[Forma Nôrden](https://formanorden.com/).

- [Open-source GTM systems](https://github.com/forma-norden): all repos in the library  
- [GTM engineering blog](https://formanorden.com/blog/): strategy, systems, and outbound deep-dives  
- [All resources](https://formanorden.com/resources/): guides, frameworks, and templates  

If this saves you time, star the repo and follow 
[Forma Nôrden on LinkedIn](https://www.linkedin.com/company/formanorden/).

Built by [Forma Nôrden](https://formanorden.com/): GTM engineering for B2B companies.