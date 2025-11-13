# Discount Strategies & Annual Pricing

Optimize discounting and annual billing for cash flow and retention.

## Overview

**Discounting goals:**
1. Incentivize annual billing (improve cash flow, reduce churn)
2. Close deals faster (volume discounts, multi-year)
3. Reward loyalty (renewals, early adopters)
4. Enable accessibility (non-profit, education, startups)

**2024 data:**
- 30-50% of B2B SaaS customers choose annual billing
- Annual customers have 20-30% lower churn vs monthly
- Optimal annual discount: 16-20% (2 months free)

## Annual vs Monthly Pricing

### Why Offer Annual Billing

**Benefits:**

**1. Cash flow (upfront payment)**
- Monthly: $99 × 12 months = $1,188/year (paid over time)
- Annual: $1,188 paid upfront (Day 1 cash)
- **Impact:** Fund growth, reduce burn rate

**2. Lower churn**
- Monthly: 5-7% churn/month (avg)
- Annual: 2-3% churn/month (locked in for year)
- **Why:** Psychological commitment + switching cost

**3. Faster CAC payback**
- Monthly ($99): Recover $1,200 CAC in 12 months
- Annual ($1,188 upfront): Recover CAC in Day 1
- **Impact:** Improve unit economics

**4. Predictable revenue**
- Monthly: Varies (churn, expansion, seasonality)
- Annual: Locked in (12 months visibility)

---

### Optimal Annual Discount

**2024 benchmark:** 16-20% discount for annual (most common)

**Translation:**
- 16% = 2 months free ($99/month → $999/year)
- 20% = 2.4 months free ($99/month → $950/year)
- 25% = 3 months free ($99/month → $891/year)

**Data:**
- 16-20% discount → 30-40% of customers choose annual
- 25%+ discount → 50%+ choose annual (but margin erosion)
- <15% discount → <25% choose annual (not compelling)

**Recommendation:** Start at 16-17%, test up to 20%

See `core/09-pricing-experimentation-testing.md` for testing methodology.

---

### Messaging Annual Discount

**Option 1: Percentage discount**
- "Save 20% with annual billing"
- Clear, straightforward

**Option 2: Dollar savings**
- "Save $240/year with annual"
- Concrete, tangible

**Option 3: Months free**
- "Get 2 months free with annual"
- Most compelling (tested 18% higher conversion vs % discount)

**Recommendation:** Use "months free" (highest conversion)

**Example:**
```
Monthly: $99/month
Annual: $990/year (Get 2 months free!)
```

---

## Discount Types & Strategies

### 1. Annual Billing Discount

**Standard: 16-20% off monthly price**

**Example:**
- Monthly: $99/month ($1,188/year)
- Annual: $990/year (17% discount, 2 months free)

**Eligibility:** All customers

**Goal:** Incentivize annual commitment

---

### 2. Multi-Year Discount

**Model:** Additional discount for 2-3 year commitments

**Example:**
- 1-year: $990/year (17% vs monthly)
- 2-year: $1,782/2 years (25% vs monthly, 10% vs 1-year)
- 3-year: $2,376/3 years (33% vs monthly, 20% vs 1-year)

**Eligibility:** Enterprise customers (large ACV)

**Goal:** Lock in revenue, reduce churn, improve LTV

**2024 data:** 10-15% of enterprise customers accept multi-year

---

### 3. Volume Discount

**Model:** Discount based on # of users/seats

**Example (per-user pricing):**
- 1-10 users: $20/user/month
- 11-50 users: $18/user/month (10% discount)
- 51-200 users: $15/user/month (25% discount)
- 201+ users: Custom (30-40% discount)

**Eligibility:** Mid-market and enterprise

**Goal:** Incentivize expansion (add more users)

**Impact:** 15-25% revenue increase from volume incentives (expand vs churn)

---

### 4. Renewal Discount

**Model:** Discount for renewing early (before contract expires)

**Example:**
- Renew 90+ days early: 10% discount on next year
- Renew 60-89 days early: 5% discount

**Goal:** De-risk churn (lock in before they consider alternatives)

**2024 data:** 20-30% of customers renew early for discount

---

### 5. Startup/Early-Stage Discount

**Model:** 50% off Year 1 for qualifying startups

**Qualification:**
- <2 years old
- <$1M funding or <$1M revenue
- First-time customer

**Example:**
- Regular: $149/month
- Startup: $75/month Year 1, then $149 Year 2

**Goal:** Acquire high-growth customers early (land before they scale)

**Providers:** YC Startup School, Stripe Atlas, Microsoft for Startups (50-100% discounts)

---

### 6. Non-Profit & Education Discount

**Model:** 20-50% off for qualified organizations

**Qualification:**
- 501(c)(3) non-profit (US) or equivalent
- Accredited educational institution
- Proof required (.edu email, tax docs)

**Example:**
- Regular: $99/month
- Non-profit/Edu: $49/month (50% off)

**Goal:** Social impact, brand building, future revenue (students → professionals)

---

### 7. Competitive Displacement Discount

**Model:** Temporary discount to win customer from competitor

**Example:**
- Customer currently paying competitor $10K/year
- Offer: $7K Year 1 (30% off), $9K Year 2 (10% off), $10K Year 3 (full price)

**Goal:** Win competitive deals (temporary margin sacrifice)

