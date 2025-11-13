# Selecting Value Metrics

Choose the metric that best aligns pricing to customer value.

## Overview

**Value metric:** The dimension you use to measure and charge for value (users, API calls, storage, outcomes, etc.).

**Patrick Campbell's critical insight:** "If you get everything else wrong in pricing, but you get your value metric right, you'll do OK. It's that important."

**Why it matters:**
- **Drives customer behavior** (per-user = share logins, per-API-call = use less)
- **Determines expansion revenue** (good metric scales with value)
- **Affects product adoption** (bad metric creates usage anxiety)
- **Impacts churn** (misaligned metrics feel unfair)

**Patrick Campbell's warning:** "8 out of 10 companies using per-user pricing should be using a different value metric."

## The Problem with Defaulting to Per-User

**Per-user is the lazy default** for most SaaS products, but it's often wrong.

### When Per-User Works

✅ **Collaboration tools** where each user gets independent value:
- Slack, Microsoft Teams (each user communicates)
- Figma, Miro (each designer creates)
- Notion, Confluence (each person contributes content)

✅ **Seat-dependent value** where users can't share:
- Salesforce, HubSpot (each sales rep needs own data/pipeline)
- Email tools (each user has own inbox)
- Identity management (each employee needs own account)

---

### When Per-User Fails

❌ **Outcome-focused products** where team size doesn't correlate to value:
- Marketing automation (value = leads, not number of marketers)
- Analytics (value = insights, not number of viewers)
- Project management (value = projects completed, not team size)

❌ **API/infrastructure** where users are irrelevant:
- APIs (value = API calls, not who makes them)
- Cloud infrastructure (value = compute/storage, not engineers)
- Data pipelines (value = data processed, not data scientists)

