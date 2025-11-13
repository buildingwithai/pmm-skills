# Value Metric Selection Worksheet

Framework for choosing the right value metric for your pricing.

## What is a Value Metric?

**Definition:** The unit you charge for (per user, per API call, per GB, etc.)

**Examples:**
- Slack: Per user
- Twilio: Per API call
- Snowflake: Per compute credit
- Dropbox: Per GB storage

---

## Why Value Metric Matters

**Patrick Campbell's rule:** "8 out of 10 companies using per-user pricing should be using a different value metric."

**Impact:**
- Right metric = price scales with value delivered
- Wrong metric = leave money on table or price out customers

---

## Criteria for Good Value Metric

### 1. Correlates with Value Delivered

**Question:** As customers use more [metric], do they get more value?

**Example (Good):**
- Stripe charges per transaction → more transactions = more revenue processed = more value ✓

**Example (Bad):**
- Charging per login → more logins ≠ more value ✗

**Your product:**
Does [proposed metric] correlate with value? Yes / No
Explanation: _____________________

---

### 2. Easy to Understand

**Question:** Can customers predict their usage and costs?

**Example (Good):**
- Calendly: Per event type → "I have 3 meeting types" = easy to predict ✓

**Example (Bad):**
- Per "data point processed" → what's a data point? Hard to predict ✗

**Your product:**
Can customers easily estimate [proposed metric]? Yes / No
Explanation: _____________________

---

### 3. Grows as Customer Succeeds

**Question:** As customers grow their business, does usage of [metric] increase?

**Example (Good):**
- Mailchimp: Per subscriber → as business grows, email list grows ✓

**Example (Bad):**
- Per campaign sent → successful businesses might send fewer, better campaigns ✗

**Your product:**
Does [proposed metric] grow with customer success? Yes / No
Explanation: _____________________

---

### 4. Measurable & Attributable

**Question:** Can you accurately track [metric] per customer?

**Example (Good):**
- API calls: Each call logged with customer ID ✓

**Example (Bad):**
- "Value delivered" → subjective, unmeasurable ✗

**Your product:**
Can you measure [proposed metric] accurately? Yes / No
Technical feasibility: Easy / Medium / Hard
Explanation: _____________________

---

## Value Metric Options Analysis

### Option 1: Per User/Seat

**Description:** Charge per person with access ($X/user/month)

**When it works:**
- Collaboration tools (Slack, Notion)
- Software where value = team size
- B2B SaaS (familiar model)

**When it doesn't:**
- Single-user tools
- Value unrelated to team size
- Disincentivizes adding users (bad for viral growth)

**Your product fit:**
- Fits well: Yes / No
- Correlation with value: Low / Medium / High
- Ease of understanding: Easy / Medium / Hard
- Growth alignment: Yes / No
- Measurability: Easy / Medium / Hard

**Score:** ___/20 (4 criteria × 5 points each)

---

### Option 2: Usage-Based (Per API Call, Transaction, etc.)

**Description:** Charge per unit consumed ($X per 1,000 API calls)

**When it works:**
- APIs, infrastructure (Twilio, AWS)
- Usage directly correlates with value
- Customers want "pay for what you use"

**When it doesn't:**
- Unpredictable usage (customers fear bill shock)
- Usage doesn't correlate with value
- Hard to track/attribute

**Your product fit:**
- Fits well: Yes / No
- Correlation with value: Low / Medium / High
- Ease of understanding: Easy / Medium / Hard
- Growth alignment: Yes / No
- Measurability: Easy / Medium / Hard

**Score:** ___/20

---

### Option 3: Storage/Data Volume

**Description:** Charge per GB stored or processed

**When it works:**
- Storage products (Dropbox, Box)
- Data processing (Snowflake, Databricks)
- Value = data managed

**When it doesn't:**
- Storage is cheap (not meaningful differentiator)
- Value unrelated to data volume

**Your product fit:**
- Fits well: Yes / No
- Correlation with value: Low / Medium / High
- Ease of understanding: Easy / Medium / Hard
- Growth alignment: Yes / No
- Measurability: Easy / Medium / Hard

**Score:** ___/20

---

### Option 4: Feature-Based (Flat-Rate Tiers)

**Description:** Charge based on features included, not usage ($X/month for Tier 1)

**When it works:**
- Defined customer segments (SMB, enterprise)
- Usage relatively flat across customers
- Want simplicity (no metering needed)

**When it doesn't:**
- High variance in usage (10x difference between customers)
- Power users subsidized by light users

**Your product fit:**
- Fits well: Yes / No
- Correlation with value: Low / Medium / High
- Ease of understanding: Easy / Medium / Hard
- Growth alignment: Yes / No
- Measurability: Easy / Medium / Hard

**Score:** ___/20

---

### Option 5: Outcome-Based

**Description:** Charge based on result delivered ($X per report generated, per lead qualified)

**When it works:**
- Clear, measurable outcome
- Value = outcome achieved
- Premium positioning

**When it doesn't:**
- Outcome hard to define/measure
- Multiple factors affect outcome (not just your product)

**Your product fit:**
- Fits well: Yes / No
- Correlation with value: Low / Medium / High
- Ease of understanding: Easy / Medium / Hard
- Growth alignment: Yes / No
- Measurability: Easy / Medium / Hard

**Score:** ___/20

---

### Option 6: Hybrid (Subscription + Usage)

**Description:** Base fee + usage overage ($X/month + $Y per unit beyond cap)