**Approval:** VP Sales or CEO (case-by-case)

---

### 8. Upsell/Cross-Sell Discount

**Model:** Discount when customer buys additional products

**Example:**
- Product A: $99/month
- Product B: $79/month
- Bundle: $149/month (16% discount vs $178 separate)

**Goal:** Increase wallet share, reduce churn (more products = stickier)

---

## Discounting Policies & Governance

### Discount Authority Matrix

| Discount | Who Can Approve | Notes |
|----------|-----------------|-------|
| 0-10% | AE (sales rep) | Standard annual, volume |
| 10-20% | Sales Manager | Multi-year, large deals |
| 20-30% | VP Sales | Strategic accounts, competitive |
| 30-40% | CEO | Rare, case-by-case |
| >40% | Board (almost never) | Only for massive strategic deals |

**Why needed:** Prevent over-discounting (train customers to negotiate)

---

### Discount Approval Process

**Step 1: AE requests discount**
- Submits deal details: Customer, ACV, discount %, rationale
- Example: "Request 25% discount for 3-year commitment ($100K → $75K)"

**Step 2: Manager reviews**
- Checks: Is deal strategic? Competitive? Within policy?
- Approves or denies (or negotiates counter-offer)

**Step 3: Contract**
- Discount reflected in quote/contract
- Tracked in CRM (Salesforce, HubSpot)

**Step 4: Post-mortem**
- Quarterly review: Avg discount %, win rate by discount level
- Adjust policy if needed

---

## When NOT to Discount

### Red Flags

❌ **Customer asks for discount before seeing product**
- Indicates price shopping, not value shopping
- Action: Demo value first, discuss price later

❌ **Discount request without rationale**
- "Can you do better on price?" (vague)
- Action: Ask "What price were you expecting?" (anchor them)

❌ **Customer threatens to churn for discount**
- "I'll cancel unless you give me 50% off"
- Action: Offer minor discount (5-10%) or accept churn (don't train bad behavior)

❌ **Discount erodes margin below threshold**
- Gross margin <70% after discount (unsustainable)
- Action: Hold firm or walk away

---

### Alternatives to Discounting

**Alternative 1: Add value instead**
- Don't discount price, add features/services
- Example: "I can't discount, but I can include advanced analytics ($50/month value)"

**Alternative 2: Extended payment terms**
- "I can't discount, but I can offer quarterly payments instead of annual upfront"
- Customer gets cash flow relief, you keep price

**Alternative 3: Free pilot/trial extension**
- "I can't discount, but I can extend your trial 30 days so you can fully evaluate"

**Alternative 4: Flex on contract terms**
- "I can't discount, but I can reduce auto-renewal notice from 90 days to 30 days"

---

## Annual Pricing Psychology

### Framing Monthly vs Annual

**Bad:**
```
Monthly: $99/month
Annual: $1,188/year
```
(Sticker shock from $1,188)

**Better:**
```
Monthly: $99/month
Annual: $990/year (Save $198)
```
(Emphasize savings)

**Best:**
```
○ Monthly: $99/month
● Annual: $82.50/month (billed annually, save 2 months)
```
(Show monthly equivalent + savings in months)

**Why:** Anchors to $99 (familiar), then shows discount ($82.50 feels cheaper)

---

### Toggle Design

**Effective toggle (Notion example):**
```
[ Monthly ]  [ Annual - Save 20% ]
```

**Highlight annual:** Make annual the default or visually emphasized

**2024 data:** Annual toggle highlighted = 35% choose annual vs 25% when neutral

---

## Monitoring Discount Impact

### Metrics to Track

**1. Average discount %**
- Formula: Total discounts / Total revenue × 100
- Benchmark: 10-20% for B2B SaaS
- **Too high (>30%):** Over-discounting (margin erosion)

**2. Discount by segment**
- SMB: 5-10%
- Mid-market: 10-20%
- Enterprise: 20-40%
- **Insight:** Segment expectations differ

**3. Win rate by discount level**
- 0-10% discount: 30% win rate
- 10-20%: 50% win rate
- 20-30%: 70% win rate
- **Insight:** Diminishing returns (30% discount not 2x better than 20%)

**4. Annual vs monthly mix**
- % choosing annual billing
- Benchmark: 30-50% (target 40%+)
- **If low (<30%):** Increase annual discount or improve messaging

**5. Multi-year adoption**
- % of enterprise deals on multi-year
- Benchmark: 10-15%
- **Opportunity:** Increase multi-year incentives

---

## Key Takeaways

1. **Annual discount: 16-20% (2 months free)** - Standard, 30-40% adoption
2. **"Months free" messaging** - Converts 18% better than "% off"
3. **Multi-year: +10% discount** - On top of annual (total 25-30% vs monthly)
4. **Volume discounts: 10-30%** - Incentivize expansion (more users)
5. **Discount authority: AE <10%, Manager 10-20%, VP 20-30%** - Prevent over-discounting
6. **Annual customers: 20-30% lower churn** - Major retention benefit
7. **Alternatives to discounting:** Add value, extend terms, longer trial

## Next Steps

**Test annual discount levels:**
→ Read `core/09-pricing-experimentation-testing.md`

**Design pricing page with annual toggle:**
→ Read `core/08-pricing-page-design.md`

**Track discount metrics:**
→ Read `core/12-monitoring-optimization-metrics.md`
