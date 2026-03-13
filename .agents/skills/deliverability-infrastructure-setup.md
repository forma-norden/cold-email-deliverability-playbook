# deliverability-infrastructure-setup

Use this skill to configure email infrastructure from scratch for
cold outbound campaigns.

## Setup Sequence

### 1. Domain Strategy
Never use your primary domain (e.g., `company.com`) for cold outreach.
Purchase 3-5 secondary domains (`trycompany.com`, `companyapp.com`).
Forward all secondary domains to your primary domain using 301 redirects.

### 2. Workspace Provisioning
Google Workspace is the gold standard for B2B deliverability.
Microsoft 365 is acceptable but limits daily volume sooner.
Create 2-3 mailboxes per secondary domain (e.g., `first@`, `first.last@`).

### 3. DNS Authentication (The Big 3)

#### SPF (Sender Policy Framework)
Authorizes the mail server to send on behalf of the domain.
Value for Google: `v=spf1 include:_spf.google.com ~all`

#### DKIM (DomainKeys Identified Mail)
Cryptographic signature ensuring the email wasn't tampered with.
Generate the key in Google Admin, add the TXT record to DNS.

#### DMARC (Domain-based Message Authentication)
Tells receiving servers what to do if SPF or DKIM fails.
Value for new domains: `v=DMARC1; p=none; rua=mailto:dmarc@yourprimary.com;`
(Upgrade `p=none` to `p=quarantine` after 60 days of good sending.)

### 4. Technical Configuration
- Set up a custom tracking domain in your sending tool (Smartlead/Instantly).
- Add a CNAME record pointing to the tracking provider.
- Disable open and click tracking during the first 30 days of sending.

### 5. Warmup Protocol
Connect inboxes to a warmup pool immediately.
Ramp up target: 2-3 emails/day, increasing by 2/day until reaching 30/day.
Maintain warmup for 3-4 weeks before sending the first cold email.
Leave warmup running at 20-30% volume while sending campaigns.

## Benchmark Limits

- **Max daily sends per inbox:** 30-40 (including warmup)
- **Time between individual sends:** 8-15 minutes
- **Total daily volume per domain:** 100-120 max
- **Minimum warmup duration:** 21 days (ideally 30)

## Execution Checklist

1. List the domains to purchase.
2. Outline the mailbox naming convention.
3. Provide step-by-step DNS records needed.
4. Define the warmup schedule.

## Output Contract

Return:

- Domain purchasing strategy
- Specific TXT/CNAME records for SPF, DKIM, DMARC, and Custom Tracking
- Mailbox configuration plan
- 30-day warmup ramp schedule
- Pre-launch testing checklist (e.g., mail-tester.com, GlockApps)

## Anti-Patterns

- Sending cold emails from `name@primarydomain.com`
- Starting campaigns on day 1 without warmup
- Sending 100+ emails from a single inbox
- Missing DMARC records (causes instant blocks at Google/Yahoo)
- Using the same IP for cold outreach and transactional emails
