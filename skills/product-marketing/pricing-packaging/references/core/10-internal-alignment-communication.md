# Internal Alignment & Communication

Get cross-functional buy-in before launching pricing changes.

## Overview

Pricing is NOT just marketing's job. It impacts every function:
- **Product:** Feature gating, upgrade prompts, billing infrastructure
- **Sales:** Talk tracks, deal negotiation, objection handling  
- **Customer Success:** Expansion conversations, renewals, usage optimization
- **Finance:** Revenue recognition, forecasting, billing systems
- **Marketing:** Messaging, competitive positioning, campaigns

**Elena Verna's Monetization Council Framework:** Quarterly pricing review with DRI from each function.

## The Monetization Council

### Structure

**DRI (Directly Responsible Individual):** Product Marketing or Product Management

**Core members:**
- Product Marketing (lead)
- Product Management
- Sales (leader)
- Customer Success (leader)
- Finance (CFO or Revenue Operations)
- Marketing

**Meeting cadence:**
- **Quarterly:** Full pricing review
- **Monthly:** Early-stage companies
- **Ad-hoc:** When major pricing changes proposed

---

### Agenda Template

**Q1: Review Performance** (30 min)
- Current pricing metrics (conversion, ACV, NRR)
- Wins and losses
- Customer feedback on pricing
- Competitive changes

**Q2: Experimentation Results** (20 min)
- Active tests and results
- Learnings from experiments
- Recommendations

**Q3: Proposed Changes** (30 min)
- New pricing proposals
- Rationale and data
- Expected impact
- Risks and mitigations

**Q4: Next Quarter Plan** (20 min)
- Roadmap for experiments
- Research needed (WTP studies, competitive analysis)
- Launch timeline for approved changes

---

## Sales Enablement for New Pricing

### Sales Kickoff/Training

**Timing:** 2-4 weeks before launch

**Content:**
1. **Why we're changing** (context, data, customer feedback)
2. **What's changing** (old vs new pricing, feature changes)
3. **How to position** (value messaging, talk tracks)
4. **Objection handling** (FAQs, competitive responses)
5. **Deal desk guidance** (discounting rules, approval workflows)

---

### Sales Talk Tracks

**Situation: Customer asks "Why so expensive?"**

**Talk track:**
```
"I understand price is important. Let me show you the ROI.

Our customers typically see [specific outcome] within [timeframe].

For example, [Company X] saved $50K in the first year by [use case].

Based on your [situation], you'd likely see similar results, 
which means the $10K investment pays for itself in 2 months.

Does that math work for your team?"
```

**Formula:**
1. Empathize
2. Quantify value/ROI
3. Social proof (customer example)
4. Apply to their situation
5. Ask confirming question

---

### Objection Handling Playbook

**Common objections:**

**1. "Competitor X is cheaper"**

Response:
```
"Good question. Competitor X is $X less per month. 

Here's what we include that they don't: [A, B, C].

Our customers tell us that [specific feature] alone 
saves them [quantified value] which more than makes up 
the difference.

We're also [differentiated capability] which 
Competitor X doesn't offer at any price.

Would those capabilities be valuable for your team?"
```

**2. "We're over budget"**

Response:
```
"I understand budget constraints. A few options:

1. We offer annual billing with 20% savings—that brings 
   it to $X/month, closer to your budget.

2. We could start with the Pro tier instead of Business, 
   which is $X less, and you can upgrade when ready.

3. If timing is the issue, we can start next quarter 
   when you have budget.

Which of these would work best?"
```

**3. "Can you offer a discount?"**

Response:
```
"I can check with my manager on what's possible.

To help me make the case, can you share:
- How many users/volume you're looking at?
- Are you considering annual vs monthly?
- Are there other products you're evaluating together?

Depending on your answers, there may be ways to 
structure this to get you better value."
```

(Then follow discount policy—typically 10-20% for annual, multi-year, or volume)

---

## Customer Success Enablement

### Expansion Playbook

**Trigger: Customer hits 80% of usage limit**

CS action:
1. Proactive outreach: "I noticed you're at 80% of your API limit. Want to discuss upgrading to avoid hitting the cap?"
2. Share upgrade options with cost/benefit
3. Offer to schedule call if questions

**Trigger: Customer tries to use gated feature**

CS action:
1. In-app prompt: "Advanced analytics is available on Business plan. Upgrade now or schedule demo?"
2. Follow-up email with use cases and ROI
3. Offer trial of higher tier (14 days)

**Trigger: Renewal approaching (90 days out)**

CS action:
1. Check usage trends (growing = expansion opportunity)
2. Schedule renewal/expansion conversation
3. Present tier upgrade or additional users as part of renewal

---

### Handling Price Increase Conversations

**Scenario:** Existing customer renewing, price increased 15%

**CS talk track:**
```
"As you know, your renewal is coming up on [date].

Since you signed, we've added [X, Y, Z features] which 
increase the value you're getting.

The new price is $X, which is a 15% increase, but 
includes all these new capabilities:
- [Feature A] which helps you [benefit]
- [Feature B] which saves you [time/money]
- [Feature C] which [competitive advantage]

We're also grandfathering customers who renew by [date] 
at current pricing for 6 months, which gives you time 
to see the value of the new features.

Does that work for you, or do you have questions?"
```

See `advanced/price-increase-communication-migration.md` for full strategies.

