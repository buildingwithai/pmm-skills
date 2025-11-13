# Choosing Your Pricing Model

Select the pricing model that aligns with how customers consume and perceive value.

## Overview

**Pricing model:** The structure for how you charge (subscription vs usage vs freemium vs hybrid).

**Why it matters:** Your pricing model affects:
- Customer acquisition (freemium vs paid trial)
- Revenue predictability (subscription vs usage)
- Usage patterns (per-user discourages adoption)
- Expansion revenue (usage-based scales automatically)

**2024 trends:**
- **56% have consumption elements** (+31% since 2023)
- **Pure subscription declined** from 65% to 43%
- **Hybrid models** (subscription + usage) = 38% higher NRR
- **Freemium** = 42% of SaaS (PLG influence)

## The Five Core Pricing Models

### Model 1: Flat-Rate Subscription

**What it is:** Single price, unlimited usage

**Example:** Basecamp ($299/month, unlimited users, projects, storage)

**When it works:**
- ✅ Simple product, easy to understand value
- ✅ Want to encourage adoption (no usage anxiety)
- ✅ Can't easily meter usage
- ✅ Small customer base willing to pay premium for simplicity

**Pros:**
- Dead simple (no confusion)
- Encourages full product adoption
- No billing complexity
- Predictable revenue

