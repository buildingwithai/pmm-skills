# Pricing Methodologies

Complete guide to pricing research and strategy methodologies.

## Research Methodologies

### Van Westendorp Price Sensitivity Meter (PSM)

**What it is:**
Survey method to determine acceptable price range

**How it works:**
Ask respondents 4 questions:
1. At what price is [Product] too expensive to consider?
2. At what price is [Product] so inexpensive you'd question quality?
3. At what price is [Product] starting to get expensive?
4. At what price is [Product] a bargain?

**Analysis:**
- Plot cumulative curves for each question
- Find intersections:
  - OPP (Optimal Price Point): "too expensive" × "great value"
  - IPP (Indifference Price Point): "getting expensive" × "great value"
  - Acceptable range: Between OPP and IPP

**Sample size:** 30-50 minimum, 200+ ideal

**When to use:**
- New product pricing
- Price change validation
- Market entry pricing

**Pros:**
- Simple, quick (10 minutes per respondent)
- Provides price range, not just single point
- Inexpensive (online survey)

**Cons:**
- Hypothetical (stated vs revealed preference)
- Doesn't account for features/packaging
- Cultural bias (some cultures always say "too expensive")

**Tools:** SurveyMonkey, Typeform, Qualtrics

**Example:**
- Too expensive: $200
- Getting expensive: $150
- Great value: $100
- Too cheap: $50
- OPP: $120 (intersection of $200 and $100 curves)

**Reference:** `core/02-willingness-to-pay-research.md`

---

### Conjoint Analysis

**What it is:**
Advanced research method to understand feature/price trade-offs

**How it works:**
- Show combinations of features + prices
- Ask: "Which would you choose?"
- Repeat with many combinations
- Calculate: Value weight of each feature

**Example combinations:**
- Option A: Feature X + Y, $99/month
- Option B: Feature X + Z, $149/month
- Option C: Feature Y + Z, $129/month

**Analysis:**
Statistical model (regression) determines:
- Value of Feature X: +$30
- Value of Feature Y: +$50
- Value of Feature Z: +$70

**Sample size:** 200-500 respondents

**When to use:**
- Complex products (many features)
- Packaging decisions (which features in which tier)
- Understanding feature value

**Pros:**
- Quantifies feature value
- Simulates real trade-off decisions
- Predicts demand at different price/feature combinations

**Cons:**
- Complex to design
- Expensive ($5K-$50K for agency)
- Requires statistical expertise
- Time-intensive (30-45 min per respondent)

**Tools:**
- Qualtrics Conjoint
- Sawtooth Software
- Agency: Simon-Kucher, PriceBeam

**Reference:** `core/02-willingness-to-pay-research.md`

---

### Customer Interviews (Qualitative)

**What it is:**
1-on-1 conversations to understand value, WTP, objections

**Structure:**
- 30-45 minutes per interview
- Semi-structured (script with flexibility)
- Mix: 50% customers, 50% prospects

**Key questions:**
- What problem does [Product] solve for you?
- If [Product] didn't exist, what would you use?
- What's the most valuable feature?
- What would you pay for [Product]? (WTP)
- What price would make you walk away?

**Sample size:** 20-30 interviews

**When to use:**
- Early-stage (no data yet)
- Understand "why" behind pricing decisions
- Validate quantitative findings

**Pros:**
- Deep insights ("why" not just "what")
- Flexibility (follow interesting threads)
- Builds relationships (customers feel heard)

**Cons:**
- Small sample (not statistically significant)
- Biased (stated vs actual behavior)
- Time-intensive (hours to conduct + synthesize)

**Best practices:**
- Record and transcribe (with permission)
- Ask "why" 3 times (get to root reason)
- Don't lead ("What do you think of $X?" vs "Would you pay $X?")

**Reference:** `templates/willingness-to-pay-research-script.md`

---

### Competitive Analysis

**What it is:**
Systematic audit of competitor pricing

**Process:**
1. Identify top 5 competitors
2. Document: Model, tiers, prices, features, discounts
3. Screenshot pricing pages
4. Sign up for trials (test product)
5. Analyze: Positioning, messaging, gaps

