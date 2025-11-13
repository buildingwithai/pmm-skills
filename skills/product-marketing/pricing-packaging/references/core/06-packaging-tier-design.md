# Packaging & Tier Design

Design good/better/best tiers that drive conversion and expansion.

## Overview

**Packaging:** How you bundle features and pricing into tiers.

**Why it matters:**
- **60%+ of top SaaS use 3-tier model** (Simon-Kucher 2024)
- **Middle tier converts 60-70%** (anchor effect)
- **Clear upgrade path = expansion revenue**

**Key insight:** Packaging is often more important than the price itself. Price of $99 vs $149 matters less than which features are in each tier.

## The Good/Better/Best Framework

### Optimal Tier Count

**Research consensus:** 3 tiers is optimal.

| # of Tiers | Conversion | Why |
|-----------|------------|-----|
| **1 tier** | Low | No segmentation, one-size-fits-none |
| **2 tiers** | Medium | Limits choice, binary decision |
| **3 tiers** | **High** | **Sweet spot - choice without overwhelm** |
| **4 tiers** | Medium-High | Maximum before confusion |
| **5+ tiers** | Low | Analysis paralysis |

**Common 3-tier structures:**

**A) Free/Pro/Enterprise** (Freemium PLG)
- Free: Viral adoption, limited features
- Pro: Self-serve paid, core value
- Enterprise: Custom pricing, advanced features

**B) Starter/Professional/Business** (SMB-focused)
- Starter: Small teams, basic features
- Professional: Growing teams, advanced features  
- Business: Larger teams, premium features

**C) Pro/Business/Enterprise** (No free tier)
- Pro: Individual/small team
- Business: Teams/departments
- Enterprise: Whole company/custom

---

### Middle Tier is Anchor

**Pricing psychology:** Most customers choose middle tier (60-70%).

**Why:**
- **Goldilocks effect:** Not too cheap (quality concerns), not too expensive (budget)
- **Default choice:** When unsure, pick middle
- **Decoy effect:** Top tier makes middle look like better value

**Design implication:** Price your target tier as middle tier, anchor with premium tier above.

**Example: Notion Pricing (2024)**
- Plus: $10/user/month (middle tier) ← Target for teams
- Business: $15/user/month (premium anchor)
- Enterprise: Custom (super-premium, makes Business look reasonable)

---

## Feature Allocation Strategy

### Tier Differentiation Matrix

**Features by tier type:**

| Feature Type | Free/Starter | Pro/Mid | Business/Top | Enterprise |
|--------------|-------------|---------|--------------|-----------|
| **Core product** | ✓ Basic | ✓ Full | ✓ Full | ✓ Full |
| **Limits** | Strict | Moderate | High/Unlimited | Unlimited |
| **Integrations** | Few (0-5) | Standard (10-25) | Many (50+) | Unlimited |
| **Support** | Community/Email | Email | Priority/Phone | Dedicated CSM |
| **Analytics** | Basic | Standard | Advanced | Custom |
| **Admin/Security** | ✗ | Basic | Advanced | Full (SSO, SAML, audit logs) |
| **APIs** | ✗ or Limited | ✓ Standard | ✓ Advanced | ✓ Custom |
| **Customization** | ✗ | Limited | Moderate | Extensive |

---

### 5-8 Key Differentiators (Not 20)

**Common mistake:** Compare 20 features across tiers → paralysis

**Better:** Highlight 5-8 key differentiators only

**Example: Good (Notion)**
1. Collaboration (guests: 10 → Unlimited)
2. Version history (7 days → 90 days → Unlimited)
3. Admin tools (None → Basic → Advanced)
4. Support (Community → Priority)
5. Advanced features (AI, automations)

**vs Bad (Overwhelming):**
20-feature comparison table with checkmarks

---

### What to Gate

**Table stakes (in ALL tiers, even free):**
- Core product functionality
- Basic security (encryption)
- Email support (at least community)
- Mobile app access

**Gate in middle tier:**
- Advanced features (automations, AI)
- Higher usage limits
- Priority support
- Standard integrations
- Team collaboration features

**Gate in top tier:**
- Enterprise features (SSO, SAML)
- Unlimited usage
- Advanced admin controls
- Dedicated support
- Custom SLAs
- API access (sometimes)

**Gate in enterprise tier:**
- Custom integrations
- On-premise deployment
- Dedicated infrastructure
- White-glove onboarding
- Legal/compliance features

---

## Tier Naming Conventions

**Avoid generic names:**
❌ Basic, Standard, Premium, Enterprise
❌ Bronze, Silver, Gold, Platinum

