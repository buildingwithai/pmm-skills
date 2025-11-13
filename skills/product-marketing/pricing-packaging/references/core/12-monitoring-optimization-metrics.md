# Monitoring & Optimization Metrics

Track pricing performance and optimize continuously.

## Overview

Pricing is not "set and forget"—it requires ongoing monitoring and optimization.

**Best practice cadence:**
- Early-stage: Monthly reviews
- Growth-stage: Quarterly reviews
- Scale-stage: Bi-annual reviews

## Key Pricing Metrics

### 1. Conversion Rate by Tier

**What it measures:** % of visitors who purchase each tier

**Formula:** (Purchases of Tier X / Pricing Page Visitors) × 100

**Example:**
- 1,000 visitors to pricing page
- 50 purchase Starter tier = 5% conversion
- 80 purchase Pro tier = 8% conversion
- 20 purchase Business tier = 2% conversion

**Benchmark (B2B SaaS):**
- Self-serve: 2-5% (typical), 6-8% (good)
- Trial-to-paid: 15-25% (typical), 30-40% (good)

**Insights:**
- Which tier converts best?
- Is middle tier converting 60-70%? (expected)
- Lower conversion than expected = pricing too high or poor positioning

---

### 2. Average Contract Value (ACV)

**What it measures:** Average annual revenue per customer

**Formula:** Total Annual Revenue / # of Customers

**Example:**
- 100 customers
- $500K annual revenue
- ACV = $5,000

**Segment by tier:**
- Starter ACV: $588/year ($49/month)
- Pro ACV: $1,788/year ($149/month)
- Business ACV: $4,788/year ($399/month)

**Trends to track:**
- Is ACV growing (customers upgrading)?
- Is ACV by cohort improving (newer customers buying higher tiers)?

**2024 Benchmarks:**
- SMB SaaS: $500-$5,000 ACV
- Mid-market SaaS: $5,000-$50,000 ACV
- Enterprise SaaS: $50,000-$500,000+ ACV

---

### 3. Net Revenue Retention (NRR)

**What it measures:** Revenue retention + expansion from existing customers

**Formula:** ((Starting MRR + Expansion - Churn - Contraction) / Starting MRR) × 100

**Example:**
- Start of month: $100K MRR
- Expansion (upgrades): +$20K
- Churn (canceled): -$8K
- Contraction (downgrades): -$2K
- End: $110K from same cohort
- NRR = ($110K / $100K) × 100 = 110%

**Interpretation:**
- <100% = losing revenue from cohort (bad)
- 100-110% = okay, some expansion
- **110-120% = good**
- **120%+ = excellent**

**2024 Benchmarks:**
- Average B2B SaaS: 100-110% NRR
- High-growth SaaS: **115-125% NRR** (target)
- Best-in-class: 130%+ NRR

**Pricing impact:**
- Good pricing enables expansion (upsells, cross-sells, usage growth)
- Hybrid models (subscription + usage) = 38% higher NRR (2024 data)

---

### 4. Customer Acquisition Cost (CAC) Payback

**What it measures:** Months to recover acquisition cost

**Formula:** CAC / (MRR × Gross Margin)

**Example:**
- CAC = $1,200
- MRR = $150
- Gross Margin = 80%
- Payback = $1,200 / ($150 × 0.80) = 10 months

**2024 Benchmarks:**
- Excellent: <6 months
- Good: 6-12 months
- Acceptable: 12-18 months
- Concerning: >18 months

**Pricing impact:**
- Higher prices = faster payback
- Annual billing = instant payback (cash upfront)

---

### 5. Price Sensitivity by Segment

**What it measures:** Conversion rate changes when price changes

**Example:**
- SMB (<50 employees): -20% conversion when price +10%
- Mid-market (50-500): -10% conversion when price +10%
- Enterprise (500+): -2% conversion when price +10%

**Insight:** Enterprise less price-sensitive, SMB very sensitive

**Application:** 
- SMB: Keep pricing transparent, competitive
- Enterprise: Focus on value, less on price

---

### 6. Expansion Revenue %

**What it measures:** % of revenue from existing customers (not new)

**Formula:** (Expansion Revenue / Total Revenue) × 100