**When to use:**
- Market entry
- Pricing updates
- Competitive positioning

**Pros:**
- Objective data (publicly available)
- Fast (1-2 weeks)
- Inexpensive (free if DIY)

**Cons:**
- Surface-level (don't see discounting, negotiation)
- Copycat risk (follow competitors blindly)
- Static (pricing changes frequently)

**Deliverable:** Competitive pricing audit matrix

**Reference:** `templates/competitive-pricing-audit-template.md`

---

### Price Elasticity Testing

**What it is:**
Measure how demand changes when price changes

**Method:**
A/B test different prices:
- 50% see price A ($99)
- 50% see price B ($119)
- Measure conversion, revenue

**Analysis:**
- Price elasticity = (% change in demand) / (% change in price)
- Example: +20% price → -5% demand = -0.25 elasticity (inelastic = good)

**When to use:**
- Have traffic (250+ visitors per variation)
- Established product (can A/B test)
- Optimize existing pricing

**Pros:**
- Real behavior (not stated preference)
- Quantifies price sensitivity
- Identifies optimal price point

**Cons:**
- Requires traffic (sample size)
- Ethical concerns (different prices to different people)
- Time (30-60 days minimum)

**Reference:** `core/09-pricing-experimentation-testing.md`

---

## Pricing Strategy Frameworks

### Value-Based Pricing

**Definition:** Price based on value delivered to customer (not cost or competition)

**Process:**
1. Quantify value delivered
   - Time saved: Hours/week × Hourly rate
   - Revenue generated: Sales increase, conversions
   - Cost reduced: Efficiency gains
2. Calculate ROI
   - Example: Save 10 hours/week × $100/hour = $1,000 value/week
3. Price as % of value
   - Price: 10-20% of value delivered
   - Example: $1,000 value/week → $200/month ($800/month customer keeps)

**When to use:**
- Clear, quantifiable value
- B2B (easier to quantify business value)
- Premium positioning

**Pros:**
- Aligns price with value (fair)
- Maximizes revenue (charge what customer gets)
- Easier to sell (ROI-based)

**Cons:**
- Value varies by customer (hard to standardize)
- Requires research (quantify value)
- Customer may not perceive value same way

**Example:**
- Salesforce saves sales reps 2 hours/day
- Sales rep costs $60/hour
- Value: 2 hours × $60 × 20 days = $2,400/month
- Salesforce price: $150/user/month (6% of value)

**Reference:** `core/01-pricing-fundamentals-strategy.md`

---

### Cost-Plus Pricing

**Definition:** Price = Cost + Markup

**Formula:** Price = (COGS + Fixed costs) × (1 + Desired margin)

**Example:**
- Cost to serve: $10/customer/month
- Desired margin: 80%
- Price: $10 / (1 - 0.80) = $50/month

**When to use:**
- Commodity products
- Manufacturing (physical goods)
- Regulated industries

**Pros:**
- Simple (easy to calculate)
- Guarantees margin

**Cons:**
- Ignores value (leave money on table)
- Ignores competition (may overprice)
- Not recommended for SaaS (low marginal cost)

**SaaS reality:**
- Cost to serve: $5/customer/month (infrastructure)
- Cost-plus at 80% margin: $25/month
- But value delivered: $500/month → should price $100-200/month
- Result: Cost-plus underprices significantly

**Reference:** `core/01-pricing-fundamentals-strategy.md`

---

### Competitor-Based Pricing

**Definition:** Price based on what competitors charge

**Variants:**
- **Match competitors:** Same price as market leader
- **Undercut:** 10-20% below competitors (value play)
- **Premium:** 20%+ above competitors (quality/differentiation play)

**When to use:**
- Commoditized market (price-sensitive)
- New entrant (need market share)
- Parity product (no differentiation)

**Pros:**
- Market-validated (customers familiar)
- Competitive (won't lose on price)
- Simple (just copy competitors)

**Cons:**
- Race to the bottom (price wars)
- Ignores value (may underprice)
- Reactive (not strategic)

**Best practice:**
- Use competitive analysis as input (not sole driver)
- Price based on value, check vs competition
- Differentiate (don't compete only on price)

**Reference:** `core/03-competitive-market-analysis.md`

---

### Penetration Pricing

**Definition:** Price low to gain market share quickly, raise later

**Example:**
- Launch at $49/month (below competitors at $99)
- Gain 10,000 customers in Year 1
- Year 2: Raise to $79, then $99 (over time)

**When to use:**
- New market entry
- Winner-take-all dynamics (network effects)
- Land-and-expand strategy

**Pros:**
- Fast adoption (low barrier)
- Market share capture
- Word-of-mouth (low price = tryable)

**Cons:**
- Low margin (hard to sustain)
- Trains market to expect low price
- Raising prices later = churn risk

**Example:** Uber (subsidized rides initially to gain riders + drivers)

---

### Skimming Pricing

**Definition:** Price high initially, lower over time

**Example:**
- Launch at $199/month (premium positioning)
- Early adopters pay premium
- Year 2: Add $99 tier (expand market)

**When to use:**
- Innovative product (first to market)
- Premium brand positioning
- Low price elasticity (not price-sensitive)

**Pros:**
- Maximizes early revenue (high WTP customers)
- Premium positioning
- Can lower later (expand market)

**Cons:**
- Limits adoption (high price barrier)
- Attracts competition (high margins)
- Hard to raise later (only lower)

**Example:** Apple iPhone (high initial price, lower-priced models later)

---

## Packaging Frameworks

### Good/Better/Best

**Structure:** 3 tiers (sometimes + Enterprise)

**Tiers:**
- **Good (Tier 1):** Basic, entry-level
  - Target: 15-20% of customers
  - Purpose: Low barrier, gateway
- **Better (Tier 2):** Target tier ⭐
  - Target: 60-70% of customers
  - Purpose: Best value, optimal choice
- **Best (Tier 3):** Premium, power users
  - Target: 15-20% of customers
  - Purpose: Anchor pricing, serve high-end

**Psychology:**
- Decoy effect (Tier 1 makes Tier 2 attractive)
- Anchoring (Tier 3 makes Tier 2 seem reasonable)
- Choice architecture (3 options optimal)

**Reference:** `core/06-packaging-tier-design.md`

---

### Freemium Ladder

**Structure:** Free → Paid tiers

**Free tier:**
- Core value (must be useful)
- Limited scale (10 projects, 5 users, 100 API calls)
- Upgrade triggers (hit limit, want advanced feature)

**Paid tiers:**
- Remove limits (unlimited projects, users, etc.)
- Add features (analytics, integrations, etc.)
- Add support (priority, phone, CSM)

**Conversion:** 2-5% free → paid (typical), 6-8% (good)

**Reference:** `advanced/freemium-free-trial-strategies.md`

---

### PLG (Product-Led Growth) Packaging

**Principles:**
- Self-serve (no sales call required)
- Free entry (freemium or trial)
- Value before price (aha moment first)
- Viral (encourage sharing, collaboration)

**Tier design:**
- Free: Individual use, limited
- Tier 1: Small team, collaboration
- Tier 2: Growing team, advanced features
- Tier 3: Large team, no limits
- Enterprise: Custom, security, support

**Reference:** `advanced/product-led-growth-monetization.md`

---

## Pricing Model Selection

### Decision Framework

**Questions:**
1. **How do customers want to pay?**
   - Predictable subscription vs pay-as-you-go?
2. **What correlates with value?**
   - Users, usage, data, features?
3. **How does usage vary?**
   - Uniform (flat pricing) vs 10x variance (usage-based)?
4. **What's measurable?**
   - Can you accurately track the metric?

**Model mapping:**
- **Flat-rate:** Simple product, uniform usage
- **Tiered:** Different customer segments (SMB vs enterprise)
- **Per-user:** Value = team size (collaboration tools)
- **Usage-based:** Value = consumption (APIs, infrastructure)
- **Hybrid:** Predictable base + variable expansion

**Reference:** `core/04-choosing-pricing-model.md`

---

## Value Metric Selection

### Patrick Campbell Framework

**Criteria for good value metric:**
1. **Correlates with value delivered**
   - More [metric] = more value
2. **Easy to understand**
   - Customer can predict usage/costs
3. **Grows as customer succeeds**
   - Metric increases with customer growth
4. **Measurable**
   - Can accurately track per customer

**Examples:**
- Slack: Per user (correlates with team size/value)
- Stripe: Per transaction (correlates with revenue processed)
- Dropbox: Per GB (correlates with data stored)
- Calendly: Per event type (correlates with meeting complexity)

**Reference:** `core/05-selecting-value-metrics.md`

---

## International Pricing

### Purchasing Power Parity (PPP) Model

**Formula:** Local price = US price × (Local PPP / US PPP)

**Example:**
- US price: $99
- India PPP index: 0.42
- India price: $99 × 0.42 = $42

**When to use:**
- Global expansion
- Large WTP variance by country
- Volume opportunity in emerging markets

**Pros:**
- Fair (adjusts for purchasing power)
- Data-driven (World Bank data)
- Increases access (affordable in emerging markets)

**Cons:**
- Complex (multiple price points)
- Arbitrage risk (VPN to cheaper country)
- Perception (customers compare prices)

**Reference:** `advanced/international-localized-pricing.md`

---

### Regional Pricing Tiers

**Model:** 3-4 regional price bands

**Example:**
- Tier 1 (High-WTP): US, Nordics, Switzerland, Australia → $99
- Tier 2 (Medium): Western Europe, Japan → $79
- Tier 3 (Low): Eastern Europe, LatAm, SE Asia → $49
- Tier 4 (Very Low): India, Africa → $29

**Simpler than:** Country-by-country pricing

**Reference:** `advanced/international-localized-pricing.md`

---

## Discounting Strategies

### Annual Discount Model

**Standard:** 16-20% discount (2 months free)

**Formula:**
- Monthly price × 12 = $1,188
- Annual price = $999 (16% discount)
- Messaging: "Get 2 months free"

**Impact:**
- Annual adoption: 30-50% of customers
- Lower churn: 20-30% lower than monthly
- Faster CAC payback: Instant (upfront cash)

**Reference:** `advanced/discount-strategies-annual-pricing.md`

---

### Volume Discount Model

**Structure:** Price per unit decreases with volume

**Example:**
- 1-10 users: $20/user/month
- 11-50 users: $18/user/month (-10%)
- 51-200 users: $15/user/month (-25%)
- 201+ users: Custom (-30-40%)

**Purpose:**
- Incentivize expansion (add more users)
- Reward large customers
- Compete for enterprise deals

**Reference:** `advanced/discount-strategies-annual-pricing.md`

---

## Optimization Methodologies

### A/B Testing

**Setup:**
- Control: Current pricing
- Variant: New pricing
- Split: 50/50 traffic
- Duration: 30-60 days
- Sample: 250-500 per variation

**Metrics:**
- Primary: Revenue per visitor (conversion × price)
- Secondary: Conversion rate, ACV, churn
- Guardrail: NPS, churn (don't harm)

**Decision:**
- If statistically significant + revenue increase → Implement
- If not significant → Keep current
- If guardrails violated → Reject

**Reference:** `core/09-pricing-experimentation-testing.md`

---

### Cohort Analysis

**Method:**
Track customers by signup month, compare metrics

**Example:**
- Jan 2024 cohort: 100 customers, 80% retained at 12 months
- Feb 2024 cohort: 100 customers, 85% retained at 11 months
- Insight: Newer cohorts retaining better (pricing improvements working)

**Use:**
- Validate pricing changes (are new customers better?)
- Segment analysis (SMB vs enterprise)
- Churn prediction

**Reference:** `core/12-monitoring-optimization-metrics.md`

---

**Last updated:** 2025-01-13
**Source:** 2023-2025 industry research and frameworks
