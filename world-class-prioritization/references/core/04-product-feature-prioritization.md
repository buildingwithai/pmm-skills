# Product & Feature Prioritization Frameworks

*When you have more features to build than time to build them, you need a systematic way to decide what ships first.*

## Why Product Prioritization Matters

You're facing the universal product challenge:
- **Unlimited ideas** from customers, stakeholders, competitors, your own team
- **Limited resources** (engineering time, design capacity, budget)
- **Competing stakeholders** who all think their request is most important
- **No objective criteria** leads to the loudest voice winning (usually HiPPO - Highest Paid Person's Opinion)

**The cost of wrong priorities:**
- Opportunity cost (you built X instead of Y, and Y would have had 10× impact)
- Technical debt (rushed features create future problems)
- Team morale (building things nobody uses is demoralizing)
- Customer churn (you didn't build what they actually needed)

**The value of good prioritization:**
- Build what matters most
- Align stakeholders around data, not politics
- Say no confidently (with rationale)
- Ship faster (focus on vital few, not trivial many)

## How to Choose Your Framework

Different situations need different frameworks. Here's the quick guide:

| Your Situation | Use This Framework | Why |
|----------------|-------------------|-----|
| Ready-made product, have usage data | **RICE** | Most comprehensive; uses real data |
| Early stage, MVP mode, need speed | **ICE** | Faster than RICE; good with limited data |
| Need stakeholder alignment fast | **MoSCoW** | Simple categories; builds consensus |
| Cost of delay is critical | **WSJF** | Explicitly accounts for time sensitivity |
| Want to understand customer expectations | **Kano Model** | Reveals what delights vs. what's expected |
| Need simple visual for execs | **Value vs. Effort Matrix** | 2×2 quadrant everyone understands |
| Want customer input directly | **Buy a Feature** | Collaborative; surfaces real preferences |
| Tight budget, need economic focus | **CD3** | Pure ROI calculation |

**General rule of thumb:**
- **Quantitative frameworks** (RICE, WSJF, CD3): When you have data and want rigor
- **Qualitative frameworks** (MoSCoW, Value/Effort): When you need speed or stakeholder buy-in
- **Customer-focused** (Kano, Buy a Feature): When understanding customer expectations matters most

---

## Framework 1: RICE

**Best for:** Established products with user data; teams that want data-driven prioritization

### What It Is

RICE scores features based on four factors:
- **R**each: How many users/customers will this impact? (per time period)
- **I**mpact: How much will it impact each user? (scale: 3=massive, 2=high, 1=medium, 0.5=low, 0.25=minimal)
- **C**onfidence: How sure are you about Reach and Impact? (percentage: 100%=high, 80%=medium, 50%=low)
- **E**ffort: How much work will it take? (person-months or story points)

**Formula:** `RICE Score = (Reach × Impact × Confidence) / Effort`

Higher score = higher priority

### When to Use RICE

✅ **Use RICE when:**
- You have a ready-made product with users
- You can measure or estimate reach (active users, customers)
- You want to depoliticize prioritization (data over opinions)
- Stakeholders keep disagreeing on priorities
- You need to compare very different types of features

❌ **Don't use RICE when:**
- You're pre-launch (no reach data yet)
- You can't estimate reach reliably
- You need a decision in the next 30 minutes (RICE takes time)
- Your team won't commit to the scoring process

### How to Use RICE (Step-by-Step)

**Step 1: List all feature candidates**
Create a spreadsheet with one feature per row.

**Step 2: Estimate Reach**
For each feature, estimate: *How many users/customers will this affect in the next quarter (or year)?*

Examples:
- "Mobile app redesign" → Affects all mobile users → 10,000 users/quarter
- "Admin panel export feature" → Affects only admins → 50 users/quarter
- "New onboarding flow" → Affects all new signups → 500 users/quarter

**Step 3: Score Impact**
For each feature, rate impact per user:
- **3 (Massive)**: Solves a critical pain point; user can't live without it
- **2 (High)**: Major improvement to workflow; users will love it
- **1 (Medium)**: Noticeable improvement; users will appreciate it
- **0.5 (Low)**: Minor improvement; nice to have
- **0.25 (Minimal)**: Barely noticeable; marginal value

**Step 4: Set Confidence**
How confident are you in your Reach and Impact estimates?
- **100%**: You have hard data; you've validated with customers
- **80%**: Strong anecdotal evidence; customer requests; usage data supports it
- **50%**: Educated guess; limited validation; uncertain

*Tip: If confidence is below 50%, you probably need to do more research before prioritizing.*

**Step 5: Estimate Effort**
How much work to build this? Use person-months (or story points if you prefer).

Examples:
- "Simple UI tweak" → 0.5 person-months
- "New dashboard page" → 2 person-months
- "Complete platform migration" → 12 person-months

**Step 6: Calculate RICE scores**
Plug into formula: `(Reach × Impact × Confidence%) / Effort`

**Step 7: Sort by score (highest first)**
This is your prioritized list.

### Example RICE Scoring

Let's say you're a PM with 4 competing features:

| Feature | Reach | Impact | Confidence | Effort | RICE Score | Priority |
|---------|-------|--------|------------|--------|------------|----------|
| Mobile redesign | 10,000 | 2 | 80% | 3 | **5,333** | #2 |
| Export to CSV | 2,000 | 1 | 100% | 0.5 | **4,000** | #3 |
| New onboarding | 500 | 3 | 80% | 1 | **1,200** | #4 |
| API rate limiting | 15,000 | 3 | 100% | 2 | **22,500** | #1 |

**Result:** Build API rate limiting first (highest RICE score), even though it's not the loudest request.

### Why This Removes Politics

When a stakeholder says "We MUST build my feature," you can respond:

> "Let's run it through RICE. What's the reach? Impact? Our confidence level? Effort required? Based on those numbers, here's how it compares to other priorities. If it scores higher, we'll move it up. If not, we need to deprioritize something else. What should we deprioritize?"

This shifts the conversation from **opinions** ("I think...") to **data** ("The numbers show...").

### Common Mistakes with RICE

1. **Inflating scores to win**: Stakeholders game the system by inflating their reach/impact
   - *Fix: Require evidence; challenge unrealistic estimates*

2. **Ignoring confidence**: Treating a 50% confidence score the same as 100%
   - *Fix: Explicitly discuss confidence; validate low-confidence ideas before prioritizing*

3. **Effort inflation**: Engineering estimates are always pessimistic
   - *Fix: Use historical data; track actual vs. estimated effort*

4. **Not revisiting scores**: Priorities change; yesterday's RICE may not apply today
   - *Fix: Re-score quarterly; adjust when new data emerges*

5. **Using RICE alone**: Numbers don't capture strategic bets or brand value
   - *Fix: Reserve 10-20% capacity for strategic bets outside RICE*

### Tools for RICE Scoring

- **Spreadsheet** (Google Sheets, Excel): Simple, flexible, free
- **Productboard**: Built-in RICE scoring
- **Airfocus**: RICE + other frameworks
- **Aha!**: RICE scoring with roadmap integration

---

## Framework 2: ICE

**Best for:** Early-stage products; MVPs; teams that need to move fast with limited data

### What It Is

ICE is a simplified version of RICE (no Reach component). Score features on:
- **I**mpact: How much will this move the needle? (1-10)
- **C**onfidence: How sure are you? (1-10)
- **E**ase: How easy is this to build? (1-10, inverse of effort)

**Formula:** `ICE Score = (Impact + Confidence + Ease) / 3`

Or sometimes: `ICE Score = Impact × Confidence × Ease`

*Note: Different teams use different formulas. Pick one and be consistent.*

### When to Use ICE

✅ **Use ICE when:**
- You're pre-product-market fit (don't have reach data yet)
- You need a quick prioritization (RICE is too slow)
- You're in MVP/iteration mode (ship fast, learn fast)
- Your team is small and nimble

❌ **Don't use ICE when:**
- You have good data (use RICE instead for more rigor)
- You need to justify decisions to exec team (ICE is more subjective)
- Stakeholder alignment is critical (ICE lacks the nuance for politics)

### How to Use ICE

**Step 1: List feature ideas**

**Step 2: Score each on 1-10 scale**
- **Impact:** Will this move key metrics? (10=game changer, 1=marginal)
- **Confidence:** How sure are you? (10=certain, 1=total guess)
- **Ease:** How easy to build? (10=trivial, 1=herculean effort)

**Step 3: Calculate ICE score** (using average or multiplication)

**Step 4: Sort and prioritize**

### Example ICE Scoring

Same 4 features from before:

| Feature | Impact | Confidence | Ease | ICE Score (avg) | Priority |
|---------|--------|------------|------|-----------------|----------|
| Mobile redesign | 8 | 7 | 4 | 6.3 | #3 |
| Export to CSV | 5 | 10 | 9 | 8.0 | #2 |
| New onboarding | 9 | 7 | 8 | 8.0 | #2 (tie) |
| API rate limiting | 10 | 10 | 7 | 9.0 | #1 |

### ICE vs. RICE: When to Use Which

- **RICE** = More rigorous, more data, slower, better for stakeholder alignment
- **ICE** = Faster, less data needed, more subjective, better for small teams iterating

Think of ICE as "RICE for startups."

---

## Framework 3: MoSCoW

**Best for:** Stakeholder alignment; release planning; setting clear expectations

### What It Is

MoSCoW categorizes features into 4 buckets:
- **M**ust have: Non-negotiable; product fails without it
- **S**hould have: Important but not critical; workaround exists
- **C**ould have: Nice to have; include if time permits
- **W**on't have: Out of scope for this release (explicitly deferred)

### When to Use MoSCoW

✅ **Use MoSCoW when:**
- You need fast stakeholder alignment (hours, not days)
- You're planning a specific release (MVP, v2.0, etc.)
- You want simple categories everyone understands
- Politics are high (MoSCoW forces tough conversations)

❌ **Don't use MoSCoW when:**
- You need granular prioritization (MoSCoW only gives 4 buckets)
- You want quantitative comparison (it's qualitative)
- Everything is "Must have" (forces hard choices)

### How to Use MoSCoW

**Step 1: List all feature candidates for the release**

**Step 2: Categorize each feature**

Ask: *"Can we ship this release without this feature?"*
- **Yes, easily** → Could have or Won't have
- **Yes, but users will complain** → Should have
- **No, absolutely not** → Must have

**Key rule:** Limit "Must have" to **60% of your capacity**. If everything is "Must have," you haven't prioritized.

**Step 3: Within each category, rank if needed**
You can sub-prioritize within "Should have" and "Could have."

**Step 4: Communicate the categorization**
Make it visible to all stakeholders. Lock in "Must have" scope; everything else is flexible.

### Example MoSCoW for MVP Launch

**Must Have (60% capacity):**
- User signup/login
- Create account
- Basic dashboard
- Payment processing
- Email notifications

**Should Have (20% capacity):**
- Password reset
- User profile editing
- Activity log

**Could Have (10% capacity):**
- Dark mode
- Export to PDF
- Custom themes

**Won't Have (out of scope for v1):**
- Mobile app
- API for third parties
- Advanced analytics
- Integrations

### Why MoSCoW Works for Alignment

It forces the hard conversation upfront:

> Stakeholder: "We MUST have advanced analytics in v1."
> You: "Okay, if that's Must have, what Should have or Could have do we drop? We're already at 60% capacity on Must haves."
> Stakeholder: "Well... maybe it's a Should have for v1.1."

The constraint (60% Must have limit) creates clarity.

### Common Mistakes with MoSCoW

1. **Everything is "Must have"**: No constraint → no prioritization
   - *Fix: Enforce 60% rule; push back on Must have inflation*

2. **"Won't have" is ignored**: Teams treat it as "nice to have later" and clutter backlog
   - *Fix: Won't have means NO for this release; document WHY*

3. **No sub-ranking**: 10 "Should haves" but no order
   - *Fix: Rank within each category*

4. **Set-and-forget**: MoSCoW decided once, never revisited
   - *Fix: Revisit weekly; adjust as scope changes*

---

## Framework 4: WSJF (Weighted Shortest Job First)

**Best for:** Agile teams; when cost of delay matters; SAFe framework users

### What It Is

WSJF prioritizes based on **economic value per unit of time**. It asks: *What's the cost of NOT doing this, divided by how long it takes?*

**Cost of Delay (CoD)** = User/Business Value + Time Criticality + Risk Reduction/Opportunity Enablement

**Job Size** = Effort estimate (story points, days, etc.)

**Formula:** `WSJF = Cost of Delay / Job Size`

Higher WSJF = higher priority (maximize value per unit of time).

### When to Use WSJF

✅ **Use WSJF when:**
- Time sensitivity matters (regulatory deadline, competitive threat, seasonal)
- You're using SAFe (Scaled Agile Framework)
- Cost of delay is measurable or estimable
- You want to prioritize "quick wins" AND high-value bets

❌ **Don't use WSJF when:**
- Your team doesn't understand Cost of Delay (requires training)
- Time doesn't matter much (stable product, no urgency)
- You need simplicity (WSJF has more components than RICE/ICE)

### How to Use WSJF

**Step 1: Score Cost of Delay (3 components, each 1-10):**

**User/Business Value:** Revenue potential, user impact
- 10 = Huge revenue or massive user impact
- 5 = Moderate revenue or impact
- 1 = Minimal revenue or impact

**Time Criticality:** How fast does value decay?
- 10 = Urgent (regulatory, competitive, seasonal)
- 5 = Moderate urgency
- 1 = No urgency (value doesn't decay)

**Risk Reduction/Opportunity Enablement:** Does this reduce risk or enable future work?
- 10 = Massive risk mitigation or unlocks key capabilities
- 5 = Some risk reduction
- 1 = No risk reduction or enablement

**Total CoD = User Value + Time Criticality + Risk Reduction**

**Step 2: Estimate Job Size** (story points, person-days, etc.)

**Step 3: Calculate WSJF** = CoD / Job Size

**Step 4: Sort by WSJF (highest first)**

### Example WSJF Scoring

| Feature | User Value | Time Crit | Risk Red | CoD | Job Size | WSJF | Priority |
|---------|------------|-----------|----------|-----|----------|------|----------|
| Security patch | 5 | 10 | 10 | 25 | 3 | **8.33** | #1 |
| New pricing page | 8 | 7 | 2 | 17 | 5 | **3.40** | #3 |
| Quick UI fix | 3 | 3 | 1 | 7 | 1 | **7.00** | #2 |
| Platform migration | 9 | 2 | 9 | 20 | 20 | **1.00** | #4 |

**Insight:** Security patch wins (high urgency + high risk, moderate effort). Platform migration is valuable but expensive and not urgent → lower priority.

### Why WSJF Prioritizes "Quick Wins"

Because WSJF divides by Job Size, **small valuable things score higher than large valuable things**.

This prevents "big project syndrome" where teams spend 6 months on one massive feature while ignoring 20 quick wins.

### WSJF vs. RICE

- **RICE** emphasizes reach and impact
- **WSJF** emphasizes time sensitivity and quick wins
- Use **RICE** for user-centric prioritization
- Use **WSJF** for economic/time-sensitive prioritization

---

## Framework 5: CD3 (Cost of Delay Divided by Duration)

**Best for:** Economic prioritization; portfolio management; maximizing ROI

### What It Is

A simplified version of WSJF focused purely on ROI.

**Formula:** `CD3 = Revenue potential / (Months to implement × 1,000)`

Highest CD3 = fastest return on investment.

### When to Use CD3

✅ **Use CD3 when:**
- You have revenue estimates for features
- Budget/capacity is constrained
- You want pure economic prioritization
- Executive team cares about ROI

❌ **Don't use CD3 when:**
- Not everything is revenue-driven (internal tools, infrastructure)
- Revenue estimates are unreliable

### Example CD3

| Feature | Revenue Potential | Months | CD3 | Priority |
|---------|------------------|--------|-----|----------|
| Enterprise SSO | $500K/year | 4 | **125** | #1 |
| Mobile app | $300K/year | 6 | **50** | #2 |
| Analytics dashboard | $100K/year | 2 | **50** | #2 (tie) |

---

## Framework 6: Kano Model

**Best for:** Understanding customer expectations; balancing feature types; avoiding feature bloat

### What It Is

The Kano Model categorizes features based on how they affect customer satisfaction:

1. **Basic/Must-Have Features**: Expected; no delight if present, huge dissatisfaction if absent
   - *Example: Turn signal in a car; login functionality*

2. **Performance Features**: Satisfaction scales linearly with quality
   - *Example: Speed, ease of use, price*

3. **Excitement/Delighter Features**: Not expected; disproportionate delight if present, no dissatisfaction if absent
   - *Example: Surprise features nobody asked for; iPhone's first touchscreen*

Two additional categories:
- **Indifferent**: Customers don't care either way
- **Reverse**: Some customers want it, others actively dislike it

### Why Kano Matters

**Key insight:** Features migrate over time.
- **Yesterday's delighter** → **Today's performance** → **Tomorrow's basic**
- Example: AI features were excitement in 2023 → performance in 2024 → basic expectation in 2025

**Prioritization implication:**
- Build **Basic features first** (must haves)
- Invest in **Performance features** for competitive advantage
- Sprinkle in **Delighters** for differentiation
- Cut **Indifferent features** (waste of resources)

### When to Use Kano

✅ **Use Kano when:**
- You want to understand customer expectations
- You need to balance feature types (basics vs. delighters)
- You're planning product refresh (what's now "basic"?)
- You want to avoid feature bloat

❌ **Don't use Kano when:**
- You need quick prioritization (Kano requires surveys)
- You don't have customer access
- You're in pure MVP mode (focus on basics only)

### How to Use Kano (Survey Method)

**Step 1: Create Kano survey**
For each feature, ask two questions:
- **Functional:** "How do you feel if this feature IS present?"
- **Dysfunctional:** "How do you feel if this feature is NOT present?"

Answers: Like, Expect, Neutral, Live with, Dislike

**Step 2: Map responses to categories**
Based on response pairs, classify feature as Basic, Performance, Excitement, Indifferent, or Reverse.

**Step 3: Prioritize based on category**
- **Basic** → Must build (table stakes)
- **Performance** → Invest here for competitive advantage
- **Excitement** → Budget 10-20% for differentiation
- **Indifferent** → Cut (nobody cares)

### Example Kano Analysis

For a B2B SaaS product in 2025:

| Feature | Kano Category | Implication |
|---------|---------------|-------------|
| Login/authentication | Basic | Must have (table stakes) |
| Fast load times | Performance | Competitive advantage (invest) |
| AI-powered suggestions | Basic→Performance | Was excitement in 2023, now expected |
| Dark mode | Performance | Some love it, others don't care |
| Custom mascot | Indifferent | Nobody asked for this; cut it |
| Voice commands | Excitement | Differentiator if done well |

---

## Framework 7: Value vs. Effort Matrix (2×2)

**Best for:** Quick visual prioritization; exec presentations; simple stakeholder alignment

### What It Is

A simple 2×2 matrix:
- **X-axis:** Effort (Low → High)
- **Y-axis:** Value (Low → High)

**Four quadrants:**
1. **High Value / Low Effort** = Quick Wins (do first)
2. **High Value / High Effort** = Big Bets (strategic investment)
3. **Low Value / Low Effort** = Fill-ins (do if time permits)
4. **Low Value / High Effort** = Money Pits (avoid)

### When to Use Value vs. Effort

✅ **Use Value vs. Effort when:**
- You need a visual for execs or stakeholders
- You want quick consensus in a workshop
- You have limited time (can plot in 30 mins)
- Precision doesn't matter (just need directional)

❌ **Don't use Value vs. Effort when:**
- You need granular prioritization
- Stakeholders will argue about placement
- You want quantitative comparison

### Example Matrix

```
High Value  │  Big Bets        │  Quick Wins
            │  • Platform      │  • Export CSV
            │    migration     │  • UI fix
            │                  │  • Password reset
────────────┼──────────────────┼───────────────
Low Value   │  Money Pits      │  Fill-ins
            │  • Rewrite from  │  • Dark mode
            │    scratch       │  • Custom themes
            │                  │
            └──────────────────┴───────────────
              High Effort       Low Effort
```

**Action plan:**
1. Do **Quick Wins** immediately (low-hanging fruit)
2. Schedule **Big Bets** strategically (require planning, resources)
3. Batch **Fill-ins** when you have spare capacity
4. Avoid **Money Pits** entirely

---

## Framework 8: Buy a Feature

**Best for:** Collaborative prioritization; customer input; team consensus; stakeholder workshops

### What It Is

A prioritization "game" where participants (customers, stakeholders, team members) "buy" features with fake money.

**Setup:**
- List all feature ideas
- Assign each a "price" (based on development cost)
- Give each participant "money" (typically 1/3 to 2/3 of total feature cost)
- Participants "buy" features they value most
- Participants can pool money for expensive features

**Result:** Features with most "purchases" = highest priority.

### When to Use Buy a Feature

✅ **Use Buy a Feature when:**
- You want customer input directly
- You have conflicting stakeholder opinions (forces trade-offs)
- You want to build consensus in a workshop
- You need to surface coalitions (who cares about what)

❌ **Don't use Buy a Feature when:**
- You can't get customers/stakeholders in a room (or virtual session)
- Features aren't easily priced
- You need a decision today (requires setup)

### How to Run Buy a Feature

**Step 1: Prepare the feature list**
- 10-20 features max (more is overwhelming)
- Assign prices based on estimated development effort
  - Small feature: $10
  - Medium feature: $50
  - Large feature: $100

**Step 2: Give participants money**
- Each person gets $100-200 (enough to buy some, not all)
- Forces prioritization

**Step 3: Let them shop**
- Participants "buy" features by allocating their money
- Allow pooling (2+ people combine money for expensive feature)
- Track purchases on a board (physical or digital)

**Step 4: Tally results**
- Which features got most money?
- What coalitions formed? (Who pooled for what?)

**Step 5: Discuss**
- Why did Feature X get so much money?
- Why did Feature Y get nothing?
- Insights emerge

### Example Buy a Feature Session

**Features & Prices:**
- Mobile app: $150
- Export to CSV: $25
- Dark mode: $25
- Advanced analytics: $100
- API access: $100

**Participants (5 customers, each with $150):**
- 3 customers pool $450 for Mobile app → Mobile wins
- 4 customers buy Export to CSV ($100 total) → Clear demand
- 1 customer buys Dark mode → Low priority
- 2 customers pool $200 for API access → Moderate demand
- 0 customers buy Advanced analytics → Cut it

**Result:** Mobile app #1, Export CSV #2, API #3, Dark mode #4, Advanced analytics = cut.

### Tools for Buy a Feature

- **In-person:** Physical money (Monopoly money, poker chips)
- **Virtual:** Miro, Mural templates with voting dots

---

## Combining Frameworks

You don't have to pick just one. Here's how to combine them:

### RICE + MoSCoW
- Use **RICE** to score all features
- Use **MoSCoW** to categorize by release
  - Top RICE scores → Must have
  - Medium scores → Should have
  - Low scores → Could have or Won't have

### Kano + RICE
- Use **Kano** to categorize feature types
- Use **RICE** within each category
  - Build all Basics (sorted by RICE)
  - Then invest in top Performance features (sorted by RICE)
  - Sprinkle in top Delighters

### Buy a Feature + RICE
- Run **Buy a Feature** with customers to get qualitative input
- Run **RICE** internally to add data rigor
- Combine: Customer preference + RICE score = final priority

---

## Implementation Tips

### Getting Stakeholder Buy-In

**Before introducing a framework:**
1. **Acknowledge the problem:** "We all have different opinions on priorities. We need an objective way to decide."
2. **Propose the framework:** "Let's try RICE scoring. Here's how it works..."
3. **Invite collaboration:** "Let's score these together so everyone's input is included."
4. **Commit to the output:** "Once we score them, we commit to the top priorities. Deal?"

**Handling pushback:**
- "This is too slow" → Start with ICE or Value/Effort (faster)
- "My feature is special" → "Great, let's score it. If it wins, we'll prioritize it."
- "I don't trust the numbers" → "What data would make you trust it? Let's get that data."

### Making It Stick

**Common failure mode:** You score once, then revert to HiPPO decision-making.

**How to make it stick:**
1. **Document the process:** "We use RICE for all roadmap decisions"
2. **Revisit quarterly:** Re-score as data changes
3. **Make it visible:** Roadmap shows RICE scores
4. **Use it in roadmap meetings:** "What's the RICE score?" becomes standard question

### When to Override the Framework

Frameworks are tools, not laws. Override when:
- **Strategic bet:** Low score but aligns with company vision
- **Technical debt:** Doesn't score well but prevents future problems
- **Regulatory/Legal:** Must do regardless of score
- **Customer commitment:** Already promised to key customer

**Key:** Make the override explicit. Don't just ignore the framework.

> "This scores low on RICE, but we're doing it anyway because [strategic/legal/commitment reason]. This is the exception, not the rule."

---

## Quick Reference: Which Framework When

### You Need...
**Fast decision (30 mins):** Value vs. Effort Matrix
**Stakeholder alignment:** MoSCoW
**Data-driven rigor:** RICE
**Economic focus:** CD3
**Time sensitivity:** WSJF
**Customer expectations insight:** Kano Model
**Customer collaboration:** Buy a Feature
**MVP speed:** ICE

### Your Situation...
**Startup, pre-PMF:** ICE, Value/Effort
**Growth stage, scaling:** RICE, WSJF
**Enterprise, portfolio:** WSJF, CD3
**High stakeholder politics:** MoSCoW, Buy a Feature, RICE (data depoliticizes)
**Customer-obsessed culture:** Kano, Buy a Feature

---

## Summary: The Meta-Framework

Here's the framework for choosing frameworks:

1. **Do you have user/usage data?**
   - Yes → RICE or WSJF
   - No → ICE or MoSCoW

2. **Is time sensitivity critical?**
   - Yes → WSJF
   - No → RICE or ICE

3. **Do you need stakeholder alignment fast?**
   - Yes → MoSCoW or Buy a Feature
   - No → RICE

4. **Do you want customer input directly?**
   - Yes → Buy a Feature or Kano
   - No → RICE, ICE, or WSJF

5. **Is this purely economic/budget-driven?**
   - Yes → CD3
   - No → RICE

6. **Need simple visual for execs?**
   - Yes → Value vs. Effort Matrix
   - No → Any of the above

**When in doubt, start with RICE** (if you have data) **or ICE** (if you don't).

---

## Next Steps

Now that you understand the frameworks:

1. **Pick one** that fits your current situation
2. **Try it** on your top 10 feature candidates
3. **Share with stakeholders** and get feedback
4. **Iterate** - adjust the framework to your context
5. **Make it a habit** - use it for every roadmap decision

**Remember:** The goal isn't perfect prioritization. The goal is **better prioritization than gut feel alone** and **alignment around shared criteria**.

The framework is a tool to facilitate better conversations, not a replacement for judgment.

---

**Related references:**
- For stakeholder conflict: `05-stakeholder-management-prioritization.md`
- For saying no to requests: `07-saying-no-professionally.md`
- For delegation of features: `06-delegation-mastery.md`
- For OKR alignment: `02-goal-setting-frameworks.md`