**Example:**
- Total revenue: $100K/month
- New customer revenue: $60K
- Expansion revenue (upgrades, upsells): $40K
- Expansion % = 40%

**2024 Benchmarks:**
- Median SaaS: 20-30%
- High-growth SaaS: 35-45%
- Best-in-class: 50%+

**Pricing impact:**
- Good tier structure = easier upgrades
- Usage-based = automatic expansion
- Feature gating = expansion triggers

---

### 7. Annual vs Monthly Mix

**What it measures:** % choosing annual vs monthly billing

**Example:**
- 100 new customers
- 60 choose monthly
- 40 choose annual
- Annual mix = 40%

**2024 Benchmarks:**
- B2B SaaS: 30-50% annual (target: 40%+)
- Enterprise: 70-90% annual
- SMB: 20-40% annual

**Pricing impact:**
- Annual discount affects mix (16-20% = 30-40% annual, 25%+ = 50%+ annual)
- Higher annual mix = better cash flow, lower churn

---

## Dashboard Setup

### Weekly Pricing Metrics Dashboard

**Core metrics (check weekly):**
- Pricing page traffic
- Conversion rate by tier
- MRR/ARR growth
- Churn rate (%)
- Support tickets re: pricing

**Tools:** 
- Google Analytics (traffic)
- Stripe/Chargebee (conversions, revenue)
- Mixpanel/Amplitude (product analytics)

---

### Monthly Pricing Deep-Dive

**Metrics to review monthly:**
- Conversion rate trends (up/down?)
- ACV by cohort (improving?)
- NRR (stable, growing, shrinking?)
- CAC payback (getting faster?)
- Expansion revenue (growing?)
- Annual vs monthly mix

**Actions:**
- If conversion dropping: Diagnose (price too high? positioning issue? competitive?)
- If NRR declining: Focus on retention and expansion
- If CAC payback lengthening: Consider raising prices or improving LTV

---

### Quarterly Pricing Review (Monetization Council)

**Agenda:**

**1. Performance review (30 min)**
- Review quarterly metrics vs targets
- Segment analysis (SMB vs enterprise, geography)
- Cohort trends (are newer customers better?)

**2. Experiment results (20 min)**
- A/B test outcomes
- Learnings and insights
- Recommendations

**3. Customer feedback (20 min)**
- Pricing objections from sales
- Churn reasons (is price a factor?)
- Competitive intel (what are competitors doing?)

**4. Proposed changes (30 min)**
- Price increase recommendations
- Packaging adjustments
- New tier proposals
- Model changes (subscription → usage)

**5. Next quarter plan (10 min)**
- Experiments to run
- Research needed
- Launch timeline

---

## Cohort Analysis

### Why Cohorts Matter

**Cohort:** Customers who signed up in same time period (month, quarter)

**Track by cohort:**
- Retention rates
- Expansion rates
- LTV
- Pricing tier distribution

**Example:**
- Jan 2024 cohort: 100 customers, 40% on Pro, 60% on Business
- Jan 2025 cohort: 100 customers, 20% on Pro, 80% on Business
- **Insight:** Newer cohorts buying higher tiers = pricing attracting better customers

---

### Cohort Retention Table

```
Cohort    | Month 0 | Month 3 | Month 6 | Month 12
----------|---------|---------|---------|----------
Jan 2024  | 100%    | 92%     | 85%     | 78%
Feb 2024  | 100%    | 90%     | 83%     | 75%
Mar 2024  | 100%    | 88%     | 80%     | ?
```

**Insights:**
- Are newer cohorts retaining better? (pricing improvements working)
- Is retention declining? (churn increasing, investigate)

---

## Leading Indicators (Predict Future Revenue)

### 1. Trial-to-Paid Conversion

**Leading indicator for:** MRR growth

**If trial conversion drops:** Future MRR will decline

**Action:** Optimize onboarding, pricing page, trial experience

---

### 2. Feature Adoption by Tier

**Measure:** % of Pro tier customers using advanced features

**Example:**
- Pro tier includes "Advanced Analytics"
- Only 30% of Pro customers using it
- **Insight:** Feature not valuable, or not discovered? (investigate)

**Action:** 
- If not valuable: Remove from Pro, add different feature
- If not discovered: Improve onboarding, in-app prompts