**When it works:**
- Best of both worlds (predictable + scalable)
- Variable usage between customers
- Want expansion revenue + stable base

**When it doesn't:**
- Complexity (two components to explain)
- Harder to implement (metering + subscription)

**Your product fit:**
- Fits well: Yes / No
- Correlation with value: Low / Medium / High
- Ease of understanding: Easy / Medium / Hard
- Growth alignment: Yes / No
- Measurability: Easy / Medium / Hard

**Score:** ___/20

---

## Value Metric Comparison

| Option | Correlation | Ease | Growth | Measurable | Total Score | Rank |
|--------|-------------|------|--------|------------|-------------|------|
| Per User | ___/5 | ___/5 | ___/5 | ___/5 | ___/20 | ___ |
| Usage-Based | ___/5 | ___/5 | ___/5 | ___/5 | ___/20 | ___ |
| Storage/Data | ___/5 | ___/5 | ___/5 | ___/5 | ___/20 | ___ |
| Feature-Based | ___/5 | ___/5 | ___/5 | ___/5 | ___/20 | ___ |
| Outcome-Based | ___/5 | ___/5 | ___/5 | ___/5 | ___/20 | ___ |
| Hybrid | ___/5 | ___/5 | ___/5 | ___/5 | ___/20 | ___ |

**Top 2 options:**
1. ___________________ (Score: ___/20)
2. ___________________ (Score: ___/20)

---

## Competitive Analysis

### What do competitors use?

| Competitor | Value Metric | Rationale |
|------------|--------------|-----------|
| Competitor 1 | _____________ | _____________ |
| Competitor 2 | _____________ | _____________ |
| Competitor 3 | _____________ | _____________ |

**Market norm:** _____________ (most common metric in your category)

**Implication:**
- [ ] Follow market norm (familiar to customers)
- [ ] Differentiate with different metric (competitive advantage)

---

## Customer Validation

### Interview customers:

**Question 1:** "If you could choose how to pay for [Product], what would feel most fair?"
- Customer A: _____________________
- Customer B: _____________________
- Customer C: _____________________

**Question 2:** "Between [Option A] and [Option B], which makes more sense?"
- Customer A: _____________________
- Customer B: _____________________
- Customer C: _____________________

**Pattern:** ___% prefer [Option], ___% prefer [Option]

---

## Financial Modeling

### Estimate revenue per customer under each model:

| Metric | Avg Usage | Price | Revenue/Customer/Year |
|--------|-----------|-------|-----------------------|
| Per user | ___ users | $___ | $___ |
| Usage-based | ___ units | $___ | $___ |
| Feature-based | — | $___ | $___ |
| Hybrid | ___ + ___ | $___ + $___ | $___ |

**Highest revenue potential:** _________________

**Note:** Don't optimize purely for revenue (consider alignment with value)

---

## Implementation Complexity

### Technical effort required:

| Metric | Metering Required | Billing Integration | Dev Effort | Timeline |
|--------|------------------|---------------------|------------|----------|
| Per user | Low (count seats) | Simple | Low (1-2 weeks) | _____ |
| Usage-based | High (log every call) | Complex | High (4-8 weeks) | _____ |
| Feature-based | None (tier-based) | Simple | Low (1-2 weeks) | _____ |
| Hybrid | Medium | Complex | Medium (3-6 weeks) | _____ |

**Consideration:** Balance ideal metric vs implementation effort

---

## Decision Matrix

### Criteria Weighting

| Criterion | Weight | Option 1: _____ | Option 2: _____ | Option 3: _____ |
|-----------|--------|----------------|----------------|----------------|
| Correlation with value | 40% | ___ × 0.4 = ___ | ___ × 0.4 = ___ | ___ × 0.4 = ___ |
| Easy to understand | 25% | ___ × 0.25 = ___ | ___ × 0.25 = ___ | ___ × 0.25 = ___ |
| Grows with customer | 20% | ___ × 0.2 = ___ | ___ × 0.2 = ___ | ___ × 0.2 = ___ |
| Measurable | 15% | ___ × 0.15 = ___ | ___ × 0.15 = ___ | ___ × 0.15 = ___ |
| **Total** | 100% | **___** | **___** | **___** |

**Winner:** _____________________ (Highest weighted score)

---

## Recommendation

**Selected value metric:** _____________________

**Rationale:**
- Correlates with value because: _____________________
- Easy for customers to understand: _____________________
- Grows as customers succeed: _____________________
- Technically feasible: _____________________

**Alternative considered:** _____________________
**Why rejected:** _____________________

---

## Testing Plan

**Hypothesis:** "[Chosen metric] will resonate with customers and drive [X]% higher conversion vs [current metric]"

**Test approach:**
- [ ] Interview 10-15 customers on preferred metric
- [ ] A/B test pricing page (metric A vs metric B)
- [ ] Pilot with 50 customers (new metric)
- [ ] Monitor: Conversion, ARPU, NPS

**Success criteria:**
- Conversion rate: ___% (target)
- ARPU: $_____ (target)
- Customer feedback: Positive (qualitative)

**Timeline:** _____________________

---

## Iteration Plan

**Review after:**
- 90 days: Conversion, ARPU, feedback
- 6 months: LTV, churn, expansion revenue
- 12 months: Full evaluation

**Potential pivots:**
- If [metric] doesn't correlate with value → Switch to [alternative]
- If customers confused → Simplify or change metric
- If usage unpredictable → Move to hybrid or flat-rate

---

**Worksheet owner:** ___________
**Completed date:** ___________
**Next review:** ___________ (recommended: annually)