---

## Finance & Operations Alignment

### Revenue Recognition

**Subscription (annual prepaid):**
- Customer pays $12,000 upfront
- Recognize $1,000/month over 12 months (not all at once)
- Finance needs to track deferred revenue

**Usage-based:**
- Recognize revenue when usage occurs
- Requires accurate usage metering and billing

**Finance needs:**
- Clear revenue recognition policies
- Accounting for discounts, credits
- Refund/churn impact on forecasts

---

### Forecasting Impact

**When raising prices:**
- Assume 10-20% drop in new customer volume
- Assume 5-10% increase in churn (existing customers)
- Net impact: Usually positive (+5-15% revenue) if done right

**Finance scenario planning:**
- Best case: +20% revenue, 5% churn
- Base case: +10% revenue, 10% churn
- Worst case: +0% revenue, 20% churn (if poorly communicated)

---

## Product Alignment

### Feature Gating

**Product needs to implement:**
- Usage limits (API calls, storage, users)
- Feature flags (hide/show based on tier)
- Upgrade prompts (when limit hit or gated feature clicked)
- Billing integration (Stripe, Chargebee, etc.)

**Example:**
```
User clicks "Advanced Analytics" button
→ Check tier: User on Pro plan
→ Pro plan doesn't include Advanced Analytics
→ Show modal: "Advanced Analytics available on Business plan. 
   [Upgrade Now] or [Learn More]"
```

---

### In-Product Messaging

**Upgrade prompts:**
- Tier-gated features: "Available on Business plan"
- Usage limits: "You've used 90% of API calls. Upgrade to Pro for unlimited."
- Value messaging: "Unlock advanced features and save time. Upgrade to Business."

**Best practices:**
- Show value, not just "upgrade"
- Provide clear path (button to upgrade page)
- Don't spam (max 1-2 prompts per session)

---

## Marketing Alignment

### Pricing Page Updates

**Timing:** Coordinated launch (all channels same day)

**Assets needed:**
- Updated pricing page copy
- Feature comparison table
- FAQ updates
- Blog post announcement
- Email to prospects/customers

---

### Campaign Messaging

**For price increases:**
- "We've added [features], price now $X"
- "Existing customers grandfathered at current price for [duration]"
- "New pricing effective [date]"

**For new pricing model:**
- "Introducing flexible pricing based on [value metric]"
- "Pay only for what you use"
- "Better value for teams of all sizes"

---

## Documentation

### Internal Pricing Wiki

**Create single source of truth:**

**Section 1: Current Pricing**
- Pricing model (subscription, usage, hybrid)
- Tier prices (monthly, annual)
- Feature matrix (what's in each tier)
- Discounting policy (annual, volume, enterprise)

**Section 2: Value Messaging**
- Core value proposition
- Tier positioning ("Pro is for...")
- Competitive differentiation
- ROI/value quantification

**Section 3: Sales Resources**
- Talk tracks
- Objection handling
- Competitive responses
- Case studies/social proof

**Section 4: Processes**
- Discount approval workflow
- Custom pricing (enterprise) process
- Contract amendments
- Refund/credit policies

**Section 5: FAQ**
- Internal FAQ (for sales, CS, support)
- External FAQ (for customers)

**Tools:** Notion, Confluence, Google Docs (accessible to all)

---

### Pricing One-Pager

**Format:** Single-page PDF or slide

**Content:**
- Tiers and prices
- Key differentiators (5-8 features)
- Annual discount
- Positioning ("Pro for small teams, Business for companies")
- Contact for questions

**Distribution:** Sales, CS, support, leadership

---

## Launch Communication Timeline

### T-minus 4 weeks

- ☐ Monetization Council approves changes
- ☐ Product begins implementation (feature gating, billing)
- ☐ Finance updates forecasts

### T-minus 2 weeks

- ☐ Sales kickoff/training
- ☐ CS enablement
- ☐ Marketing prepares campaigns
- ☐ Internal pricing wiki updated

### T-minus 1 week

- ☐ Final review with all teams
- ☐ Pricing page staged (not live)
- ☐ Email drafts for customers
- ☐ Support FAQ prepared

### Launch Day

- ☐ Pricing page goes live (9am)
- ☐ Blog post published
- ☐ Email to existing customers (if price change)
- ☐ Sales/CS/Support notified "live"
- ☐ Monitor first 24 hours

### T-plus 1 week

- ☐ Review customer feedback
- ☐ Address objections/issues
- ☐ Sales/CS debrief
- ☐ Adjust messaging if needed

---

## Key Takeaways

1. **Monetization Council = cross-functional pricing DRI** (quarterly reviews)
2. **Sales enablement critical** - Talk tracks, objection handling, discount policies
3. **CS drives expansion** - Upgrade prompts, renewal conversations
4. **Finance needs forecasts** - Revenue recognition, churn assumptions
5. **Product implements** - Feature gating, upgrade prompts, billing
6. **Internal wiki = single source of truth** - Pricing, messaging, processes
7. **4-week launch timeline** - Align all teams before go-live

## Next Steps

**Ready to launch pricing:**
→ Read `core/11-launching-new-pricing.md`

**Need to handle price increases:**
→ Read `advanced/price-increase-communication-migration.md`

**Ready to monitor results:**
→ Read `core/12-monitoring-optimization-metrics.md`
