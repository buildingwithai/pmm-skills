# Metrics & Optimization

**Purpose:** Track launch performance with AARRR metrics and optimize based on data.

**When to use:** From Day 1 planning through post-launch optimization (Days 61-90+).

**Output:** Analytics dashboard, performance benchmarks, and optimization roadmap.

---

## Overview

You can't optimize what you don't measure. Launch metrics fall into two categories: **vanity metrics** (impressive but meaningless) and **actionable metrics** (drive decisions).

**Key principle:** Focus on activation and retention over sign-ups. A thousand users who churned is worse than 100 who stayed.

**The AARRR framework** (Pirate Metrics) provides the structure for tracking what matters.

---

## AARRR Pirate Metrics Framework

### Overview

**AARRR = Acquisition → Activation → Retention → Referral → Revenue**

This framework, created by Dave McClure (500 Startups), focuses on the full customer lifecycle.

**Why "Pirate Metrics"?** AARRR = "Arrr!" like a pirate. Makes it memorable.

---

### 1. Acquisition: How do users find you?

**Definition:** User discovers your product and visits your website/landing page.

**Key metrics:**
- **Website visitors** (unique visitors, sessions)
- **Traffic sources** (organic, paid, referral, direct, social)
- **Top acquisition channels** (which sources drive most visitors)
- **Cost per visitor (CPV)** for paid channels

**Launch-specific acquisition metrics:**

| Metric | Day 1 | Week 1 | Month 1 |
|--------|-------|--------|---------|
| **Visitors** | 2,000-5,000 | 10,000-20,000 | 30,000-60,000 |
| **Traffic sources** | 3-5 channels | 5-8 channels | 8-12 channels |
| **Top source %** | 40-60% (PH launch day) | 25-40% (diversified) | 15-30% (organic grows) |

**Tools:**
- Google Analytics or Plausible (privacy-focused)
- UTM parameters for source tracking
- Mixpanel or Amplitude for event tracking

**Red flags:**
- ❌ Single channel dependency (>70% from one source)
- ❌ High bounce rate (>70%)
- ❌ Very low time on page (<30 seconds)

---

### 2. Activation: Do they have a great first experience?

**Definition:** User completes key actions that demonstrate they've experienced core value ("Aha moment").

**The "Aha moment"** varies by product:
- **Slack:** Team sends 2,000 messages
- **Dropbox:** User uploads first file to at least one folder
- **LinkedIn:** User makes 7 connections in 1 week
- **Canva:** User creates and exports first design

**Key metrics:**
- **Activation rate:** % of sign-ups who reach "Aha moment"
- **Time to activation:** How long from sign-up to "Aha moment"
- **Onboarding completion rate:** % who finish onboarding flow
- **Feature adoption:** % who use core features in first session

**Launch-specific activation benchmarks:**

| Product Type | Good | Great | Exceptional |
|--------------|------|-------|-------------|
| **PLG SaaS** | 25% | 40% | 60%+ |
| **Sales-led** | 60% | 75% | 85%+ |
| **Consumer** | 20% | 35% | 50%+ |
| **Developer tools** | 15% | 30% | 45%+ |

**Time to activation targets:**

| Product Type | Target | Maximum |
|--------------|--------|---------|
| **PLG SaaS** | <15 min | <1 hour |
| **Sales-led** | <1 day | <3 days |
| **Consumer** | <5 min | <15 min |
| **Developer tools** | <30 min | <2 hours |

**Activation funnel example (PLG SaaS):**

```
100 visitors → 30 sign-ups (30% conversion)
  → 18 complete onboarding (60% completion)
  → 12 reach "Aha moment" (40% activation)

Overall activation rate: 12/30 = 40%
```

**Tools:**
- Mixpanel or Amplitude for event funnels
- Hotjar or FullStory for session recordings
- Pendo or Appcues for onboarding flows

**Optimization tactics:**
1. **Shorten time to value:** Remove friction, simplify onboarding
2. **Progressive onboarding:** Don't ask for everything upfront
3. **Use product tours:** But make them skippable
4. **Show value early:** Demo data, templates, quick wins
5. **Personalize onboarding:** Different flows for different use cases

