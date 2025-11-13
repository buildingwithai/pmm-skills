# Enterprise vs SMB Pricing

Design pricing strategies for different market segments.

## Overview

**SMB (Small-Medium Business):** <500 employees, self-serve buying
**Mid-Market:** 500-5,000 employees, hybrid buying (self-serve + sales)
**Enterprise:** 5,000+ employees, sales-led buying

**Different segments need different pricing:**
- Pricing model
- Sales motion
- Contract structure
- Discounting policies

## Key Differences

| Dimension | SMB | Mid-Market | Enterprise |
|-----------|-----|------------|------------|
| **ACV** | $500-$5K | $5K-$50K | $50K-$500K+ |
| **Sales cycle** | Hours-days | Days-weeks | Weeks-months |
| **Buying motion** | Self-serve | Hybrid | Sales-led |
| **Decision maker** | Individual/manager | Director/VP | C-suite/committee |
| **Price sensitivity** | High | Medium | Low |
| **Contract** | Monthly CC | Annual CC/invoice | Multi-year, invoice |
| **Discounting** | 0-10% | 10-20% | 20-40% |
| **Support** | Self-serve/email | Email/chat | Phone/CSM |
| **Security needs** | Low | Medium | High (SSO, SAML, SOC 2) |

---

## SMB Pricing Strategy

### Pricing Model

**Best: Simple, transparent, self-serve**

**Model 1: Flat-rate**
- $49/month or $99/month
- All features, simple
- Example: Basecamp ($99/month unlimited)

**Model 2: 2-3 tiers (Good/Better/Best)**
- Starter: $49/month
- Professional: $99/month
- Business: $199/month

**Model 3: Per-seat (small teams)**
- $10-20/user/month
- Example: Notion ($10/user/month)