**Cons:**
- Leaves money on table (large vs small customers pay same)
- Hard to justify premium price
- No built-in expansion (can't grow ACV)

**Who uses it:** Basecamp, Netflix (consumer), Superhuman ($30/month per user, unlimited)

**2024 prevalence:** ~8% of B2B SaaS (declining)

---

### Model 2: Tiered Subscription (Good/Better/Best)

**What it is:** Multiple tiers, features/limits differentiate pricing

**Example:** HubSpot (Starter $45, Professional $800, Enterprise $3,600)

**When it works:**
- ✅ Clear customer segments (SMB, mid-market, enterprise)
- ✅ Can gate valuable features by tier
- ✅ Want to serve multiple markets
- ✅ Predictable revenue needed

**Tier structure:**
- **2 tiers:** Simple but limiting (startup vs enterprise)
- **3 tiers:** Optimal (Good/Better/Best) - 60%+ of SaaS use this
- **4 tiers:** Maximum before confusion (Free/Starter/Pro/Enterprise)
- **5+ tiers:** Decision paralysis (avoid)

**Common tier names:**
- Free/Starter/Pro/Business/Enterprise
- Basic/Professional/Advanced/Enterprise
- Individual/Team/Business/Enterprise

**What differentiates tiers:**
- Feature access (basic vs advanced capabilities)
- Usage limits (users, contacts, API calls, storage)
- Support level (email → phone → dedicated CSM)
- SLAs and uptime guarantees
- Integrations and API access
- Admin controls (SSO, SAML, audit logs)

**Pros:**
- Serves multiple segments
- Clear upgrade path
- Middle tier converts 60-70% (anchor effect)
- Predictable revenue

**Cons:**
- Doesn't scale with customer success
- User limits discourage adoption
- Tier complexity can confuse

**Who uses it:** HubSpot, Salesforce, Slack (old model), Notion, Airtable

**2024 prevalence:** ~65% of B2B SaaS (most common)

See `core/06-packaging-tier-design.md` for detailed tier design.

---

### Model 3: Per-User/Seat-Based Pricing

**What it is:** Price × number of users/seats

**Example:** Slack pre-2024 ($8/user/month), Salesforce ($25-$325/user/month)

**When it works:**
- ✅ Value scales with team size
- ✅ Collaborative products (each user gets value)
- ✅ Easy to understand and meter
- ✅ Built-in expansion (teams grow = revenue grows)

**Value metrics:**
- Users (most common)
- Seats (named users)
- Licenses (concurrent vs named)

**Pros:**
- Simple to understand
- Expansion built in (add users = add revenue)
- Aligns to team growth

**Cons:**
- **Discourages adoption** (teams avoid adding users to save money)
- **Misaligned incentives** (you want adoption, they want fewer users)
- **Easy to game** (shared logins, role accounts)
- **Patrick Campbell's warning:** "8/10 using per-user should use different metric"

**When per-user is RIGHT:**
- **Collaboration tools:** Slack, Notion, Figma (each user gets full value)
- **Seat-dependent value:** CRM (each sales rep needs own seat)
- **User-specific data:** Email tools (each user has own account)

**When per-user is WRONG:**
- **Outcome-focused:** Marketing automation (value = leads, not users)
- **API/infrastructure:** Value = API calls, not who makes them
- **Analytics:** Value = insights, not number of viewers

**2024 trend:** Declining (40% in 2024 vs 55% in 2021) as companies move to usage/outcome-based

**Alternatives to per-user:**
- Slack 2024: Moved to per-active-user (only charge for users who use it)
- Calendly: Per-event-type (charge for outcomes, not users)
- Segment: Per-monthly-tracked-users (usage-based, not seats)

---

### Model 4: Usage-Based Pricing (Consumption)

**What it is:** Pay for what you use (API calls, compute, storage, events)

**Examples:**
- AWS ($0.10/GB data transfer)
- Snowflake ($2-$4 per compute-hour)
- Twilio ($0.0075 per SMS)
- OpenAI ($0.03 per 1K tokens)

**When it works:**
- ✅ Variable usage patterns (some use 10x more than others)
- ✅ Usage correlates directly to value
- ✅ Infrastructure/API products (easy to meter)
- ✅ AI products (model costs variable)
- ✅ PLG motion (eliminate usage anxiety at start)

**Common value metrics:**
- **API calls:** Twilio, Stripe, OpenAI
- **Compute time:** AWS, Snowflake, Databricks
- **Storage:** S3, Dropbox Business
- **Events/actions:** Segment, Amplitude
- **Users tracked:** Mixpanel, Heap

**Pros:**
- **Aligns perfectly to value** (use more = pay more)
- **Expansion built-in** (usage grows = revenue grows)
- **Fair to customers** (small users pay less)
- **38% higher NRR** than pure subscription (2024 data)

**Cons:**
- **Unpredictable revenue** (usage fluctuates)
- **Customer budget uncertainty** (hard to forecast spend)
- **Usage anxiety** (customers afraid to use product)
- **Billing complexity** (metering, invoicing, edge cases)

**2024 surge:**
- 77% of largest software companies use consumption pricing
- 78% adopted UBP in last 5 years
- 50% of UBP adopters added it in last 2 years (accelerating)
- AI spending +75.2% YoY driving UBP adoption

**How to overcome usage anxiety:**
- **Caps/limits:** "Your bill will never exceed $X"
- **Alerts:** "You're at 80% of your budget"
- **Calculators:** Let customers estimate costs upfront
- **Free tier:** Generous free allowance (Twilio: $15 free credit)
- **Prepaid credits:** Buy $1,000 credits, use over time

See `advanced/usage-based-pricing-deep-dive.md` for implementation details.

---

### Model 5: Hybrid (Subscription + Usage)

**What it is:** Base subscription fee + usage overages

**Examples:**
- MongoDB: Base platform fee + consumption charges
- Datadog: $15/host/month + $5/million custom metrics
- Stripe: 2.9% + $0.30 per transaction (pure usage, but acts like hybrid with minimum)

**When it works:**
- ✅ Need revenue predictability (base fee)
- ✅ Usage varies widely (usage component)
- ✅ Want to capture expansion (usage overages)
- ✅ Serve both small and large customers

**Common structures:**

**A) Base + Overages:**
- $99/month base (includes 1,000 API calls)
- $0.05 per API call beyond 1,000

**B) Base + Add-Ons:**
- $199/month (core features)
- +$50/month (advanced analytics)
- +$100/month (API access)

**C) Tiered Base + Usage:**
- Starter: $49/month + $0.10 per event
- Pro: $199/month + $0.05 per event (cheaper usage)
- Enterprise: $999/month + $0.01 per event (cheapest usage)

**Pros:**
- **Best of both worlds:** Predictability + expansion
- **38% higher NRR** than pure subscription (2024 data)
- **Serves wide range** (small customers pay less, large pay more)
- **Aligns to value** (base = access, usage = value consumed)

**Cons:**
- More complex to explain
- Requires metering infrastructure
- Potential for bill shock if not managed

**2024 trend:** Fastest-growing model (23% of SaaS have hybrid, up from 12% in 2022)

**Best practices:**
- Keep base fee reasonable (covers your costs)
- Make usage pricing transparent (calculator, examples)
- Offer usage-based discounts in higher tiers
- Provide usage alerts and caps