---

### 3. Retention: Do users come back?

**Definition:** Users return and continue using the product over time.

**Why retention matters most:** Acquiring a new customer costs 5-7x more than retaining an existing one. High churn kills growth.

**Key metrics:**
- **Day 1, Day 7, Day 30 retention:** % of users who return
- **Cohort retention curves:** Retention by signup cohort
- **Churn rate:** % of users who stop using product
- **Monthly Active Users (MAU) / Daily Active Users (DAU)**
- **DAU/MAU ratio:** Stickiness (how often users return)

**Launch-specific retention benchmarks:**

| Cohort | Consumer | PLG SaaS | Sales-led SaaS |
|--------|----------|----------|----------------|
| **Day 1** | 40-60% | 50-70% | 70-85% |
| **Day 7** | 20-40% | 30-50% | 60-75% |
| **Day 30** | 10-20% | 20-35% | 50-65% |
| **Day 90** | 5-10% | 15-25% | 45-60% |

**Good retention curve:** Flattens after initial drop-off (indicates product-market fit)

```
Week 1: 100 users → Week 2: 60 users → Week 3: 50 users → Week 4: 45 users → Week 8: 40 users (plateau)
```

**Bad retention curve:** Continuous steep decline (poor product-market fit)

```
Week 1: 100 users → Week 2: 50 users → Week 3: 25 users → Week 4: 12 users → Week 8: 3 users
```

**DAU/MAU stickiness benchmarks:**

| Product Type | Good | Great | Exceptional |
|--------------|------|-------|-------------|
| **Social/Communication** | 20% | 40% | 60%+ (Facebook ~50%) |
| **SaaS Tools** | 10% | 20% | 35%+ |
| **Games** | 15% | 25% | 40%+ |
| **E-commerce** | 5% | 10% | 15%+ |

**Retention tactics:**
1. **Email re-engagement:** Triggered emails for inactive users
2. **Push notifications:** (If mobile) Remind users of value
3. **In-app notifications:** Highlight new features or unused features
4. **Habit loops:** Daily/weekly use cases
5. **Value reinforcement:** Show progress, achievements, ROI

---

### 4. Referral: Do users tell others?

**Definition:** Users recommend your product to others, driving organic growth.

**Why referral matters:** Referred customers have 37% higher retention rates and 16% higher LTV (Wharton study).

**Key metrics:**
- **Net Promoter Score (NPS):** Would you recommend (0-10 scale)?
  - 9-10 = Promoters
  - 7-8 = Passives
  - 0-6 = Detractors
  - NPS = % Promoters - % Detractors
- **Viral coefficient (K-factor):** How many new users does each user bring?
  - K > 1.0 = exponential growth
  - K = 0.5-1.0 = strong viral growth
  - K < 0.5 = weak virality
- **Referral conversion rate:** % of invited users who sign up
- **Time to first referral:** How long before user invites someone

**Launch-specific referral benchmarks:**

| Metric | Good | Great | Exceptional |
|--------|------|-------|-------------|
| **NPS (Week 1)** | +20 | +40 | +60 |
| **K-factor** | 0.3 | 0.6 | 1.0+ |
| **% who refer** | 10% | 25% | 40%+ |
| **Referral conversion** | 15% | 30% | 50%+ |

**NPS benchmarks by industry (2024):**
- SaaS average: +30 to +40
- B2B software: +25 to +35
- Consumer apps: +20 to +30
- Apple: +72 (best-in-class)

**K-factor calculation:**

```
K = (# of invites sent per user) × (conversion rate of invites)

Example:
- Each user invites 5 people on average
- 20% of invites convert to sign-ups
- K = 5 × 0.20 = 1.0 (exponential growth!)
```

**Referral tactics:**
1. **Built-in sharing:** Make it easy to invite teammates or share work
2. **Referral incentives:** Give credit, discounts, or features for referrals
3. **Network effects:** Product gets better with more users (Slack, Zoom)
4. **Social proof:** Showcase customer success stories
5. **Word-of-mouth triggers:** Create moments worth talking about

