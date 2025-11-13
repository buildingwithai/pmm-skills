# Annual Pricing Calculator

Calculate optimal annual discounts and pricing scenarios.

## Calculator Overview

**Purpose:** Determine optimal annual discount that maximizes cash flow and retention while remaining profitable.

---

## Input Variables

### Current Pricing

**Monthly price:** $_____
**Annual price (if exists):** $_____
**Current annual discount:** _____%

**Current customer split:**
- Monthly customers: ___%
- Annual customers: ___%

---

### Customer Metrics

**Total customers:** _____
**Monthly churn rate:** _____%
**Annual churn rate:** _____%
**Average LTV:** $_____
**CAC:** $_____

---

### Financial Metrics

**Gross margin:** _____%
**Cost to serve (per customer/month):** $_____
**Cost of capital / discount rate:** _____%

---

## Scenario Analysis

### Scenario 1: Current State (Baseline)

**Monthly price:** $_____
**Annual price:** $_____ (___% discount)
**Annual adoption:** ___%

**Calculations:**

| Metric | Monthly Customers | Annual Customers | Total |
|--------|------------------|------------------|--------|
| # Customers | _____ (___%) | _____ (___%) | _____ |
| Revenue/customer/year | $_____ (× 12 months) | $_____ | — |
| Total annual revenue | $_____ | $_____ | $_____ |
| Upfront cash (Year 1) | $0 | $_____ | $_____ |
| Churn rate | ___% monthly | ___% annual | — |
| Net revenue retention | ___% | ___% | ___% |

**Cash flow (Year 1):**
- Monthly: $_____ collected over 12 months
- Annual: $_____ collected upfront
- **Total cash Year 1:** $_____

---

### Scenario 2: Increase Annual Discount

**Monthly price:** $_____ (no change)
**Annual price:** $_____ (___% discount) ← **Increased from ___%**
**Expected annual adoption:** ___% ← **Increased from ___%**

**Assumptions:**
- +5% annual discount → +10% annual adoption (benchmark)
- Annual churn = 70% of monthly churn (typical)

**Calculations:**

| Metric | Monthly Customers | Annual Customers | Total |
|--------|------------------|------------------|--------|
| # Customers | _____ (___%) | _____ (___%) | _____ |
| Revenue/customer/year | $_____ | $_____ | — |
| Total annual revenue | $_____ | $_____ | $_____ |
| Upfront cash (Year 1) | $0 | $_____ | $_____ |
| Churn rate | ___% monthly | ___% annual | — |
| Net revenue retention | ___% | ___% | ___% |

**Cash flow (Year 1):**
- Monthly: $_____
- Annual: $_____
- **Total cash Year 1:** $_____

**Comparison to Scenario 1:**
- Revenue change: +/- $_____  (+/- ___%)
- Cash flow change: +/- $_____  (+/- ___%)
- **Recommendation:** Implement / Reject

---

### Scenario 3: Decrease Annual Discount

**Monthly price:** $_____ (no change)
**Annual price:** $_____ (___% discount) ← **Decreased from ___%**
**Expected annual adoption:** ___% ← **Decreased from ___%**

**Calculations:**
[Repeat table structure from Scenario 2]

**Comparison to Scenario 1:**
- Revenue change: +/- $_____  (+/- ___%)
- Cash flow change: +/- $_____  (+/- ___%)
- **Recommendation:** Implement / Reject

---

## Annual Discount Optimization Matrix

| Discount % | Annual Price | Annual Adoption (est.) | Total Revenue | Upfront Cash | NPV | Recommendation |
|------------|--------------|------------------------|---------------|--------------|-----|----------------|
| 0% (no discount) | $_____ | ___%  | $_____ | $_____ | $_____ | — |
| 10% | $_____ | ___% | $_____ | $_____ | $_____ | — |
| 15% | $_____ | ___% | $_____ | $_____ | $_____ | — |
| 16% (2 months free) | $_____ | ___% | $_____ | $_____ | $_____ | — |
| 20% (2.4 months free) | $_____ | ___% | $_____ | $_____ | $_____ | ⭐ **Optimal** |
| 25% (3 months free) | $_____ | ___% | $_____ | $_____ | $_____ | — |
| 30% | $_____ | ___% | $_____ | $_____ | $_____ | — |

**Optimal discount:** ___%
**Rationale:** _____________________

---

## Break-Even Analysis

### What annual adoption needed to break even?

**Question:** At X% annual discount, what % of customers must choose annual to equal baseline revenue?

**Formula:**
```
Break-even adoption = (Monthly price × 12) / (Annual discounted price) × Current annual adoption
```

**Example:**
- Monthly: $99 × 12 = $1,188
- Annual at 20% discount: $950
- Current annual adoption: 30%
- Break-even: ($1,188 / $950) × 30% = 37.5% annual adoption needed

**Your calculation:**
- Monthly revenue: $_____ × 12 = $_____
- Annual revenue: $_____
- Current adoption: ___%
- **Break-even adoption: ___%**

