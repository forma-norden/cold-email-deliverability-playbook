# Deliverability Benchmarks

Performance data for email infrastructure and inbox placement.
Use these to set alarms, diagnose issues, and validate setups.

## Inbox Placement

| Metric | Healthy | Warning | Critical |
|--------|---------|---------|----------|
| Primary Inbox | > 85% | 70-85% | < 70% |
| Promotions Tab | < 10% | 10-20% | > 20% |
| Spam Folder | < 5% | 5-15% | > 15% |

## Volume Limits

| Metric | Safe Limit | Aggressive | High Risk |
|--------|------------|------------|-----------|
| Cold sends per inbox / day | 30 | 40-50 | > 50 |
| Total sends (inc. warmup) | 40-50 | 60-70 | > 80 |
| Inboxes per secondary domain| 2-3 | 4-5 | > 5 |
| Total sends per domain / day| 100 | 150-200 | > 200 |

## Campaign Health

| Metric | Healthy | Warning | Critical |
|--------|---------|---------|----------|
| Open rate (if tracked) | > 50% | 30-50% | < 30% |
| Reply rate (overall) | 4-8% | 1-3% | < 1% |
| Bounce rate | < 1% | 1-3% | > 3% |
| Spam complaint rate | < 0.05% | 0.05-0.1% | > 0.1% |

## Warmup Ramp

| Week | Warmup Target/Day | Cold Sends | Behavior |
|------|-------------------|------------|----------|
| 1 | 5 -> 15 | 0 | Build initial reputation |
| 2 | 15 -> 25 | 0 | Stabilize volume |
| 3 | 25 -> 35 | 0 | Reach sending capacity |
| 4 | 30 | 5 -> 15 | Slow transition to outreach |
| 5+ | 15-20 | 25-30 | Maintain steady state |

## Infrastructure Health Checks

| Frequency | Check | Method |
|-----------|-------|--------|
| Daily | Bounce rate | Sequencer analytics |
| Weekly | Blacklist check | MxToolbox / GlockApps |
| Weekly | Reply rate variance | Sequencer analytics |
| Monthly | DNS validation | mail-tester.com |
| Quarterly | Deliverability audit | GlockApps full scan |