**Examples:**
- **Dropbox:** 500MB free storage per referral (both sides) → 3900% growth
- **Superhuman:** $30 credit for referrer + referee
- **Notion:** Invite team members to collaborate (built-in virality)

---

### 5. Revenue: Are users paying?

**Definition:** Users convert to paying customers or generate revenue.

**Key metrics:**
- **Conversion rate (free → paid):** % of trial users who convert
- **Average Revenue Per User (ARPU):** Total revenue / # users
- **Monthly Recurring Revenue (MRR):** Predictable monthly revenue
- **Annual Recurring Revenue (ARR):** MRR × 12
- **Customer Acquisition Cost (CAC):** Total marketing + sales cost / # customers
- **Lifetime Value (LTV):** Average revenue per customer over lifetime
- **LTV:CAC ratio:** How much value vs cost to acquire
- **Payback period:** Months to recover CAC

**Launch-specific revenue benchmarks (B2B SaaS):**

| Metric | Tier 1 Week 1 | Tier 1 Month 1 | Tier 2 Week 1 |
|--------|---------------|----------------|---------------|
| **MRR** | $5K-$10K | $20K-$50K | $2K-$5K |
| **Paying customers** | 50-100 | 200-500 | 20-50 |
| **ARPU** | $50-$150 | $50-$150 | $50-$150 |
| **Free→Paid** | 5-10% | 8-15% | 10-20% (existing users) |

**SaaS financial health metrics:**

| Metric | Healthy | Warning | Danger |
|--------|---------|---------|--------|
| **LTV:CAC** | >3:1 | 2:1 to 3:1 | <2:1 |
| **CAC Payback** | <12 months | 12-18 months | >18 months |
| **Gross Margin** | >80% | 70-80% | <70% |
| **Net Revenue Retention** | >110% | 90-110% | <90% |

**Pricing model impact on metrics:**

**Freemium:**
- Free→Paid conversion: 2-5% (typical), 5-10% (good), 10%+ (great)
- Higher user volume, lower ARPU
- Example: Notion (free tier → paid plans)

**Free trial:**
- Trial→Paid conversion: 15-25% (typical), 25-40% (good), 40%+ (great)
- Lower user volume, higher ARPU
- Example: Superhuman (7-day free trial)

**No free tier:**
- Immediate revenue, lower acquisition
- Requires strong brand or sales motion
- Example: Linear ($8/user/month, no free tier)

**Revenue optimization tactics:**
1. **Pricing experiments:** Test different price points (use Price Intelligently, Paddle)
2. **Usage-based pricing:** Align cost with value (e.g., per seat, per transaction)
3. **Annual plans:** Offer 2-month discount for annual vs monthly
4. **Expansion revenue:** Upsell and cross-sell existing customers
5. **Reduce churn:** Saving a customer is easier than acquiring a new one

---

## Metrics by Launch Tier

### Tier 1 Launch Metrics (Major Product)

**Week 1 targets:**

| Metric | Minimum | Target | Stretch |
|--------|---------|--------|---------|
| **Visitors** | 5,000 | 10,000 | 20,000+ |
| **Sign-ups** | 500 | 1,000 | 2,500+ |
| **Activation rate** | 25% | 40% | 60%+ |
| **Day 7 retention** | 30% | 50% | 70%+ |
| **NPS** | +20 | +40 | +60+ |
| **MRR (B2B)** | $5K | $10K | $25K+ |
| **Paying customers** | 50 | 100 | 200+ |

**Month 1 targets:**

| Metric | Minimum | Target | Stretch |
|--------|---------|--------|---------|
| **Visitors** | 20,000 | 40,000 | 80,000+ |
| **Total sign-ups** | 2,000 | 4,000 | 8,000+ |
| **MRR** | $20K | $40K | $80K+ |
| **CAC** | <$200 | <$150 | <$100 |
| **LTV:CAC** | 2:1 | 3:1 | 5:1+ |

---

### Tier 2 Launch Metrics (Feature)

**Week 1 targets:**

