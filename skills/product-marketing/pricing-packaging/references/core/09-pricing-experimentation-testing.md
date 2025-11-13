# Pricing Experimentation & Testing

Test pricing scientifically to maximize revenue and conversion.

## Overview

**Reality:** Only 24% of SaaS companies regularly test pricing (2024 data).

**Those who test:** Outperform peers by 30% in Net Revenue Retention.

**Why most don't test:** Fear of customer perception ("unfair"), lack of infrastructure, don't know how.

**Truth:** You can test pricing ethically and effectively.

## The Power of Testing

**Impact of 1% improvements:**
- Price: +11-15% operating profit
- Packaging: +8-12% conversion
- Page design: +5-10% conversion

**Example:** Changing from "$99/month" to "$95/month billed annually" increased conversions 18% (real case).

## What to Test

### Price Points

**Test variations:**
- ±10-20% from current price
- Example: $99 vs $119 vs $79

**Don't test:**
- >30% variations (too extreme)
- Too many variations (splits traffic thin)

**Sample test:**
- Control: $99/month
- Variant A: $119/month (+20%)
- Variant B: $89/month (-10%)

Run 30-60 days, measure conversion, revenue, churn.

---

### Packaging (Feature Allocation)

**Test:**
- Which features in which tier
- Tier names
- Number of tiers (3 vs 4)

**Example test:**
- Control: Basic ($49), Pro ($99), Business ($199)
- Variant: Starter ($49), Team ($149), Enterprise ($299)

Measure: Conversion to each tier, ACV, NRR.

---

### Presentation

**Test:**
- CTA copy ("Get Started" vs "Start Free Trial")
- Tier order (high-to-low vs low-to-high)
- Highlighted tier (which gets "Most Popular")
- Framing (annual vs monthly default)
- Comparison table design

**Example test:**
- Control: "Get Started" CTA
- Variant: "Start Free Trial" CTA

Measure: Click-through rate, trial starts.

---

### Discount Strategies

**Test:**
- Annual discount (15% vs 20% vs 25%)
- Messaging ("Save $240" vs "2 months free")
- Volume discounts (at what tier)

**Example test:**
- Control: "Save 16% with annual" ($1,000/year)
- Variant A: "Save $200 with annual" ($1,000/year)
- Variant B: "2 months free with annual" ($1,000/year)

Measure: Annual vs monthly adoption rate.

---

## Statistical Requirements

### Sample Size

**Minimum:**
- 250-500 visitors per variation
- For conversion rate tests (trial signups, purchases)

**Rule of thumb:**
- Smaller difference = larger sample needed
- Testing $99 vs $100 (1% diff) = 10,000+ visitors needed
- Testing $99 vs $119 (20% diff) = 250-500 visitors sufficient