**Use outcome-based names:**
✅ Starter, Pro, Business, Enterprise (functional)
✅ Individual, Team, Business, Enterprise (audience-based)
✅ Plus, Professional, Advanced, Enterprise (value-based)

**Examples from successful SaaS:**
- **Notion:** Free, Plus, Business, Enterprise
- **Slack:** Free, Pro, Business+, Enterprise Grid
- **HubSpot:** Starter, Professional, Enterprise
- **Airtable:** Free, Plus, Pro, Enterprise

---

## Pricing Tier Strategies

### Strategy 1: Linear Scaling

**Each tier = ~2-3x previous tier price**

Example:
- Starter: $49/month
- Pro: $149/month (3x)
- Business: $399/month (2.7x)
- Enterprise: Custom

**Pros:** Clear value scaling, predictable
**Cons:** May overprice or underprice specific segments

---

### Strategy 2: Compressed Pricing (SMB-friendly)

**Smaller gaps, more accessible tiers**

Example:
- Starter: $29/month
- Pro: $79/month (2.7x)
- Business: $149/month (1.9x)

**Pros:** Lower barrier to entry, easier upgrades
**Cons:** Less revenue per customer

**Use when:** SMB-focused, high volume strategy

---

### Strategy 3: Anchored Premium (Enterprise focus)

**Large gap between Business and Enterprise**

Example:
- Pro: $99/month
- Business: $299/month (3x)
- Enterprise: $2,999/month (10x) or Custom

**Pros:** Enterprise price anchors Business tier value
**Cons:** May scare mid-market

**Use when:** Targeting enterprise, premium positioning

---

## Usage Limits vs Feature Limits

### Usage Limits Strategy

**Gate on volume, not features:**

Example (Mailchimp):
- Free: 500 contacts, all features
- Essentials: 50,000 contacts
- Standard: 100,000 contacts
- Premium: Unlimited contacts

**Pros:**
- Simple to understand
- Customers try all features
- Natural upgrade (when they grow)

**Cons:**
- Doesn't differentiate on capabilities
- All customers get same features

---

### Feature Limits Strategy

**Gate on capabilities, generous usage:**

Example (Notion):
- Free: Unlimited pages, limited integrations
- Plus: Unlimited pages, unlimited integrations, version history
- Business: Everything in Plus + advanced permissions, analytics

**Pros:**
- Value differentiation clear
- Sells advanced capabilities
- Power users pay more

**Cons:**
- Can feel restrictive
- Hard to communicate value of gated features

---

### Hybrid (Best Practice)

**Combine usage + feature limits:**

Example (HubSpot):
- Starter: 1,000 contacts + basic features
- Professional: 2,000 contacts + advanced automation
- Enterprise: 10,000 contacts + custom reporting, permissions

**Pros:** Serves both small (usage) and power users (features)

---

## Pricing Psychology Tactics

### Tactic 1: Decoy Pricing

**Create "dominated" option to make target tier look better:**

Example:
- Pro: $99/month (10 users, basic features)
- **Business: $149/month (unlimited users, advanced features)** ← Target
- Business+: $139/month (unlimited users, no advanced features) ← Decoy

Business+ is dominated by Business (more money, fewer features), making Business look like best value.

**Result:** 70% choose Business (target tier)

See `core/07-pricing-psychology-tactics.md` for more.

---

### Tactic 2: Good/Better/Best Labels

**Mark one tier as "Most Popular" or "Best Value":**

Visual cues:
- Highlight middle tier with color/badge
- "Most Popular" label
- Slight visual elevation

**Result:** Drives 65-75% to highlighted tier

---

### Tactic 3: Enterprise "Contact Sales"

**Don't show Enterprise price:**
- Shows "Contact Sales" button
- Indicates custom pricing
- Makes Business tier look transparent and fair

**When to use:** Enterprise deals >$100K ARR, complex/variable pricing

---

## Tier Migration & Expansion

### Designing Upgrade Triggers

**In-product prompts:**
- Hit usage limit (90% of API calls used)
- Try to use gated feature (SSO button says "Upgrade to Enterprise")
- Team size exceeds plan (10 users on 5-user plan)

**Messaging:**
- "You've hit your limit of 5 projects. Upgrade to Pro for unlimited projects."
- "Advanced analytics is available on Business plan. Upgrade now."

---

### Expansion Revenue Opportunities

**1. Seat expansion** (per-user pricing):
- Start: 5 users on Pro ($500/month)
- Growth: 25 users on Pro ($2,500/month)
- Expansion: $2,000/month (+400%)

**2. Tier upgrade** (feature unlock):
- Start: Pro plan ($149/month)
- Upgrade: Business plan ($399/month)
- Expansion: $250/month (+167%)