❌ **Products with sharing use cases**:
- Password managers (teams share logins)
- Design tools (clients review designs but shouldn't need accounts)
- Documentation (external stakeholders read but shouldn't pay per-person)

---

### Why Per-User Creates Problems

**Problem 1: Discourages Adoption**
- Teams limit users to save money
- Shared logins instead of individual accounts
- Gatekeepers control access
- Misaligned incentive: You want adoption, they want fewer users

**Example:** Company needs 50 employees on tool but only buys 20 licenses → shared logins → bad experience → churn

**Problem 2: Doesn't Scale with Value**
- 10-person team vs 100-person team may get same value
- Or 2-person team may get 10x value (depends on use case)
- Per-user assumes linear value with team size (often false)

**Problem 3: Easy to Game**
- Shared role accounts (sales@company.com)
- Password sharing among team
- Rotate users in/out of platform

**Problem 4: Expansion Friction**
- "Can we add 5 more users?" = budget approval process
- Slows adoption, creates admin overhead
- Procurement friction every time team grows

---

## Value Metric Types

### Type 1: Functional Value Metrics (Input-Based)

**Definition:** Based on usage volume (how much they use).

**Examples:**
- **API calls:** Stripe, Twilio, OpenAI (per 1K tokens)
- **Storage:** Dropbox (per GB), AWS S3 (per GB stored)
- **Compute time:** AWS EC2 (per hour), Snowflake (per compute-hour)
- **Events tracked:** Segment, Amplitude (per event)
- **Emails sent:** SendGrid, Mailchimp (per email)
- **Users tracked:** Mixpanel (per monthly tracked user)

**Pros:**
- Aligns to value (use more = get more value)
- Fair (small customers pay less)
- Scales automatically (expansion built-in)

**Cons:**
- Unpredictable costs (usage anxiety)
- Revenue variability (harder to forecast)
- Requires metering infrastructure

**When to use:** Infrastructure, APIs, high-volume/variable usage products

---

### Type 2: Outcome-Based Value Metrics (Results)

**Definition:** Based on results delivered (what they achieve).

**Examples:**
- **Leads generated:** Marketing automation (per lead)
- **Invoices processed:** Accounting software (per invoice)
- **Candidates hired:** Recruiting tools (per hire or % of salary)
- **Deals closed:** Some CRMs (% of deal value)
- **Reports created:** BI tools (per report)
- **Savings generated:** Procurement tools (% of savings)

**Pros:**
- Perfectly aligned to value (pay for results, not inputs)
- Customers love it (pay when you win)
- Differentiates from competition

**Cons:**
- Hard to measure outcomes reliably
- Attribution challenges (did your tool cause result?)
- Revenue timing uncertainty (when did outcome happen?)
- Customers may game metrics

**When to use:** Clear, measurable outcomes that you directly drive

---

### Type 3: Feature-Based Value Metrics

**Definition:** Based on access to features (not usage volume).

**Examples:**
- **Basic vs Advanced features:** Notion (AI features in paid tier)
- **Number of integrations:** Zapier (5 integrations free, unlimited paid)
- **Automation rules:** Marketing tools (3 automations free, unlimited paid)
- **Projects:** Design tools (3 projects free, unlimited paid)

**Pros:**
- Simple to understand
- Predictable revenue
- Easy to tier (good/better/best)

**Cons:**
- Doesn't scale with customer success
- Arbitrary limits can frustrate
- No automatic expansion

**When to use:** Clear feature differentiation, stable usage patterns

---

### Type 4: Company-Size Proxies

**Definition:** Based on company attributes (employees, revenue, scale).

**Examples:**
- **Employees:** HR tools (per employee in company)
- **Revenue:** Vertical SaaS (% of revenue or revenue tiers)
- **Locations:** Multi-location businesses (per location)
- **Customers:** B2B tools serving customers (per customer served)

**Pros:**
- Aligns to ability to pay (larger companies pay more)
- Scales with company growth
- Avoids usage anxiety

**Cons:**
- Not directly tied to value delivered
- Companies may lie about size
- Doesn't reflect actual usage

**When to use:** Clear correlation between company size and value

---

## Choosing Your Value Metric: Decision Framework

### Step 1: Map Customer Journey to Value

**Exercise:** Write out how customers get value from your product:

**Example: Marketing Automation**
1. User creates email campaign
2. System sends emails to contacts
3. Contacts engage (open, click)
4. **Leads generated** (value moment!)
5. Sales team follows up
6. Deals closed (ultimate value)

**Possible value metrics from this journey:**
- Contacts in database (input)
- Emails sent (input)
- **Leads generated (outcome)** ← Aligned to value!
- Users creating campaigns (per-user) ← Not aligned
- Campaigns run (feature-based)

**Choose the metric closest to value realization.**

---

### Step 2: Score Potential Metrics

Rate each candidate metric on these criteria (1-5):

| Metric | Aligned to Value | Easy to Measure | Scales with Customer | Understandable | Total |
|--------|-----------------|-----------------|---------------------|----------------|-------|
| Contacts | 2 | 5 | 3 | 5 | 15 |
| Emails sent | 3 | 5 | 4 | 5 | 17 |
| **Leads generated** | **5** | **3** | **5** | **4** | **17** |
| Users | 1 | 5 | 2 | 5 | 13 |

**Leads generated and emails sent tie.** Choose based on differentiation (leads = unique) vs simplicity (emails = easy).

---

### Step 3: Test Metric Viability

**Questions to validate metric:**

✅ **Does usage of this metric correlate with value received?**
- If customer doubles metric, do they get 2x value?
- If yes → good metric

✅ **Is it easy for customers to understand?**
- Can they predict their cost?
- Does it make intuitive sense?

✅ **Can you measure it reliably?**
- Do you have infrastructure to meter?
- Is attribution clear?

✅ **Does it encourage or discourage desired behavior?**
- Per-API-call might discourage usage (bad if you want adoption)
- Per-outcome encourages usage (good)

✅ **Is it fair across customer segments?**
- Small customers pay less, large pay more (proportional to value)

✅ **Can you explain it in one sentence?**
- "You pay per email sent" (clear)
- "You pay per weighted computation unit adjusted for regional data residency" (confusing)

---

### Step 4: Compare to Competitors

**Not to copy, but to understand market norms:**

| Competitor | Value Metric | Why It Works/Doesn't |
|------------|--------------|---------------------|
| Competitor A | Per-user | Industry standard but discourages adoption |
| Competitor B | Per-contact | Aligns to database size, predictable |
| Competitor C | Per-email-sent | Aligns to usage, but variable costs |
| **Opportunity** | **Per-lead-generated** | **Unique, aligns to outcome** |

**Differentiation opportunity:** If everyone uses per-user, and you use per-outcome, you stand out.

---

## Value Metric Examples by Product Category

### Collaboration/Productivity Tools

| Product | Current Metric | Better Alternative? |
|---------|---------------|-------------------|
| **Slack** | Per-active-user (2024 change) | ✅ Better than per-seat (was previous) |
| **Notion** | Per-user | Could be per-workspace or per-page-views |
| **Figma** | Per-editor (viewers free) | ✅ Good (editors = value) |
| **Miro** | Per-user | Could be per-board or per-collaborator |

**Lesson:** Even collaboration tools re-think per-user (Slack → active users, Figma → editors only)

---

### Marketing/Sales Tools

| Product | Current Metric | Better Alternative? |
|---------|---------------|-------------------|
| **HubSpot** | Per-contact | ✅ Aligns to database size |
| **Salesforce** | Per-user | Makes sense (each rep needs own data) |
| **Mailchimp** | Per-contact | ✅ Aligns to email list size |
| **Calendly** | Per-event-type | ✅ Better than per-user (was previous) |

**Lesson:** Contacts/database size often better than per-user for marketing

---

### Developer/Infrastructure Tools

| Product | Current Metric | Better Alternative? |
|---------|---------------|-------------------|
| **Stripe** | % of transaction + $0.30 | ✅ Perfect (value = transaction volume) |
| **AWS** | Per-resource (EC2 hours, GB storage) | ✅ Granular usage-based |
| **Twilio** | Per-API-call (SMS, voice minute) | ✅ Aligns to usage |
| **GitHub** | Per-user | Debatable (could be per-repo or per-action-minutes) |

**Lesson:** Infrastructure = usage-based (compute, storage, API calls)

---

### Analytics/Data Tools

| Product | Current Metric | Better Alternative? |
|---------|---------------|-------------------|
| **Mixpanel** | Per-monthly-tracked-user | ✅ Scales with data volume |
| **Amplitude** | Per-event | ✅ Usage-based, fair |
| **Tableau** | Per-user | ❌ Should be per-data-source or per-dashboard |
| **Segment** | Per-monthly-tracked-user | ✅ Aligns to data scale |

**Lesson:** Analytics should charge for data scale, not viewers

---

## Multi-Dimensional Value Metrics

**Some products use multiple metrics:**

### Example 1: Datadog (Hybrid)
- **Base:** $15/host/month (access)
- **Add-on:** $5/million custom metrics (usage)
- **Add-on:** $8/GB logs ingested (usage)

**Why it works:** Base covers infrastructure, usage captures expansion

---

### Example 2: Snowflake (Tiered Usage)
- **Compute:** $2-$4 per compute-hour (varies by tier)
- **Storage:** $23-$40/TB/month (varies by tier)

**Why it works:** Higher tiers get volume discounts on usage

---

### Example 3: Slack (Active Users + Feature Tiers)
- **Free:** Unlimited users, 10K messages, basic features
- **Pro:** $7.25/active-user/month, unlimited messages, advanced features
- **Enterprise:** Custom pricing, enterprise features

**Why it works:** Active users (not all users) + feature differentiation

---

## Common Value Metric Mistakes

### Mistake 1: Choosing Easiest to Measure, Not Aligned to Value

**Example:** Choose per-user because it's simple to track, even though value comes from data processed.

**Fix:** Invest in metering infrastructure for right metric

---

### Mistake 2: Too Many Metrics (Complexity)

**Bad example:** "$99/month + $5/user + $0.10/email + $1/GB storage + $0.05/API call"

**Why it fails:** Impossible to predict costs, overwhelming

**Fix:** One primary metric, optionally one secondary (base + usage)

---

### Mistake 3: Metric Creates Perverse Incentives

**Example:** Charge per-support-ticket submitted

**Result:** Customers avoid contacting support, frustration builds, churn

**Fix:** Don't charge for things you want customers to do

---

### Mistake 4: Metric Doesn't Scale

**Example:** Flat-rate pricing where some customers use 100x more resources

**Result:** Large customers subsidized by small, unprofitable

**Fix:** Choose metric that scales with usage/value

---

### Mistake 5: Metric Too Hard to Predict

**Example:** "Weighted algorithmic processing units" (what?)

**Result:** Customers can't forecast spend, avoid commitment

**Fix:** Simple, understandable metric with cost calculator

---

## Transitioning Value Metrics (Changing Your Metric)

**Changing your value metric is hard but sometimes necessary:**

### Case Study: Calendly (Per-User → Per-Event-Type)

**Before (2020):** $8/user/month
- Problem: Teams avoided adding users (admin, support, etc.)
- Expansion limited to headcount growth

**After (2023):** $10/user/month BUT based on event-types, not pure users
- Result: 40% increase in ACV
- Teams added more event types (expansion)

**Migration strategy:**
1. Announce 90 days in advance
2. Grandfather existing (12 months)
3. New customers on new metric immediately
4. Offer migration incentive (free features for 3 months)

---

### Case Study: Slack (Per-User → Per-Active-User)

**Before (2019):** $6.67/user/month (annual)
- Problem: Companies paid for deactivated users, unused accounts

**After (2024):** $7.25/active-user/month
- Result: Fairer pricing (only pay for active users)
- Actually reduced some bills (improved customer perception)

**Why it worked:** More aligned to value (active use) vs arbitrary (all seats)

---

## Value Metric Selection Worksheet

Use `assets/templates/value-metric-selection-worksheet.md` for full template.

**Quick worksheet:**

**1. How do customers get value from your product?**
- Step 1: ____________________
- Step 2: ____________________
- **Value moment:** ____________________ ← This is your metric!

**2. List possible value metrics:**
1. ____________________
2. ____________________
3. ____________________

**3. Score each metric (1-5):**

| Metric | Aligned to Value | Measurable | Understandable | Scales | Total |
|--------|-----------------|------------|----------------|--------|-------|
| Option 1 | _ | _ | _ | _ | _ |
| Option 2 | _ | _ | _ | _ | _ |
| Option 3 | _ | _ | _ | _ | _ |

**4. Choose winner and validate:**
- ☐ Does usage correlate to value received?
- ☐ Can customers predict their cost?
- ☐ Can we measure it reliably?
- ☐ Does it encourage desired behavior?
- ☐ Is it fair across segments?
- ☐ Can we explain in one sentence?

---

## Key Takeaways

1. **"8/10 using per-user should change"** - Patrick Campbell
2. **Choose metric closest to value realization** - Not easiest to measure
3. **Functional (usage) vs Outcome (results)** - Both work, outcome better if measurable
4. **Per-user only for collaboration tools** - Where each user gets independent value
5. **Test metric against 6 criteria** - Aligned, measurable, understandable, scales, fair, simple
6. **Can change metrics** - But grandfather existing customers (6-12 months)
7. **Avoid perverse incentives** - Don't charge for things you want customers to do

## Next Steps

**Chosen value metric, ready to design tiers:**
→ Read `core/06-packaging-tier-design.md`

**Want usage-based pricing:**
→ Read `advanced/usage-based-pricing-deep-dive.md`

**Need to understand pricing models first:**
→ Read `core/04-choosing-pricing-model.md`