---

### 3. Upgrade Requests

**Measure:** # of customers requesting tier upgrades

**Leading indicator for:** Expansion revenue

**If upgrade requests increasing:** Pricing tiers working, customers growing

**If decreasing:** Top tier too generous (no reason to upgrade) or customers not growing

---

### 4. Usage Trends (Usage-Based Pricing)

**Measure:** Average usage growth month-over-month

**Example:**
- Average customer: 10K API calls/month (Month 1)
- Average customer: 15K API calls/month (Month 6)
- **50% usage growth** = automatic revenue expansion

**If usage flat or declining:** Customer not getting value (churn risk)

---

## Optimization Experiments

### Experiment 1: Raise Prices 10-20%

**Hypothesis:** We're underpriced, can raise without major conversion loss

**Test:** New customers see $119 vs $99 (20% increase)

**Measure:** 
- Conversion rate (expect 5-10% drop)
- Revenue per visitor (should increase)
- Customer quality (churn, LTV)

**Duration:** 60 days, 500 visitors per variation

**Decision:**
- If revenue per visitor higher: Implement
- If conversion drops >15%: Keep old price

---

### Experiment 2: Change Annual Discount

**Hypothesis:** 20% annual discount (vs current 16%) will increase annual mix

**Test:** 
- Control: 16% discount (2 months free)
- Variant: 20% discount (2.4 months free)

**Measure:** Annual vs monthly mix

**Duration:** 60 days

**Decision:**
- If annual mix increases >10 percentage points: Implement
- If minimal change: Keep current discount

---

### Experiment 3: Tier Repackaging

**Hypothesis:** Moving [Feature X] from Business to Pro will increase Pro conversion

**Test:**
- Control: Current packaging
- Variant: Feature X in Pro tier

**Measure:** Pro tier conversion, Business tier conversion

**Duration:** 60 days

**Decision:**
- If Pro conversion increases >15% without killing Business tier: Implement

---

## Continuous Optimization Cycle

### Monthly Cycle

**Week 1:** Analyze previous month metrics
**Week 2:** Design experiment based on insights
**Week 3:** Launch experiment
**Week 4:** Monitor results

**Repeat:** Every month, always testing something

---

### Quarterly Cycle

**Q1 Review (Week 1):** What worked, what didn't
**Q1 Planning (Week 2):** Prioritize next 3 experiments
**Q2-Q4:** Run experiments, gather data
**Q1 (Next year):** Implement winners, repeat

---

## When to Make Major Pricing Changes

### Triggers for Major Overhaul

**Product-side:**
- ✅ Launched major new capabilities (justify price increase)
- ✅ Shifted product strategy (PLG → sales-led, vice versa)
- ✅ New value metric makes more sense (per-user → usage)

**Market-side:**
- ✅ Competitors raised prices 15%+
- ✅ Market matured (can charge premium)
- ✅ Geographic expansion (need localized pricing)

**Business-side:**
- ✅ Missed revenue targets 2 quarters in row
- ✅ Churn >10% (pricing disconnect with value)
- ✅ NRR declining (need better expansion)

**Frequency:**
- Major changes: Annually maximum
- Minor tweaks: Quarterly okay
- Experiments: Ongoing

---

## Key Takeaways

1. **Monitor weekly, review monthly, overhaul quarterly**
2. **NRR is king** - Target 115-125% for high-growth
3. **Cohort analysis reveals trends** - Are newer customers better?
4. **Conversion + ACV = revenue** - Optimize both, not just conversion
5. **Leading indicators predict future** - Trial conversion, usage growth
6. **Always be testing** - Monthly experiments, continuous optimization
7. **Major changes max annually** - Don't whipsaw customers

## Next Steps

**Need to optimize existing pricing:**
→ Read `core/09-pricing-experimentation-testing.md`

**Ready to handle price increases:**
→ Read `advanced/price-increase-communication-migration.md`

**Want to deep-dive specific topics:**
→ See advanced/ files for usage-based, freemium, enterprise, international

**✅ CORE PRICING CURRICULUM COMPLETE**
You've completed all 12 core pricing files. Ready to apply advanced topics or implement what you've learned.
