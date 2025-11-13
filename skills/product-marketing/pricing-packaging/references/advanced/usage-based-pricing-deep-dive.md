# Usage-Based Pricing: Deep Dive

Implement consumption-based pricing for scalable growth.

## Overview

**Definition:** Pricing based on actual product usage (API calls, seats, storage, transactions, etc.) rather than fixed subscriptions.

**2024-2025 data:**
- 56% of SaaS companies have usage/consumption elements (up 31% since 2023)
- 77% of largest software companies use usage-based models (2025 State of UBP report)
- Hybrid models (subscription + usage) show 38% higher NRR than pure subscription

**Why now:** Product analytics make metering possible, customers demand "pay for what you use."

## When to Use Usage-Based Pricing

### ✅ Good Fit

**1. Usage correlates with value**
- More API calls = more value delivered
- More storage = more data managed
- More transactions = more revenue processed

**Example:** Stripe (charges per transaction), Twilio (per API call), AWS (per compute hour)

**2. Usage is measurable and attributable**
- Can track usage per customer accurately
- Clear metering infrastructure
- No disputes about "what counts"

**3. Customers have variable usage**
- Some customers use 10x more than others
- Usage grows as customer grows
- Captures value from power users

**4. Low barrier to entry needed**
- Free tier or low base price
- "Try before you commit" model
- PLG motion

---

### ❌ Poor Fit