---

## Emerging Model: Freemium

**What it is:** Free tier + paid upgrades

**Examples:**
- Slack: Free (10K messages) → $8/user/month
- Notion: Free (individual) → $10/user/month (team)
- Calendly: Free (1 event type) → $10/user/month

**When it works:**
- ✅ Product-led growth (PLG) strategy
- ✅ Viral/network effects (Slack, Zoom)
- ✅ Low marginal cost (SaaS, not high support)
- ✅ Can monetize 2-5% of free users (enough to cover costs)

**Free tier strategies:**

**A) Feature-gated:**
- Free: Basic features only
- Paid: Advanced features unlocked
- Example: Figma (free = 3 projects, paid = unlimited + advanced features)

**B) Usage-gated:**
- Free: Limited usage (API calls, storage, users)
- Paid: Higher or unlimited usage
- Example: Mailchimp (free = 500 contacts, paid = unlimited)

**C) Time-gated (Free Trial, not true freemium):**
- Free: 14-day trial, all features
- Paid: Continued access
- Note: This is trial, not freemium (freemium = free forever)

**Conversion rates:**
- **Self-serve freemium:** 2-5% average, 6-8% top performers
- **Sales-assisted freemium:** 10-15% top performers
- **Product-led sales (PLS):** Layer sales on top of freemium for larger accounts

**Pros:**
- Viral growth (word-of-mouth)
- Low CAC (product sells itself)
- Try before buy (reduces risk)

**Cons:**
- **Strain on resources** (support costs for free users)
- **Cannibalization** (some paid users downgrade to free)
- **Slow payback** (2-5% conversion = long CAC payback)

See `advanced/freemium-free-trial-strategies.md` for optimization tactics.

---

## Pricing Model Decision Framework

**Use this flowchart to choose:**

### Start: What type of product are you?

**→ Infrastructure/API product?**
- Consider: **Usage-based** or **Hybrid**
- Examples: AWS, Stripe, Twilio, OpenAI

**→ Collaboration/productivity tool?**
- Consider: **Per-user** (if truly collaborative) or **Freemium**
- Examples: Slack, Notion, Figma

**→ Analytics/data product?**
- Consider: **Usage-based** (events tracked) or **Tiered** (by data volume)
- Examples: Segment, Snowflake, Databricks

**→ Vertical SaaS (industry-specific)?**
- Consider: **Tiered** (by company size) or **Hybrid**
- Examples: Toast (restaurants), Veeva (pharma)

**→ Developer tools?**
- Consider: **Freemium** (generous free tier) + **Usage** or **Tiered**
- Examples: GitHub, Vercel, Auth0

---

### Customer Usage Patterns

**→ Usage varies 10x+ between customers?**
- Choose: **Usage-based** or **Hybrid**
- Reason: Fair pricing, captures expansion

**→ Usage relatively consistent?**
- Choose: **Tiered subscription**
- Reason: Predictability for both you and customer

---

### Value Delivery

**→ Value directly tied to usage (more use = more value)?**
- Choose: **Usage-based**
- Examples: More API calls = more value, More storage = more value