| Metric | Minimum | Target | Stretch |
|--------|---------|--------|---------|
| **Feature adoption** | 10% existing users | 25% | 40%+ |
| **New sign-ups** | 100 | 300 | 500+ |
| **Expansion MRR** | $2K | $5K | $10K+ |
| **Support tickets** | <50 | <20 | <10 |
| **NPS impact** | +5 | +10 | +15+ |

---

### Tier 3 Launch Metrics (Update)

**Week 1 targets:**

| Metric | Minimum | Target | Stretch |
|--------|---------|--------|---------|
| **Adoption rate** | 5% | 15% | 30%+ |
| **Bug reports** | <20 | <10 | <5 |
| **User sentiment** | Neutral | Positive | Very positive |
| **Support tickets** | <10 | <5 | 0 |

---

## Dashboard Setup

### Essential Launch Dashboard (Week 1)

**Section 1: Acquisition**
- Total visitors (daily, cumulative)
- Traffic sources breakdown (pie chart)
- Top 5 acquisition channels
- Conversion rate (visitor → sign-up)

**Section 2: Activation**
- Total sign-ups (daily, cumulative)
- Activation rate (% reaching "Aha moment")
- Time to activation (median, 90th percentile)
- Onboarding completion rate

**Section 3: Retention**
- Day 1 retention (% who return next day)
- Day 7 retention
- Cohort retention curve
- Daily Active Users (DAU)

**Section 4: Revenue**
- MRR (daily updates)
- Paying customers (cumulative)
- Conversion rate (free → paid)
- ARPU

**Section 5: Sentiment**
- NPS score
- Support tickets (volume, avg response time)
- Social media sentiment
- Top feature requests

**Tools for dashboards:**
- **Mixpanel:** Event analytics, funnels, cohorts
- **Amplitude:** Product analytics, behavioral cohorts
- **Google Data Studio:** Free, integrates with GA
- **Mode or Looker:** SQL-based, for technical teams
- **ChartMogul:** SaaS metrics (MRR, churn, LTV)

---

## Cohort Analysis

**Definition:** Track groups of users who signed up in the same period to identify trends.

**Why cohorts matter:**
- See if retention improves over time (product improving?)
- Identify which acquisition channels bring best users
- Measure impact of product changes

**Example cohort table (retention by week):**

| Cohort | Week 0 | Week 1 | Week 2 | Week 3 | Week 4 | Week 8 |
|--------|--------|--------|--------|--------|--------|--------|
| **Jan W1** | 100% | 55% | 45% | 40% | 38% | 35% |
| **Jan W2** | 100% | 60% | 50% | 48% | 45% | 42% |
| **Jan W3** | 100% | 65% | 58% | 55% | 52% | 50% |
| **Jan W4** | 100% | 70% | 65% | 62% | 60% | 58% |

**Insight:** Retention improving week-over-week (product iterations working!)

**Cohort segmentation:**
- **By channel:** Do Product Hunt users retain better than LinkedIn Ad users?
- **By feature:** Do users who complete onboarding retain better?
- **By pricing tier:** Do annual customers churn less than monthly?

---

## PLG vs Sales-Led Metrics

### PLG-Specific Metrics

**Product Qualified Leads (PQLs):**
- Users who've reached activation + usage threshold
- Example: Used product 5+ days, invited 3+ teammates, used core feature

**PQL conversion rate:**
- % of PQLs who convert to paid
- Benchmark: 15-30%

**Time to PQL:**
- How long from sign-up to PQL status
- Target: <7 days

**Viral coefficient (K-factor):**
- Critical for PLG (aim for K > 0.5)

**Self-serve revenue:**
- % of revenue from no-touch sales
- PLG companies target 30-70%+

---

### Sales-Led Metrics

**Marketing Qualified Leads (MQLs):**
- Leads who match ICP criteria + engagement signals
- Example: VP title, 500+ employees, attended webinar

**Sales Qualified Leads (SQLs):**
- MQLs vetted by sales (real buying intent)
- Benchmark MQL→SQL: 20-40%

**Pipeline generated:**
- Total value of opportunities created
- Week 1 target: $500K-$2M pipeline (enterprise)