**3. Usage overage** (hybrid pricing):
- Start: Pro plan ($199/month, 10K API calls)
- Overage: 50K API calls at $0.01 each = $400 overage
- Expansion: $400/month (+201%)

**Best: Combine all three** for maximum expansion potential.

---

## Freemium Tier Design

### What to Include in Free

**Generous enough to provide value:**
- Core product functionality (limited)
- Enough usage to get "aha moment"
- Ability to share/collaborate (viral)

**Example: Slack Free**
- Unlimited users
- 10,000 message history
- 10 integrations
- 1:1 calls

**Why it works:** Teams can actually use it, hit limits over time (messages), upgrade for unlimited history.

---

### What to Gate (Drive Upgrades)

**Gate features that:**
- ✅ Power users need (advanced automations, analytics)
- ✅ Teams need for security (SSO, advanced permissions)
- ✅ Become valuable over time (unlimited history, storage)

**Example: Calendly Free**
- 1 event type (strict limit)
- Upgrade for unlimited event types

**Result:** Solopreneurs use free, businesses upgrade immediately (need multiple event types).

See `advanced/freemium-free-trial-strategies.md` for conversion tactics.

---

## B2B Tier Segmentation

### SMB Tier (Self-Serve)

**Characteristics:**
- $50-$500/month price range
- Self-serve signup
- Credit card payment
- Email/chat support

**Example:**
- Starter: $99/month (5 users)
- Team: $299/month (20 users)

---

### Mid-Market Tier (Light Touch Sales)

**Characteristics:**
- $500-$5,000/month
- Self-serve or light sales assist
- Annual contracts preferred
- Phone support, CSM for larger accounts

**Example:**
- Business: $999/month (50 users)

---

### Enterprise Tier (Sales-Led)

**Characteristics:**
- $5,000+/month (often $50K+ annual)
- Sales-led (contact sales)
- Custom pricing, volume discounts
- Dedicated CSM, SLAs, custom terms

**Example:**
- Enterprise: Custom (100+ users, SSO, custom integrations)

See `advanced/enterprise-vs-smb-pricing.md` for detailed segmentation.

---

## Common Packaging Mistakes

### Mistake 1: Too Many Tiers (Decision Paralysis)

**Problem:** 6 tiers, customers can't decide
**Fix:** 3-4 tiers maximum

### Mistake 2: Unclear Differentiation

**Problem:** "Pro has more features than Starter" (which features?)
**Fix:** Highlight 5-8 specific differentiators

### Mistake 3: Pricing All Tiers Wrong

**Problem:** Test only middle tier pricing, assume ratios work
**Fix:** Test tier relationships (not just absolute prices)

### Mistake 4: Bottom Tier Cannibalizes Revenue

**Problem:** Too generous free/starter tier, no reason to upgrade
**Fix:** Gate valuable features, usage limits that scale users into paid

### Mistake 5: Enterprise "Contact Sales" for $100/Month Products

**Problem:** SMB customers won't call sales for small purchases
**Fix:** Show transparent pricing up to $10K ARR, then contact sales

---

## Packaging Review Checklist

- ☐ 3-4 tiers total (not 5+)
- ☐ Middle tier is target tier (expect 60-70% of customers)
- ☐ 5-8 key differentiators highlighted (not 20)
- ☐ Free tier provides value but gates premium features (if freemium)
- ☐ Clear upgrade triggers in-product
- ☐ Enterprise tier has "Contact Sales" (if complex/custom)
- ☐ Tier names are outcome/audience-based (not bronze/silver/gold)
- ☐ Features gated align to value (not arbitrary)
- ☐ Pricing scales 2-3x between tiers
- ☐ Usage limits AND feature limits combined

Use `assets/templates/pricing-tier-comparison-matrix.md` to design tiers.

---

## Key Takeaways

1. **3 tiers is optimal** - 60%+ of SaaS use Good/Better/Best
2. **Middle tier converts 60-70%** - Design as target tier
3. **5-8 differentiators only** - Not 20-feature matrix
4. **Gate features that drive value** - Advanced capabilities, enterprise needs
5. **Free tier should provide value** - But limits push to paid
6. **Combine usage + feature limits** - Serve small and power users
7. **Test tier relationships** - Not just absolute prices

## Next Steps

**Ready to design pricing page:**
→ Read `core/08-pricing-page-design.md`

**Ready to understand pricing psychology:**
→ Read `core/07-pricing-psychology-tactics.md`

**Need to design freemium tier:**
→ Read `advanced/freemium-free-trial-strategies.md`