**Calculator:** Use online A/B test calculator (Optimizely, VWO, Evan's Awesome A/B Tools).

---

### Time Duration

**Minimum:** 30-60 days

**Why:** 
- Account for weekly/monthly cycles
- Allow statistical significance
- Capture different customer segments (early vs late month visitors)

**Warning:** Don't end test early just because one variation "winning" at day 7.

---

### Statistical Significance

**Target:** 95% confidence level

**Meaning:** 95% confident the difference is real, not chance.

**P-value:** <0.05 (5% chance result is random)

**Tools calculate automatically:** VWO, Optimizely, Google Optimize.

---

## Testing Methodologies

### A/B Test (Price Point)

**Setup:**
- 50% see price A ($99)
- 50% see price B ($119)

**Randomization:** By visitor (not by account—one price per visitor always)

**Duration:** 30-60 days

**Measure:** 
- Conversion rate (which price converts better)
- Revenue (which generates more $)
- Customer quality (which gets lower churn)

**Winner determination:**
- If $99 converts 10% and $119 converts 8%:
  - $99 revenue: $99 × 10% = $9.90 per visitor
  - $119 revenue: $119 × 8% = $9.52 per visitor
  - Winner: $99 (higher revenue per visitor)

---

### Multivariate Test (Package + Price)

**Setup:** Test multiple changes simultaneously

**Example:**
- Variant A: $99, 3 tiers, "Get Started" CTA
- Variant B: $119, 3 tiers, "Start Trial" CTA
- Variant C: $99, 4 tiers, "Get Started" CTA
- Variant D: $119, 4 tiers, "Start Trial" CTA

**Requires:** 4x traffic (250-500 per variation = 1,000-2,000 total)

**Use when:** Have high traffic, want to test interactions

**Don't use:** Low traffic (takes forever to reach significance)

---

### Sequential Testing (Price Laddering)

**Setup:** Test prices sequentially, not simultaneously

**Example:**
- Month 1-2: $99 → measure conversion
- Month 3-4: $119 → measure conversion
- Month 5-6: $79 → measure conversion

**Use when:**
- Low traffic (can't split)
- Want to test more than 2-3 variations
- Okay with slower results

**Warning:** Confounds with seasonality (Month 3 results may differ because of market, not price)

---

## SMB vs Enterprise Testing

### SMB Pricing Tests

**Characteristics:**
- High volume (100s-1000s of visitors/month)
- Short sales cycles (hours-days)
- Can A/B test effectively

**Approach:**
- A/B test price points (±10-20%)
- Test over 30-60 days
- 250-500 per variation

**Example:**
- Traffic: 2,000 visitors/month to pricing page
- Split: 1,000 see $99, 1,000 see $119
- Duration: 60 days → 2,000 per variation → statistically significant

---

### Enterprise Pricing Tests

**Characteristics:**
- Low volume (10-50 deals/month)
- Long sales cycles (weeks-months)
- Can't A/B test traditional way

**Approach:**
- Test with 3-5 key accounts (not randomized A/B)
- Larger price variations (20-40% okay)
- Longer assessment (3-6 months)
- Qualitative feedback heavy

**Example:**
- Offer 3 enterprise prospects pricing at $200K/year
- Offer 3 other prospects pricing at $300K/year
- Compare: Win rate, time to close, objections, churn (after 6-12 months)

---

## Ethics of Pricing Tests

### The Fairness Problem

**Customer perception:** "Why does my friend pay less than me?"

**Reality:** Can damage trust if discovered.

### Ethical Approaches

**1. Test with new customers only**
- Don't change prices for existing customers
- Test all new visitors

**2. Time-limited tests**
- Run test for 30-60 days only
- Then pick winner, apply to all

**3. Segment-based pricing (not random)**
- Different prices by geography (acceptable—Nordics pay more)
- Different prices by company size (acceptable—enterprise gets volume discount)
- NOT by random assignment (feels unfair)

**4. Transparent experiments**
- "Beta pricing" (openly testing)
- "Early adopter pricing" (limited time discount)

**5. Grandfather everyone to best price**
- If test shows $79 converts better than $99
- Lower price to $79 for everyone (existing + new)
- Existing customers at $99 now grandfathered at $79 (no one pays more)

### What NOT to Do (Unethical)

❌ **Dynamic pricing by willingness to pay**
- Showing higher prices to those who "look rich"
- Feels manipulative, unfair

❌ **Permanent A/B tests**
- Running forever with different customers paying different amounts
- Eventually discovered, backlash

❌ **Raising prices mid-contract**
- Customer signs at $99, you raise to $119 during their annual
- Breach of trust

---

## Tools for Pricing Experiments

### Dedicated Pricing Tools

**PriceWell** ($200-$500/month)
- Stripe integration
- A/B test prices, packages
- Automatic statistical significance

**Monetizely** ($300-$1,000/month)
- Experimentation platform
- Feature gating tests
- Revenue analytics

---

### General A/B Testing Tools

**VWO (Visual Website Optimizer)** ($200-$1,000/month)
- Test pricing page layouts
- CTA copy tests
- Heatmaps, session recordings

**Optimizely** ($50K+/year enterprise)
- Robust experimentation platform
- Multivariate testing
- Large-scale tests

**Google Optimize** (Free, basic)
- Simple A/B tests
- Good for getting started
- Limited features

---

### Analytics (Measure Results)

**Stripe Billing** (built-in)
- Tracks conversions by price
- Revenue analytics
- Churn by cohort

**Mixpanel/Amplitude** ($100-$500/month)
- User behavior analytics
- Funnel analysis
- Cohort retention

---

## Test Design Framework

### Step 1: Hypothesis

**Format:** "If we [change], then [metric] will [improve] because [reason]."

**Example:** "If we increase Pro tier from $99 to $119, then revenue will increase by 15% because higher price outweighs slight conversion drop."

---

### Step 2: Metrics

**Primary metric:** Revenue per visitor (conversion × price)

**Secondary metrics:**
- Conversion rate
- Customer quality (churn, LTV)
- Time to close
- Objections/feedback

**Guardrail metrics:**
- Customer satisfaction (NPS)
- Churn rate (don't increase churn >5%)

---

### Step 3: Test Design

**Sample size:** 250-500 per variation
**Duration:** 30-60 days
**Traffic split:** 50/50 or 80/20 (if risk-averse, 80% control, 20% variant)

---

### Step 4: Run Test

**Monitor:**
- Daily check for technical issues (tracking working?)
- Weekly check for progress toward significance
- DON'T peek and end early ("peeking problem")

---

### Step 5: Analyze Results

**Statistical significance reached?**
- Yes → Implement winner
- No → Run longer or increase traffic

**Revenue per visitor:**
- Variant A: $99 × 10% = $9.90
- Variant B: $119 × 8.5% = $10.12
- Winner: Variant B (+2% revenue)

**Qualitative:**
- What objections came up?
- Did customer quality change?
- How did sales team react?

---

### Step 6: Implement Winner

**Rollout:**
- All new customers get winning price
- Existing customers: Grandfather or migrate (see `advanced/price-increase-communication-migration.md`)

---

## Common Testing Mistakes

### Mistake 1: Sample Size Too Small

**Problem:** 50 visitors per variation → no statistical power

**Fix:** Wait for 250-500 per variation

---

### Mistake 2: Ending Test Too Early

**Problem:** Variant winning on day 3, end test → false positive

**Fix:** Run full 30-60 days, wait for significance

---

### Mistake 3: Testing Too Many Variables

**Problem:** Test price + packaging + CTA + page layout all at once → can't tell what worked

**Fix:** Test one variable at a time (or use multivariate with enough traffic)

---

### Mistake 4: Ignoring Revenue (Only Conversion)

**Problem:** $79 converts 12%, $99 converts 10% → choose $79 based on conversion alone

**Reality:** $79 × 12% = $9.48, $99 × 10% = $9.90 → $99 better for revenue

**Fix:** Always measure revenue per visitor, not just conversion

---

### Mistake 5: Not Segmenting Results

**Problem:** Overall conversion same, but SMB converts better at lower price, Enterprise at higher

**Fix:** Segment analysis by customer size, industry, geography

---

## Key Takeaways

1. **Only 24% test regularly, they outperform by 30% NRR**
2. **250-500 visitors per variation, 30-60 days minimum**
3. **Test new customers only** - Ethical, avoids fairness issues
4. **Measure revenue per visitor** - Not just conversion rate
5. **SMB = traditional A/B, Enterprise = 3-5 account tests**
6. **Grandfather to best price if lowering** - Builds trust
7. **Use dedicated tools** - PriceWell, Monetizely, VWO

## Next Steps

**Ready to launch pricing changes:**
→ Read `core/11-launching-new-pricing.md`

**Need internal alignment first:**
→ Read `core/10-internal-alignment-communication.md`

**Ready to monitor results:**
→ Read `core/12-monitoring-optimization-metrics.md`