**Sales cycle length:**
- Time from first touch to closed-won
- Benchmark: 3-6 months (mid-market), 6-12 months (enterprise)

**Win rate:**
- % of opportunities that close
- Benchmark: 20-30% (healthy)

---

## Week 1 Metric Checkpoints

### Day 1 (Launch Day)

**6:00am check:**
- Visitors: 500-1,000
- Sign-ups: 50-100
- Activation: 25-40%

**12:00pm check:**
- Visitors: 1,500-3,000
- Sign-ups: 150-300
- Top source: Product Hunt (if launching there)

**6:00pm check:**
- Visitors: 3,000-6,000
- Sign-ups: 300-600
- MRR: $1K-$3K

**End of Day 1:**
- Visitors: 5,000-10,000
- Sign-ups: 500-1,000
- Activation: 25-40%
- MRR: $2K-$5K
- NPS: +20 to +40

---

### Day 2-3 (Sustain Momentum)

**Key question:** Did Day 1 momentum carry over?

**Metrics to watch:**
- Day 2 traffic vs Day 1 (should be 40-60% of Day 1)
- Cumulative sign-ups: 800-1,500
- Day 1 retention: 40-60% of Day 1 users return
- Support ticket volume: Manageable (<20 tickets)

---

### Day 7 (Week 1 Review)

**Full Week 1 metrics:**
- Total visitors: 10,000-20,000
- Total sign-ups: 1,000-2,500
- Activation rate: 25-40%
- Day 7 retention: 30-50%
- MRR: $5K-$10K
- Paying customers: 50-100
- NPS: +20 to +40
- CAC: <$200

**Key questions:**
1. Which channels drove most sign-ups?
2. What's the activation rate by channel?
3. Are activated users converting to paid?
4. What are top support issues?
5. What's the most-requested feature?

---

## Optimization Frameworks

### The ICE Framework (Prioritize experiments)

**ICE = Impact × Confidence × Ease**

Rate each potential optimization on scale of 1-10:
- **Impact:** How much will this improve metrics?
- **Confidence:** How confident are we it will work?
- **Ease:** How easy to implement?

**ICE Score = (Impact + Confidence + Ease) / 3**

**Example:**

| Experiment | Impact | Confidence | Ease | ICE Score | Priority |
|------------|--------|------------|------|-----------|----------|
| Add onboarding video | 8 | 7 | 9 | 8.0 | High |
| Redesign pricing page | 9 | 6 | 4 | 6.3 | Medium |
| Build referral program | 10 | 5 | 3 | 6.0 | Medium |
| Fix critical bug | 6 | 10 | 8 | 8.0 | High |

---

### The AARRR Optimization Loop

**Week 1:** Identify the biggest bottleneck in AARRR funnel

Example bottleneck analysis:
```
Acquisition: 10,000 visitors ✅ Good
  ↓
Activation: 30% sign up (3,000) → Only 20% activate (600) ❌ BOTTLENECK
  ↓
Retention: Of activated, 70% return Day 7 ✅ Good
  ↓
Referral: K-factor = 0.4 ✅ OK
  ↓
Revenue: 10% convert to paid ✅ Good
```

**Week 2-3:** Run experiments to fix bottleneck
- A/B test onboarding flows
- Add product tours
- Simplify sign-up
- Show value faster

**Week 4:** Measure improvement, move to next bottleneck

---

## A/B Testing Best Practices

**When to A/B test:**
- After Week 1 (need baseline data first)
- High-traffic pages (need statistical significance)
- High-impact changes (pricing, onboarding, messaging)

**When NOT to A/B test:**
- Low traffic (<1,000 visitors/week)
- Obvious bugs or issues (just fix them)
- Minor copy tweaks (directional testing OK)

**Sample size calculator:**
- Baseline conversion: 30%
- Minimum detectable effect: 10% relative improvement (30% → 33%)
- Confidence: 95%
- Power: 80%
- **Required sample: ~4,000 users per variant**

**Test duration:**
- Minimum 1 week (account for day-of-week effects)
- Ideal: 2-4 weeks
- Run until statistical significance reached