**Feasibility:** Achievable / Unlikely (based on market benchmarks)

---

## CAC Payback Impact

### Monthly billing:

**CAC:** $_____
**Monthly MRR:** $_____
**Gross margin:** ___%

**Payback:** CAC / (MRR × Gross Margin) = _____ months

---

### Annual billing:

**CAC:** $_____
**Annual prepayment:** $_____
**Gross margin:** ___%

**Payback:** Instant (cash upfront) or $_____ / $_____ = _____ months

**Improvement:** Annual billing reduces payback by _____ months

---

## Cash Flow Projection (3 Years)

### Scenario: Current State

| Year | New Customers | Revenue (Monthly) | Revenue (Annual) | Total Revenue | Cash Collected |
|------|---------------|-------------------|------------------|---------------|----------------|
| Year 1 | _____ | $_____ | $_____ | $_____ | $_____ |
| Year 2 | _____ | $_____ | $_____ | $_____ | $_____ |
| Year 3 | _____ | $_____ | $_____ | $_____ | $_____ |
| **Total** | — | — | — | $_____ | $_____ |

---

### Scenario: Increased Annual Discount

| Year | New Customers | Revenue (Monthly) | Revenue (Annual) | Total Revenue | Cash Collected |
|------|---------------|-------------------|------------------|---------------|----------------|
| Year 1 | _____ | $_____ | $_____ | $_____ | $_____ |
| Year 2 | _____ | $_____ | $_____ | $_____ | $_____ |
| Year 3 | _____ | $_____ | $_____ | $_____ | $_____ |
| **Total** | — | — | — | $_____ | $_____ |

**3-year NPV difference:** +/- $_____

---

## Multi-Year Discount Calculator

### 1-Year Contract (Baseline)

**Price:** $_____ (___% discount vs monthly)
**Adoption:** ___%

---

### 2-Year Contract

**Price:** $_____ per year (___% discount vs monthly)
**Total 2-year:** $_____
**Additional discount vs 1-year:** ___%
**Expected adoption:** ___% (of enterprise customers)

**Value:**
- Customer: Locks in price, saves $_____
- Us: Guaranteed 2-year revenue, reduces churn

**Recommendation:** Offer / Don't Offer

---

### 3-Year Contract

**Price:** $_____ per year (___% discount vs monthly)
**Total 3-year:** $_____
**Additional discount vs 1-year:** ___%
**Expected adoption:** ___% (rare, enterprise only)

**Recommendation:** Offer / Don't Offer

---

## Messaging Comparison

### Messaging Test: Which converts better?

**Option A: Percentage discount**
```
"Save 20% with annual billing"
```
**Expected conversion:** ___%

---

**Option B: Dollar savings**
```
"Save $240/year with annual billing"
```
**Expected conversion:** ___%

---

**Option C: Months free**
```
"Get 2 months free with annual billing"
```
**Expected conversion:** ___% ← **Highest (benchmark: +18% vs Option A)**

**Recommended messaging:** Option C (months free)

---

## Customer Lifetime Value Impact

### Monthly customers:

**Monthly price:** $_____
**Average lifetime:** _____ months
**LTV:** $_____ × _____ months = $_____

---

### Annual customers:

**Annual price:** $_____
**Average lifetime:** _____ years
**LTV:** $_____ × _____ years = $_____

**LTV difference:** +/- $_____

**Insight:** Annual customers have ___% higher LTV (typical: 20-30% higher)

---

## Implementation Checklist

- [ ] Determine optimal annual discount (__%)
- [ ] Update pricing page to show annual option
- [ ] Configure billing system (Stripe, Chargebee)
- [ ] Design toggle UI (Monthly ○ ● Annual - Save X%)
- [ ] Implement "months free" messaging
- [ ] Update sales talk tracks
- [ ] Create email campaigns promoting annual
- [ ] A/B test messaging (% vs $ vs months)
- [ ] Monitor adoption rate (target: __%)
- [ ] Review quarterly, adjust if needed

---

## Monitoring Metrics

**Track monthly:**
- Annual vs monthly mix (target: ___%)
- Annual conversion rate
- Cash collected upfront
- CAC payback (monthly vs annual)

**Review quarterly:**
- LTV comparison (monthly vs annual)
- Churn rate (monthly vs annual)
- Revenue impact (actual vs projected)
- Adjust annual discount if needed

---

## Benchmarks (2024 B2B SaaS)

**Annual discount:**
- 16-20% most common (2 months free)
- 25%+ rare (erodes margin too much)

**Annual adoption:**
- 30-50% typical (target 40%+)
- 70-90% for enterprise

**Churn impact:**
- Annual customers: 20-30% lower churn vs monthly

**CAC payback:**
- Monthly: 6-12 months average
- Annual: Instant (upfront cash)

---

**Calculator owner:** ___________
**Last updated:** ___________
**Next review:** ___________ (quarterly recommended)