**1. Usage doesn't correlate with value**
- Example: Project management tool charging per task created (doesn't reflect value)
- Better: Charge per user or team size

**2. Unpredictable costs scare customers away**
- "Bill shock" anxiety
- Enterprise buyers need predictable budgets
- CFOs hate variable line items

**Mitigation:** Hybrid model (base subscription + usage cap)

**3. Can't accurately meter usage**
- Technical limitations
- Attribution problems (who used what?)
- High dispute rates

**4. Flat usage patterns**
- All customers use roughly the same amount
- No power users vs casual users
- Better: Simple tier structure

---

## Pure Usage-Based Models

### How It Works

**Pricing formula:** Cost = (Units Used × Price per Unit)

**Example: Twilio (SMS API)**
- $0.0075 per SMS sent
- No base fee
- Pay only for what you send

**Example: AWS (compute)**
- $0.023 per hour per EC2 instance
- Thousands of pricing SKUs
- Pure consumption

---

### Advantages

1. **Aligns price with value** - Heavy users pay more, light users pay less
2. **Lowers barrier to entry** - Start free or cheap, scale up
3. **Automatic expansion revenue** - As usage grows, revenue grows (no upsell needed)
4. **Attracts PLG buyers** - "Try it" without commitment

---

### Disadvantages

1. **Revenue unpredictability** - Hard to forecast MRR/ARR
2. **Customer anxiety** - "What will my bill be?"
3. **Complex billing** - Metering, aggregation, invoicing infrastructure
4. **Churn from bill shock** - Unexpected $10K bill → cancel
5. **Lower ACV initially** - Small customers pay very little

---

## Hybrid Models (Subscription + Usage)

### Structure

**Base subscription** + **Usage overage**

**Example: Datadog (monitoring)**
- Base: $15/host/month (subscription)
- Overage: Custom metrics at $0.05/metric (usage)

**Example: Segment (CDP)**
- Base: $120/month (includes 10K events)
- Overage: $0.001 per additional event

---

### Why Hybrid Wins

**2024 data:** Hybrid models have 38% higher NRR than pure subscription or pure usage.

**Reasons:**
1. **Predictable base revenue** (subscription) + **expansion upside** (usage)
2. **Reduces customer anxiety** - Base price is predictable, overages are optional/controlled
3. **Captures power users** - Heavy users pay proportionally more
4. **Easier forecasting** - Base MRR/ARR + usage growth trends

---

### Hybrid Model Types

**Type 1: Base + Overage**
- Subscription includes X units
- Pay per additional unit beyond cap
- Example: $99/month (includes 100K API calls), $0.001 per call beyond

**Type 2: Base + À la Carte**
- Subscription for core features
- Usage-based pricing for premium features
- Example: $149/month (core platform), $0.05 per AI analysis run

**Type 3: Seat + Usage**
- Per-user subscription
- Plus usage-based add-ons
- Example: $20/user/month + $0.10 per report generated

---

## Implementing Usage-Based Pricing

### Step 1: Choose Usage Metric

**Criteria:**
1. **Correlates with value** - More usage = more value
2. **Easy to understand** - Customer can predict usage
3. **Measurable** - Can track accurately
4. **Grows with customer** - As they succeed, usage increases

**Common metrics:**
- **API calls** (Twilio, Stripe)
- **Data processed** (Snowflake: per TB)
- **Transactions** (payment processors: per transaction)
- **Active users** (MAU-based: per active user/month)
- **Compute time** (AWS: per compute hour)
- **Storage** (Dropbox: per GB)

**Patrick Campbell:** "The best value metric is one that grows as your customer's business grows."

---

### Step 2: Set Unit Price

**Approach: Value-based pricing**

**Steps:**
1. **Understand value delivered per unit**
   - Example: Stripe processes $100 transaction, customer makes $20 profit → willing to pay up to $5 (25% of profit)
   - Stripe charges 2.9% ($2.90) → good margin, attractive to customer

2. **Benchmark competitors**
   - What do similar products charge per unit?
   - Twilio SMS: $0.0075/SMS, competitors $0.006-0.01 → competitive range

3. **Test with early customers**
   - Offer pilot pricing to 5-10 customers
   - Measure adoption, feedback, churn

4. **Model revenue impact**
   - If average customer uses 50K units/month at $0.001/unit → $50 ARPU
   - Too low? Raise unit price or add base fee

---

### Step 3: Build Metering Infrastructure

**Technical requirements:**

**1. Usage tracking**
- Instrument product to log every billable event
- Example: Log every API call with customer_id, timestamp, endpoint

**2. Aggregation**
- Sum usage per customer per billing period
- Example: Customer A made 127,453 API calls in January

**3. Billing integration**
- Send usage data to billing system (Stripe, Chargebee, Metronome)
- Generate invoice based on usage

**4. Customer visibility**
- In-app dashboard showing current usage
- Alerts when approaching caps
- Historical usage trends

**Tools:**
- **Metronome** (usage-based billing platform, $500-$2K/month)
- **Stripe Billing** (built-in usage metering)
- **Chargebee** (hybrid subscription + usage)
- **Lago** (open-source usage billing)

---

### Step 4: Design Billing UX

**Customer needs:**
1. **Predict costs** - "What will I pay this month?"
2. **Control costs** - "How do I avoid surprises?"
3. **Understand usage** - "Where is usage coming from?"

**UX elements:**

**1. Usage dashboard**
- Current usage (real-time or daily)
- Usage trend (graph over time)
- Projected bill based on current usage
- Example: "You've used 45K API calls this month (90% of plan). Projected bill: $99."

**2. Usage alerts**
- 50% threshold: "You've reached 50% of your plan"
- 80% threshold: "You're approaching your limit"
- 100% threshold: "You've exceeded your plan. Overages apply."

**3. Cost controls (enterprise)**
- Hard caps: "Stop service at $10K/month" (prevent runaway costs)
- Soft caps: "Alert me at $5K, but allow overages"
- Spend approvals: "Require approval for >$10K"

---

## Overcoming "Usage Anxiety"

### Problem

**Customer fear:** "I don't know what I'll pay. What if I get a surprise $50K bill?"

**Impact:** 34% of buyers cite cost unpredictability as #1 concern with usage-based pricing (2024 OpenView)

---

### Solution 1: Committed Use Discounts

**Model:** Commit to $X/month, get discount on unit price

**Example: Snowflake**
- Pay-as-you-go: $40/credit
- Commit to $5K/month: $32/credit (20% discount)
- Commit to $50K/month: $28/credit (30% discount)

**Benefits:**
- Customer gets predictable spend + discount
- You get committed revenue
- Win-win

---

### Solution 2: Hybrid with Generous Base

**Model:** High base subscription that includes substantial usage

**Example:**
- Base: $500/month (includes 1M API calls)
- Overage: $0.0005 per additional call
- Most customers stay within 1M → predictable $500/month
- Power users pay more → expansion revenue

---

### Solution 3: Usage Insurance

**Model:** Optional "cap" add-on

**Example:**
- Standard: $99/month + usage overages
- Plus "Unlimited" add-on: $299/month (no overages, unlimited usage)

**Customer choice:**
- Predictable usage → stay on standard
- Unpredictable or high usage → buy unlimited

---

### Solution 4: Transparent Cost Calculators

**On pricing page:**
- Slider: "How many API calls per month?"
- Output: "Estimated cost: $247/month"
- Breakdown showing base + usage + discounts

**Reduces anxiety:** Customer can estimate costs before buying

See `core/08-pricing-page-design.md` for calculator design.

---

## Pricing Tiers for Usage-Based

### Tier Structure

**Good/Better/Best with usage caps:**

**Example: Sendgrid (email API)**

| Tier       | Base Price | Emails Included | Overage     |
|------------|------------|-----------------|-------------|
| Free       | $0         | 100/day         | N/A         |
| Essentials | $19.95/mo  | 50K/month       | $0.0008 each|
| Pro        | $89.95/mo  | 1.5M/month      | $0.0006 each|
| Premier    | Custom     | Custom          | Custom      |

**Why it works:**
- Low barrier (free tier)
- Predictable base price
- Overage pricing for power users
- Enterprise custom for highest usage

---

## Usage-Based Metrics to Track

### 1. Usage Growth Rate

**Formula:** (Current Month Usage - Previous Month Usage) / Previous Month Usage × 100

**Example:**
- January: Average customer used 50K API calls
- February: Average customer used 60K API calls
- Growth: (60K - 50K) / 50K × 100 = 20% MoM growth

**Target:** 10-20% MoM usage growth (indicates customer success)

**If flat or declining:** Customer not getting value (churn risk)

---

### 2. Revenue per Unit

**Formula:** Total Revenue / Total Units Consumed

**Example:**
- Total revenue: $100K
- Total API calls: 500M
- Revenue per unit: $100K / 500M = $0.0002 per call

**Track over time:** Should increase as you raise prices or customers upgrade

---

### 3. Usage Distribution (Power Users)

**Measure:** % of revenue from top 10% of users

**Example:**
- Top 10% of customers account for 60% of usage revenue
- Insight: Power users are key to revenue (focus retention here)

**Application:** Custom pricing, white-glove support for power users

---

### 4. Usage Efficiency (LTV:CAC by usage cohort)

**Segment customers by usage:**
- Low usage (<10K units): LTV $500, CAC $400 → LTV:CAC 1.25:1 (bad)
- Medium usage (10-100K): LTV $3K, CAC $600 → LTV:CAC 5:1 (good)
- High usage (>100K): LTV $15K, CAC $1K → LTV:CAC 15:1 (excellent)

**Insight:** Target medium-high usage customers in acquisition

---

## Common Mistakes

### Mistake 1: No Base Fee (Pure Usage)

**Problem:** Small customers pay $2/month, not worth CAC

**Fix:** Add base subscription ($50-100/month minimum)

---

### Mistake 2: Usage Doesn't Correlate with Value

**Example:** Charge per "file upload" when value is "storage managed"

**Fix:** Align usage metric to value delivered

---

### Mistake 3: No Usage Visibility

**Problem:** Customer doesn't see usage until bill arrives (shock)

**Fix:** In-app dashboard, alerts at 50%/80%/100%

---

### Mistake 4: Overage Pricing Too High

**Example:** $99 base, but $5/unit overage (10x base unit price)

**Impact:** Customers hit cap, stop using product (avoid overage), churn

**Fix:** Overages should be 1-2x base unit price, not 10x

---

## Case Studies

### Snowflake (Pure Usage-Based)

**Model:** Pay per compute + storage consumed

**Results:**
- $2.7B ARR (2024)
- 171% NRR (2023)
- Customers increase usage 2-3x year-over-year

**Why it works:**
- Usage correlates perfectly with value (more queries = more insights)
- Transparent cost calculator
- Committed use discounts reduce anxiety

---

### Datadog (Hybrid)

**Model:** $15/host/month base + usage-based add-ons

**Results:**
- $2.1B ARR (2024)
- 130% NRR (2023)
- Average customer spends $50K/year (starts at $180)

**Why it works:**
- Predictable base ($15/host)
- Expansion through usage (custom metrics, logs, traces)
- Customers "land and expand" naturally

---

### Twilio (Pure Usage-Based)

**Model:** Pay per API call (SMS, voice, video)

**Results:**
- $4B ARR (2024)
- 140% NRR (historically)
- Powers Uber, Airbnb, DoorDash

**Challenges:**
- Revenue volatility (customer usage fluctuates)
- Intense competition (price pressure)

**Adaptation:** Added "Twilio Flex" (subscription CCaaS) to stabilize revenue

---

## Key Takeaways

1. **56% of SaaS use usage-based elements** - Growing trend (2024)
2. **Hybrid = 38% higher NRR** - Subscription + usage wins
3. **Usage anxiety is real** - 34% cite cost unpredictability as concern
4. **Mitigation:** Committed use discounts, generous base, usage insurance
5. **Usage dashboard critical** - Real-time visibility prevents bill shock
6. **Align metric to value** - Patrick Campbell's rule
7. **Track usage growth** - 10-20% MoM = healthy

## Next Steps

**Implement usage-based pricing:**
→ Read `core/05-selecting-value-metrics.md`

**Design pricing page with calculator:**
→ Read `core/08-pricing-page-design.md`

**Monitor usage metrics:**
→ Read `core/12-monitoring-optimization-metrics.md`
