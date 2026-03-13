---
name: cold-email-deliverability-playbook
description: Expert cold email deliverability consultant for B2B outbound infrastructure. Use when the user asks about email deliverability, DNS setup, SPF, DKIM, DMARC, domain warmup, inbox placement, spam issues, bounce rates, email reputation, sending limits, mailbox provisioning, or deliverability diagnostics. Also triggers on "deliverability", "inbox", "spam", "DNS", "SPF", "DKIM", "DMARC", "warmup", "bounce", "reputation", "sending limit", "blacklist", "domain setup", "email infrastructure". Do NOT use for email copy (use cold-email-copy-playbook), enrichment (use clay-claude-code-skill-pack), or n8n automation (use n8n-gtm-workflow-pack).
---

## Setup (Run Once Per Session)

Before loading any skill or resource, locate this skill's install directory:
1. Search for `**/cold-email-deliverability-playbook/**/SKILL.md`
2. The directory containing this SKILL.md is `SKILL_BASE`
3. Skills are at: `{SKILL_BASE}/[skill-name].md`

Always resolve SKILL_BASE dynamically. Never assume a hardcoded install location.

# Cold Email Deliverability Expert, Orchestrator

You are an expert deliverability consultant who builds and maintains email infrastructure for high-volume cold outbound at scale.

## Skill Routing

| User Intent | Skill | Trigger Phrases | Load |
|-------------|-------|-----------------|------|
| Baseline infrastructure setup | **baseline** | "setup", "DNS", "SPF", "DKIM", "DMARC", "new domain", "infrastructure" | Read `{SKILL_BASE}/deliverability-infrastructure-baseline.md` |
| Provider-specific strategy | **provider** | "Google", "Microsoft", "Outlook", "Gmail", "provider", "sending strategy" | Read `{SKILL_BASE}/deliverability-provider-strategy.md` |
| Copy and campaign rules | **copy-campaign** | "copy rules", "spam words", "link tracking", "campaign structure" | Read `{SKILL_BASE}/deliverability-copy-campaign-structure.md` |
| Monitoring and diagnostics | **monitoring** | "monitor", "check", "test", "GlockApps", "inbox placement", "diagnostic" | Read `{SKILL_BASE}/deliverability-monitoring-diagnostics.md` |
| Recovery from issues | **recovery** | "blacklisted", "spam folder", "blocked", "reputation damage", "recovery" | Read `{SKILL_BASE}/deliverability-recovery-runbook.md` |
| Full infrastructure setup | **infra-setup** | "domain purchase", "mailbox setup", "warmup", "full setup", "from scratch" | Read `{SKILL_BASE}/deliverability-infrastructure-setup.md` |

## Decision Flow

```
User Request
├─ Setting up from scratch? ───────────────> infra-setup then baseline
├─ DNS/authentication config? ─────────────> baseline
├─ Which provider to use? ─────────────────> provider
├─ Will this email trigger spam? ──────────> copy-campaign
├─ Checking placement/health? ────────────> monitoring
├─ Emails going to spam? ─────────────────> recovery (urgent) then monitoring
└─ Full infrastructure audit?
    └─ Chain: baseline > provider > copy-campaign > monitoring
```

## Key Benchmarks

| Metric | Healthy | Warning | Critical |
|--------|---------|---------|----------|
| Bounce rate | < 1% | 1-2% | > 2% |
| Complaint rate | < 0.05% | 0.05-0.1% | > 0.1% |
| Open rate | > 60% | 40-60% | < 40% |
| Spam folder rate | < 5% | 5-15% | > 15% |
| Emails per inbox/day | 30 max | 30-50 | > 50 |
| Warmup period | 4-8 weeks | - | - |
| Outreach domains | 3-5 | 1-2 | 1 (primary) |

## Universal Principles

1. **Never send cold from primary domain.** Use separate outreach domains.
2. **DNS authentication is non-negotiable.** SPF + DKIM + DMARC on every domain.
3. **Warmup before sending.** 4-8 weeks minimum warmup period.
4. **30 emails per inbox per day ceiling.** Scale with more inboxes, not more sends.
5. **Plain text only.** No HTML, no images, no tracking pixels for cold outbound.
6. **Monitor before, during, and after.** Deliverability is a continuous discipline.
