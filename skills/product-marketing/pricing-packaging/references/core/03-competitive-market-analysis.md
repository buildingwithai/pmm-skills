# Competitive & Market Pricing Analysis

Understand your competitive pricing landscape and market positioning. Use as context, not as your primary pricing strategy.

## Overview

**Purpose:** Competitive pricing analysis provides context for your pricing decisions—what alternatives cost, how you compare, where whitespace exists.

**⚠️ Warning:** Competitor-based pricing is a weak strategy (see `core/01-pricing-fundamentals-strategy.md`). Use this as **reference data**, not as your price-setting method.

**Why it matters:**
- Understand market expectations
- Identify positioning opportunities (premium, value, mid-market)
- Prepare sales for competitive objections
- Spot pricing trends and shifts

## Competitive Pricing Audit Framework

### Step 1: Identify Competitive Set

**Three categories of competitors:**

**1. Direct Competitors** (Same solution, same audience)
- Solve same problem with similar approach
- Target same customer segment
- **Example:** Salesforce vs HubSpot CRM (both CRMs for SMB-Enterprise)

**2. Indirect Competitors** (Different solution, same problem)
- Solve same problem with different approach
- May target adjacent segments
- **Example:** Notion vs Microsoft Word (both for document creation)

**3. Alternatives** (What customers do if they don't buy)
- Manual processes
- Adjacent tools repurposed
- Internal builds
- **Example:** Excel as CRM (vs Salesforce)

**Audit checklist:**
- ☐ List 5-10 direct competitors
- ☐ List 3-5 indirect competitors
- ☐ Identify manual/DIY alternatives
- ☐ Segment by customer size (enterprise vs SMB tools)

---

### Step 2: Gather Pricing Data

**Public pricing pages** (easiest)
- Screenshot pricing pages (archive.org for history)
- Document tier names, features, prices
- Note annual vs monthly pricing
- Capture value proposition messaging

**Private/contact sales pricing** (harder)
- Submit RFP as anonymous company
- Network with customers (ask what they pay)
- LinkedIn/Reddit posts (people share prices)
- Gartner Peer Insights (user reviews mention pricing)

**Tools for tracking:**
- Price2Spy ($50-$200/month, automated monitoring)
- Competera (enterprise pricing intelligence)
- Manual: Excel/Google Sheets + monthly check
- Wayback Machine (archive.org) for historical pricing

**Use template:** `assets/templates/competitive-pricing-audit-template.md`

---

### Step 3: Analyze Pricing Models

| Competitor | Model | Base Price | Value Metric | Annual Discount | Target Segment |
|------------|-------|------------|--------------|-----------------|----------------|
| Competitor A | Tiered | $99/month | Per-user | 16% (2 mo free) | SMB |
| Competitor B | Usage-based | $0.10/API call | Consumption | N/A | Developer |
| Competitor C | Enterprise only | Contact sales | Unknown | Unknown | Enterprise |
| Your Product | **TBD** | **TBD** | **TBD** | **TBD** | **TBD** |

**What to look for:**
- **Model prevalence:** Are most using tiered? Usage-based? Freemium?
- **Value metric:** Per-user, per-contact, per-GB, per-outcome?
- **Tier structure:** 3-tier (Good/Better/Best), 4-tier, 2-tier?
- **Discount patterns:** Annual discounts 15-20%, enterprise volume discounts?

**2024 trends:**
- 56% have some consumption-based element (up from 25% in 2021)
- 42% offer freemium (PLG influence)
- 65% use tiered subscription (still dominant)
- 28% raised prices in 2024 (inflation, value increase)

---

### Step 4: Feature Comparison Matrix

Map features across tiers to understand packaging strategies:

```
Feature Allocation Matrix:

                    Starter    Pro       Business   Enterprise
Competitor A:
- Core feature      ✓          ✓         ✓          ✓
- Analytics         Basic      Advanced  Advanced   Custom
- Integrations      5          25        Unlimited  Unlimited
- Support           Email      Email     Phone      Dedicated CSM
- Users             5          25        Unlimited  Unlimited

Competitor B:
- Core feature      ✓          ✓         ✓          ✓
- Analytics         ✗          ✓         ✓          ✓
- Integrations      ✗          10        50         Unlimited
- Support           Community  Email     Priority   Dedicated
- Users             Unlimited  Unlimited Unlimited  Unlimited

Your Product:
- Core feature      ?          ?         ?          ?
- Analytics         ?          ?         ?          ?
[Fill in your strategy]
```

**Insights to extract:**
- What features are table stakes (in all tiers)?
- What features differentiate premium tiers?
- How do they gate value (users, features, support)?
- Gaps/opportunities (features no one offers)?

---

### Step 5: Price Positioning Map

Plot competitors on price vs value axes:

```
Price (High)
     │
     │  Premium Zone          Enterprise Zone
     │  [Competitor C]        [Competitor D: Contact Sales]
     │
     │  Mid-Market             Value Leader?
     │  [Competitor A]         [Opportunity?]
     │
     │  Economy/Freemium
     │  [Competitor B]
     │
     └─────────────────────────────────────────> Value (High)
          (Low)
```

**Positioning decisions:**
- **Premium:** Higher price, superior capabilities (10-30% price premium)
- **Parity:** Match market, compete on differentiation
- **Value:** Lower price, sufficient features (10-20% below market)
- **Freemium:** Free tier + paid upgrade (PLG)

**Example: Calendly's positioning evolution (2020-2024)**
- 2020: Value player ($8/user/month, cheaper than Chili Piper)
- 2022: Mid-market ($10/user/month, added enterprise tier)
- 2024: Premium ($16/user/month, feature expansion)

---

## International Pricing Variations

**Geography = massive WTP differences (2024 Paddle/Simon-Kucher data):**

### Willingness to Pay by Region

| Region | WTP vs US | Purchasing Power Parity | Recommended Localization |
|--------|-----------|------------------------|-------------------------|
| **Nordic Countries** | **+20-30%** | High income, high willingness | Premium pricing OK |
| **United Kingdom** | **+98%** | Similar to US, higher for software | Charge more |
| **Denmark** | **+151%** | Highest WTP globally | Significantly higher |
| **Germany/Western EU** | +10-20% | High income, price-sensitive culture | Slight premium |
| **Eastern Europe** | -20-30% | Lower purchasing power | Discount |
| **Southeast Asia** | **-40%** | Rapidly growing but price-sensitive | Significant discount |
| **India** | **-60%** | Large market but low WTP | Deep discount or PPP |
| **Latin America** | -30-40% | Varies by country | Mexico > Brazil > Argentina |

**Key insight:** Nordics are willing to pay 2.5x what India pays for same product.

**Strategy implications:**
- **Geographic pricing:** Adjust by region (50% of companies don't—missed opportunity)
- **Local currency:** Display in EUR, GBP, etc. (increases conversion 15-20%)
- **Payment methods:** Alipay in China, SEPA in EU, UPI in India
- **Purchasing power parity:** India gets 60% discount but still profitable (volume)

See `advanced/international-localized-pricing.md` for implementation.

---

## Enterprise vs SMB Pricing Differences

**Same product, different pricing for different segments:**

### SMB Pricing Characteristics

**Pricing transparency:**
- ✅ Public pricing (73% won't engage without)
- ✅ Self-serve signup
- ✅ No contact sales required

**Pricing model:**
- Monthly billing preferred (60% vs 40% annual)
- Standard annual discount: 16-20% (effectively 2 months free)
- No negotiation (posted price is final)

**Tier structure:**
- 2-3 tiers (Starter, Pro, Business)
- Feature-gated (not usage-gated)
- Clear upgrade path

**Example: HubSpot SMB**
- Starter: $45/month (2 users)
- Professional: $800/month (5 users)
- Enterprise: Contact sales (100+ users)

---

### Enterprise Pricing Characteristics

**Pricing transparency:**
- ⚠️ "Contact sales" common (but 42% still want some transparency)
- Custom pricing based on volume, deployment, support

**Pricing model:**
- Annual contracts preferred (80%+ annual)
- Multi-year commitments common
- Negotiation expected (bake in 20% discount margin)

**Tier structure:**
- Often custom tiers
- Usage-based + base fee (hybrid)
- Volume discounts (>100 users get 20-40% off)

**Example: Salesforce Enterprise**
- List price: $325/user/month
- Negotiated: $195-$260/user/month (20-40% discount)
- Multi-year: Additional 10-15% off
- Volume discount: >500 users get 30%+ off

**Key difference:** SMB = transparent, standard pricing. Enterprise = custom, negotiated.

See `advanced/enterprise-vs-smb-pricing.md` for detailed strategies.

---

## Competitor Pricing Monitoring Cadence

**How often to check:**

| Activity | Frequency | Why |
|----------|-----------|-----|
| **Screenshots of pricing pages** | Quarterly | Track changes, archive history |
| **Feature comparison update** | Bi-annually | New features, tier changes |
| **Customer interviews (what they pay)** | Ongoing | Real prices vs listed |
| **Competitive win/loss analysis** | Monthly | Why customers choose alternatives |
| **Market pricing report** | Annually | Comprehensive landscape review |

**Alert triggers:**
- ☐ Competitor raises prices >10%
- ☐ Competitor launches new tier/model
- ☐ New competitor enters market
- ☐ Competitor acquired (pricing often changes)
- ☐ Major feature parity shift

---

## Using Competitive Data (Without Becoming Competitor-Based)

### ✅ Good Uses of Competitive Pricing Data

**1. Validate pricing range**
- Your WTP research says $150/month is optimal
- Competitor range is $100-$200/month
- ✅ Validates you're in the ballpark

**2. Prepare sales objections**
- "Competitor X is cheaper"
- Response: "Yes, they're $30 less, but we include [differentiated value] which saves you $300/month"

**3. Identify positioning opportunities**
- All competitors charge per-user
- ✅ Opportunity: Charge per-outcome instead (differentiation)

**4. Understand market maturity**
- Mature market: Prices converge around $100-$150
- Emerging market: Prices range $50-$500 (still experimenting)

**5. Spot pricing trends**
- 3 competitors raised prices 15% in last 6 months
- ✅ Signal: Market can bear higher prices

---

### ❌ Bad Uses of Competitive Pricing Data

**1. Matching competitor prices**
- "Competitor charges $99, so we'll charge $99"
- ❌ Ignores your differentiated value, leads to commoditization

**2. Undercutting on price alone**
- "We'll be 10% cheaper than everyone"
- ❌ Race to the bottom, attracts price-sensitive customers

**3. Assuming competitors priced correctly**
- "Industry leader charges $X, so that must be right"
- ❌ They may have priced poorly, be legacy pricing, or have different costs

**4. Pricing to competitor features**
- "They have 10 features in Pro tier, we should too"
- ❌ Different customers value different features

**5. Changing prices reactively**
- "Competitor dropped prices, we must too!"
- ❌ Knee-jerk reactions without understanding why

---

## Competitive Pricing Intelligence Checklist

Use `assets/templates/competitive-pricing-audit-template.md` to collect:

### Competitor Profile
- ☐ Company name, founding year, funding
- ☐ Target customer segment (SMB, mid-market, enterprise)
- ☐ Go-to-market motion (PLG, sales-led, hybrid)

### Pricing Model
- ☐ Model type (subscription, usage, freemium, hybrid)
- ☐ Value metric (per-user, per-GB, per-API-call, per-outcome)
- ☐ Billing frequency (monthly, annual, multi-year)

### Tier Structure
- ☐ Tier names (Free, Starter, Pro, Business, Enterprise)
- ☐ Price per tier (monthly, annual)
- ☐ Annual discount percentage
- ☐ Features per tier (10-15 key features)
- ☐ Limits per tier (users, storage, API calls)

### Packaging Strategy
- ☐ What's free (if freemium)
- ☐ What gates upgrades (users, features, usage)
- ☐ Enterprise features (SSO, SAML, dedicated support)

### Market Positioning
- ☐ Value proposition (how they describe themselves)
- ☐ Differentiation claim (what makes them unique)
- ☐ Competitive comparison (how they position vs others)

### Changes Over Time
- ☐ Price changes (when, how much)
- ☐ Model changes (subscription → usage, etc.)
- ☐ Tier changes (added/removed tiers)

---

## Red Flags in Competitive Pricing

Watch for these signs that competitors may have priced incorrectly:

**1. Extreme Price Dispersion**
- Competitors range from $50 to $500 for similar value
- ✅ Indicates market still figuring out pricing (test higher end)

**2. Frequent Price Changes**
- Competitor changes prices quarterly
- ✅ Indicates they're struggling to find right price (they don't know either)

**3. Complex Pricing (10+ Tiers)**
- Competitor has 7 tiers with 20 feature dimensions
- ✅ Indicates confusion, opportunity for simplicity

**4. "Contact Sales" for SMB**
- Competitor requires sales call for $100/month product
- ✅ Indicates conversion problems (be transparent instead)

**5. No Price Changes in 5+ Years**
- Competitor hasn't raised prices since 2019
- ✅ Indicates complacency (they're leaving money on table)

---

## Competitive Positioning Strategies

### Strategy 1: Premium Positioning (10-30% Above Market)

**When it works:**
- Superior product capabilities
- Better support/service
- Stronger brand/trust
- Lower risk for buyers

**Example:** Salesforce vs SugarCRM
- Salesforce: $325/user/month (enterprise)
- SugarCRM: $85/user/month
- 3.8x premium justified by: ecosystem, reliability, enterprise features

**Messaging:** "We cost more because we deliver more [specific value]"

---

### Strategy 2: Parity Positioning (Match Market)

**When it works:**
- Similar capabilities to market
- Competing on differentiated features (not price)
- Established market with clear price expectations

**Example:** Asana vs Monday.com
- Asana: $10.99/user/month (Pro)
- Monday.com: $12/user/month (Standard)
- Similar pricing, compete on UX and workflow philosophy

**Messaging:** "Similar price, better [differentiated feature]"

---

### Strategy 3: Value Positioning (10-20% Below Market)

**When it works:**
- Sufficient features for target segment
- Lower cost structure (cloud-native, efficient)
- Fast follower, not market leader

**Example:** Zoom vs WebEx (2019)
- Zoom: $14.99/host/month
- WebEx: $24.95/host/month
- 40% cheaper, better UX, modern

**Messaging:** "Same quality, better price" (but must back it up)

---

### Strategy 4: Freemium/PLG Positioning

**When it works:**
- Viral product, low marginal cost
- Product-led growth motion
- Conversion from free → paid at 2-5%

**Example:** Slack vs Microsoft Teams
- Slack: Free + $7.25/user/month (Pro)
- Teams: Included with Office 365
- Freemium drove adoption, enterprise paid for advanced features

**Messaging:** "Try free, upgrade when you need [advanced features]"

---

## When to Ignore Competitors' Pricing

**Situations where competitive pricing is irrelevant:**

1. **You have unique value no competitor offers**
   - Example: Only product with real-time collaboration in your category
   - → Price to your unique value, not competitors

2. **You target different segment than competitors**
   - Example: They target SMB ($50/month), you target enterprise ($500/month)
   - → Different WTP, different pricing

3. **You have different cost structure**
   - Example: You're API-first (efficient), they're legacy (expensive)
   - → You can profitably undercut or reinvest in features

4. **Competitors are priced poorly**
   - Example: Competitor underpriced, losing money, will raise or shut down
   - → Don't follow them down

5. **You're creating new category**
   - Example: First AI-native product in space
   - → No comparable pricing, price to value created

---

## Key Takeaways

1. **Use competitive pricing as context, not as strategy** - Value-based > competitor-based
2. **Geography matters hugely** - Nordics +20-30%, SE Asia -40%, India -60%
3. **Enterprise vs SMB pricing differs** - SMB = transparent, enterprise = custom/negotiated
4. **Track quarterly, don't react to every change** - Understand why before matching
5. **Look for positioning opportunities** - Premium, parity, value, or freemium
6. **Watch for competitor red flags** - Frequent changes, complexity, staleness
7. **Ignore competitors when you have unique value** - Price to your differentiation

## Next Steps

**Gathered competitive data, ready to design pricing:**
→ Read `core/04-choosing-pricing-model.md` (subscription vs usage vs freemium)

**Need to understand WTP first:**
→ Read `core/02-willingness-to-pay-research.md`

**Ready to design tiers:**
→ Read `core/06-packaging-tier-design.md`