**→ Value from access (value doesn't scale with usage)?**
- Choose: **Subscription**
- Examples: Notion (value = access to tool, not how much you write)

---

### Business Model Needs

**→ Need predictable revenue (investors, forecasting)?**
- Choose: **Subscription** or **Hybrid** (base fee provides floor)

**→ Can tolerate variable revenue for higher expansion?**
- Choose: **Usage-based**
- Trade-off: Less predictable month-to-month, but higher NRR

---

### Go-To-Market Motion

**→ Product-led growth (PLG), viral, low-touch?**
- Choose: **Freemium** → **Usage** or **Tiered**

**→ Sales-led, enterprise?**
- Choose: **Tiered** with custom enterprise tier

---

## Pricing Model Comparison Table

| Model | Revenue Predictability | Expansion Potential | Complexity | Best For |
|-------|----------------------|-------------------|------------|----------|
| **Flat-rate** | High | Low | Very Low | Simple products, want adoption |
| **Tiered** | High | Medium | Low | Multiple segments, feature gating |
| **Per-user** | High | Medium | Low | Collaboration tools (if aligned to value) |
| **Usage-based** | Low | High | High | Variable usage, infrastructure, AI |
| **Hybrid** | Medium | High | Medium | Predictability + expansion |
| **Freemium** | Low (initially) | Medium | Medium | PLG, viral products |

---

## 2024 Pricing Model Trends

### 1. Subscription → Hybrid Shift

**Before:** Pure subscription (90% of SaaS in 2018)
**Now:** 56% have some consumption element, 23% fully hybrid

**Why:** Captures expansion better, aligns to value

---

### 2. AI Driving Usage-Based

**AI product characteristics:**
- Variable compute costs (model inference)
- Outcome-based value (answers, content created)
- Unpredictable usage patterns

**Result:** AI products priced per-token, per-query, per-output

**Examples:**
- OpenAI: $0.03 per 1K tokens (GPT-4)
- Anthropic Claude: $8 per 1M input tokens
- GitHub Copilot: $10/user/month (subscription) or $0.06 per suggestion (usage)

---

### 3. Freemium Mainstream

**2020:** 25% of SaaS offered freemium
**2024:** 42% offer freemium (PLG influence)

**Drivers:** Product-led growth, lower CAC, try-before-buy expectations

---

### 4. Per-User Declining

**2021:** 55% used per-user as primary metric
**2024:** 40% use per-user

**Why:** Misaligned incentives, discourages adoption, better metrics available

---

## Common Model Selection Mistakes

### Mistake 1: Defaulting to Per-User Without Thinking

**Problem:** Everyone uses per-user, so we should too.

**Reality:** Per-user works for <20% of products (truly collaborative tools).

**Better:** Choose metric that aligns to value (see `core/05-selecting-value-metrics.md`)

---

### Mistake 2: Usage-Based Without Mitigating Uncertainty

**Problem:** Pure usage-based pricing scares customers (unpredictable bills).

**Reality:** "Bill shock" kills conversion and causes churn.

**Better:** Add caps, alerts, free tiers, or hybrid model (base + usage).

---

### Mistake 3: Too Many Tiers (Complexity)

**Problem:** 6 tiers × 15 features = analysis paralysis

**Reality:** Customers can't decide, abandon.

**Better:** 3 tiers max, 5-8 differentiating features (see `core/06-packaging-tier-design.md`)

---

### Mistake 4: Freemium Without Conversion Strategy

**Problem:** Launch freemium, assume users will upgrade automatically.

**Reality:** 2-5% convert on average (95-98% stay free forever).

**Better:** Active conversion tactics (see `advanced/freemium-free-trial-strategies.md`)

---

## Model Migration Strategies

**Changing models is hard but sometimes necessary:**

### Migrating FROM Per-User TO Usage-Based

**Example:** Slack 2024 (per-user → per-active-user)

**Strategy:**
1. Announce 60 days in advance
2. Grandfather existing customers (6-12 months)
3. New customers on new model immediately
4. Migrate existing in cohorts (smallest first)

---

### Migrating FROM Subscription TO Hybrid

**Example:** MongoDB (subscription → consumption)

**Result:** 40% increase in LTV

**Strategy:**
1. Launch hybrid for new customers first
2. Offer existing customers option to switch (incentive: better value at scale)
3. Keep legacy plans available (6-12 months)

---

### Adding Freemium to Paid-Only

**Example:** Calendly (paid → freemium)

**Strategy:**
1. Create stripped-down free tier (1 event type)
2. Grandfather existing paid (they keep full features)
3. Drive adoption through free tier
4. Optimize conversion to paid (2-5% initially → 6-8% target)

---

## Key Takeaways

1. **Hybrid models = 38% higher NRR** than pure subscription (2024 data)
2. **56% now have consumption elements** (up from 25% in 2021)
3. **Per-user declining** (often wrong metric, discourages adoption)
4. **Freemium mainstream** (42% of SaaS, PLG influence)
5. **AI driving usage-based** (variable costs, outcome value)
6. **Choose model based on value delivery** not what everyone else does
7. **Can change models** but grandfather existing customers

## Next Steps

**Chosen model, ready to design value metric:**
→ Read `core/05-selecting-value-metrics.md`

**Ready to design tiers:**
→ Read `core/06-packaging-tier-design.md`

**Deep dive on usage-based:**
→ Read `advanced/usage-based-pricing-deep-dive.md`

**Deep dive on freemium:**
→ Read `advanced/freemium-free-trial-strategies.md`