**Avoid:**
- Complex usage-based (SMB wants predictability)
- "Contact us" pricing (73% won't engage)
- Custom/enterprise tiers (not relevant)

---

### Sales Motion

**Self-serve only:**
- No sales calls (too expensive for low ACV)
- Pricing page → credit card → instant access
- CAC target: $100-500 (for $500-5K ACV)

**Support:**
- Self-serve (docs, community, videos)
- Email support (24-48 hour response)
- No CSM

---

### Contract Structure

**Monthly or annual prepay**
- Monthly: $99/month, cancel anytime
- Annual: $990/year (2 months free = 16% discount)

**Payment:**
- Credit card only (Stripe, Chargebee)
- Auto-renewal
- Self-serve upgrade/downgrade

**No:**
- Multi-year contracts (SMB won't commit)
- Invoicing (too much overhead)
- Custom terms

---

### Discounting

**Limited discounting:**
- Annual discount: 16-20% (standard)
- Non-profit/education: 20-30% (automated, proof required)
- Startup programs: 50% off Year 1 (if qualified)

**No custom discounts:**
- SMB expects published pricing
- Discounting trains customers to negotiate

---

### Pricing Page

**Transparent:**
- Show all prices publicly
- Simple comparison table (5-8 features)
- Clear CTAs ("Start Free Trial", "Buy Now")

See `core/08-pricing-page-design.md`.

---

## Mid-Market Pricing Strategy

### Pricing Model

**Best: Tiered + volume discounts**

**Model: 3-4 tiers with seat-based pricing**
- Professional: $20/user/month (10-49 users)
- Business: $30/user/month (50-199 users)
- Enterprise: $40/user/month (200+ users)

**Volume tiers:**
- 10-49 users: $30/user
- 50-199: $25/user (17% discount)
- 200+: $20/user (33% discount)

**Rationale:** Incentivize growth, reward larger teams

---

### Sales Motion

**Hybrid:**
- Low-touch: $5-20K ACV → self-serve + sales email/call
- High-touch: $20-50K ACV → sales call required

**Process:**
1. Self-serve trial (14-30 days)
2. Sales outreach on day 3-7
3. Demo/discovery call
4. Proposal/quote
5. Close

**CAC target:** $1K-5K (for $5-50K ACV)

---

### Contract Structure

**Annual preferred, monthly available**
- Monthly: Higher price ($30/user/month)
- Annual: Discounted ($25/user/month = 17% off)

**Payment:**
- Credit card (annual, $5-20K)
- Invoice (annual, $20K+)

**Multi-year (optional):**
- 2-year: +10% discount (vs annual)
- 3-year: +15% discount

---

### Discounting

**10-20% standard**
- Annual: 10-17% (vs monthly)
- Multi-year: +5% (on top of annual)
- Volume: 10-30% (based on user count)

**Negotiable:**
- Mid-market expects some negotiation
- Sales can discount up to 20% without approval
- 20-30% requires VP approval

---

### Pricing Page

**Partially transparent:**
- Show tier pricing (Professional, Business)
- "Contact Sales" for Enterprise (custom quote)
- Volume discounts available (mention, don't show exact tiers)

---

## Enterprise Pricing Strategy

### Pricing Model

**Best: Custom, value-based, negotiated**

**Model: "Contact Us" + negotiated pricing**

**Starting point:**
- Base tier: $50K-100K/year (200-500 users)
- Custom tier: $100K-500K+/year (500+ users)

**Factors:**
- User count (seats or site license)
- Feature add-ons (SSO, advanced analytics, API access)
- Support tier (phone, CSM, SLA)
- Contract length (1-year, 3-year)
- Volume (more users = lower per-user price)

**Outcome:** Every enterprise deal is custom

---

### Sales Motion

**Sales-led:**
1. Inbound demo request or outbound prospecting
2. Discovery call (understand needs, budget, timeline)
3. Technical demo (2-3 rounds)
4. Proof of concept / pilot (30-90 days)
5. Security review (InfoSec, legal, procurement)
6. Pricing proposal (custom quote)
7. Negotiation (2-6 rounds)
8. Contract review (legal)
9. Signature
10. Implementation (30-90 days)

**Sales cycle:** 3-12 months (average 6 months)

**CAC target:** $10K-50K+ (for $50-500K ACV)

---

### Contract Structure

**Multi-year preferred:**
- 1-year: Standard
- 3-year: +15% discount, price lock
- 5-year: +25% discount (rare)

**Payment:**
- Annual invoice (net 30)
- Quarterly (if requested, no discount)
- Multi-year upfront (rare, +5% discount)

**Terms:**
- Auto-renewal (with price escalation clause: +5-10%/year)
- Termination: 60-90 days notice
- Custom SLAs (99.9% uptime, etc.)

---

### Discounting

**20-40% standard**
- List price: $100K
- Discounted price: $60-80K (typical close)

**Discount factors:**
- Multi-year: +10-15%
- Large volume: +10-20%
- Strategic account: +5-10%
- Competitive displacement: +10% (to win vs competitor)

**Approval:**
- <20%: AE can approve
- 20-30%: Sales manager
- 30-40%: VP Sales
- >40%: CEO (rare, strategic)

---

### Pricing Page

**"Contact Us" only:**
- No public pricing
- Form: Name, email, company, employees, use case
- Qualification: Sales reaches out within 24 hours

**Why:**
- Pricing too complex (custom per deal)
- High-touch sales required
- Want to control message (no sticker shock)

**Con:** Some buyers won't engage (want price transparency)

---

## Packaging Differences

### SMB Tier

**Features:**
- ✅ Core features (all basics)
- ❌ Advanced features (analytics, integrations)
- ❌ Support (self-serve only)
- ❌ Security (no SSO, SAML)

**Example:**
- 5-10 users
- Basic reporting
- Email support
- No SLA

---

### Mid-Market Tier

**Features:**
- ✅ Core + advanced features
- ✅ Priority support (email/chat)
- ⚠️ Some security (2FA, audit logs)
- ⚠️ Some integrations

**Example:**
- 50-200 users
- Advanced reporting
- Priority support (4-hour response)
- 99.5% uptime

---

### Enterprise Tier

**Features:**
- ✅ All features
- ✅ White-glove support (CSM, phone, Slack)
- ✅ Security/compliance (SSO, SAML, SOC 2, HIPAA)
- ✅ Custom integrations
- ✅ SLA (99.9% uptime)
- ✅ Dedicated infrastructure (optional)

**Example:**
- Unlimited users (or site license)
- Custom reporting
- Dedicated CSM
- 99.99% uptime SLA
- Custom integrations

---

## Good/Better/Best Across Segments

### Example: Notion

| Tier | SMB | Mid-Market | Enterprise |
|------|-----|------------|------------|
| **Name** | Plus | Business | Enterprise |
| **Price** | $10/user/mo | $18/user/mo | Custom |
| **Min users** | 1 | 10+ | 100+ |
| **Features** | Core workspace, 5GB/user | Advanced permissions, SAML | Unlimited pages, advanced security |
| **Support** | Email | Priority | CSM + phone |
| **Sales** | Self-serve | Self-serve + sales | Sales-led |

---

## When to Offer Enterprise Tier

**Triggers:**

✅ **You're getting enterprise inbound**
- Companies with >1,000 employees requesting demos

✅ **You have enterprise features**
- SSO/SAML, advanced security, compliance
- Custom integrations, SLAs

✅ **You have sales team**
- Can't close enterprise self-serve
- Need AEs, SEs, legal support

✅ **ACV justifies cost of sale**
- $50K+ ACV (can afford 6-month sales cycle)

---

**Don't offer enterprise tier if:**
❌ <$50K ACV (not worth cost of sale)
❌ No enterprise features yet (nothing to differentiate)
❌ No sales team (can't support sales cycle)

---

## Pricing Segmentation Tactics

### Tactic 1: Feature-Based Segmentation

**SMB:** Basic features only
**Mid-Market:** Advanced features (analytics, automation)
**Enterprise:** Custom + security features (SSO, audit logs)

**Example: HubSpot**
- Starter: Basic CRM
- Professional: Marketing automation, reporting
- Enterprise: Custom objects, predictive lead scoring

---

### Tactic 2: Volume-Based Segmentation

**SMB:** 1-10 users
**Mid-Market:** 11-200 users (volume discount)
**Enterprise:** 200+ users (custom pricing)

**Example: Slack**
- Free: Small teams (10K messages)
- Pro: $8/user (volume discounts at 50+)
- Enterprise Grid: Custom (10,000+ users)

---

### Tactic 3: Support-Based Segmentation

**SMB:** Self-serve, email (48-hour response)
**Mid-Market:** Priority support (4-hour response)
**Enterprise:** CSM, phone, Slack, 1-hour response SLA

---

### Tactic 4: Deployment-Based Segmentation

**SMB/Mid-Market:** Cloud-only (SaaS)
**Enterprise:** Cloud or on-prem/private cloud (custom)

**Example: GitLab**
- SaaS: Standard pricing
- Self-hosted: Enterprise pricing (custom)

---

## Pricing for Bottom-Up Enterprise (PLG)

**Model:** Start SMB (individual/small team), expand to enterprise

**Example: Figma**
1. **Individual designer:** Free tier (3 files)
2. **Design team (5-10):** Professional ($15/user/month) - self-serve
3. **Company (100+):** Organization ($45/user/month) - sales-assisted
4. **Enterprise (1,000+):** Enterprise ($75+/user/month) - sales-led, SSO, advanced security

**Expansion:**
- Free → Pro (individual upgrades)
- Pro → Organization (team admin buys for whole team)
- Organization → Enterprise (IT/security mandates SSO, centralized billing)

**Result:** 40% of Figma's enterprise customers started free (PLG motion)

---

## Key Takeaways

1. **SMB:** Self-serve, transparent pricing, $500-5K ACV
2. **Mid-Market:** Hybrid sales, partial transparency, $5-50K ACV
3. **Enterprise:** Sales-led, "Contact Us", $50K-500K+ ACV
4. **Discounting:** SMB 0-10%, Mid-Market 10-20%, Enterprise 20-40%
5. **Segmentation:** Features, volume, support, deployment
6. **PLG to Enterprise:** Start SMB, expand up-market (Figma, Slack, Notion)
7. **Enterprise needs:** SSO, SAML, CSM, SLA, custom integrations

## Next Steps

**Design tier structure for multiple segments:**
→ Read `core/06-packaging-tier-design.md`

**PLG to enterprise expansion:**
→ Read `advanced/product-led-growth-monetization.md`

**Enterprise negotiation:**
→ Read `core/10-internal-alignment-communication.md` (sales enablement)