**Tools:**
- Optimizely or VWO (visual A/B testing)
- Google Optimize (free, basic)
- Statsig or LaunchDarkly (feature flags + experiments)
- PostHog (open-source, includes A/B testing)

---

## Red Flags & Interventions

### Red Flag 1: Low Activation (<20%)

**Diagnosis:**
- Onboarding too complex
- Value proposition unclear
- Product too buggy
- Wrong target audience

**Interventions:**
1. Watch session recordings (Hotjar, FullStory)
2. User interviews (call 5-10 users who didn't activate)
3. Simplify onboarding (remove steps)
4. Add onboarding video or product tour
5. Fix critical bugs immediately

---

### Red Flag 2: Poor Day 7 Retention (<20%)

**Diagnosis:**
- Product doesn't deliver ongoing value
- Lack of habit formation
- Better alternatives exist
- Users achieved one-time goal

**Interventions:**
1. Email re-engagement campaigns
2. Push notifications (if mobile)
3. Add daily/weekly use cases
4. Show progress or achievements
5. Improve core product value

---

### Red Flag 3: Low Conversion Rate (<5% for freemium, <15% for trial)

**Diagnosis:**
- Pricing too high
- Free plan too generous (no incentive to upgrade)
- Unclear paid tier value
- Payment friction

**Interventions:**
1. A/B test pricing
2. Limit free tier features
3. Highlight paid tier benefits
4. Add annual plan discount
5. Simplify checkout flow

---

### Red Flag 4: High CAC, Low LTV (LTV:CAC < 2:1)

**Diagnosis:**
- Paid ads too expensive
- Wrong target audience
- High churn
- Low pricing

**Interventions:**
1. Pause paid ads, focus on organic
2. Improve retention (raises LTV)
3. Increase pricing
4. Target better-fit customers
5. Build viral loops (reduce CAC)

---

## Tools Stack for Launch Metrics

### Analytics (Choose 1-2)

**Free/affordable:**
- **Google Analytics 4:** Free, full-featured, privacy concerns
- **Plausible:** $9/mo, privacy-focused, simple
- **PostHog:** Open-source, self-host or cloud

**Premium:**
- **Mixpanel:** $28+/mo, event-based, great for SaaS
- **Amplitude:** Free tier generous, scales with growth
- **Heap:** Auto-capture events, no code needed

---

### User Behavior (Choose 1)

- **Hotjar:** $32+/mo, heatmaps + session recordings
- **FullStory:** $199+/mo, powerful session replay
- **Microsoft Clarity:** Free, heatmaps + recordings

---

### A/B Testing (Choose 1)

- **Google Optimize:** Free (sunset 2023, use GA4 experiments)
- **Optimizely:** $50K+/year (enterprise)
- **VWO:** $199+/mo (mid-market)
- **Statsig:** Free tier, feature flags + experiments

---

### SaaS Metrics (Choose 1 if B2B SaaS)

- **ChartMogul:** $100+/mo, MRR, churn, cohorts
- **ProfitWell:** Free, revenue analytics
- **Baremetrics:** $50+/mo, SaaS metrics dashboard

---

### Customer Feedback

- **Typeform or Tally:** Surveys and NPS
- **Delighted:** NPS tracking
- **Canny or ProductBoard:** Feature requests
- **Intercom or Drift:** In-app chat + support

---

## Next Steps

**After Week 1 launch:**

1. **Review metrics vs targets** (use Week 1 checkpoints above)
2. **Identify biggest bottleneck** (AARRR framework)
3. **Run experiments** (ICE framework to prioritize)
4. **Iterate rapidly** (see `08-iteration-retrospective.md`)
5. **Scale what works** (double down on best channels)

**Related guides:**
- `08-iteration-retrospective.md` - Post-launch feedback loops
- `06-launch-day-playbook.md` - Real-time monitoring on launch day
- `05-multi-channel-tactics.md` - Channel-specific metrics
- `03-gtm-strategy.md` - PLG vs sales-led metrics

**Remember:** Metrics are useless without action. Measure → Learn → Iterate → Repeat.
