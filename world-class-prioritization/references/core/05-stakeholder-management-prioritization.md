# Stakeholder Management & Prioritization

*When multiple stakeholders want different things and everyone thinks their request is most important, you need frameworks that remove politics and build consensus.*

## The Stakeholder Prioritization Challenge

**You're a PM/PMM with limited resources. You face:**
- VP Sales: "We need enterprise features for this $1M deal"
- CEO: "Focus on consumer growth, that's our future"  
- VP Product: "Technical debt is crushing us, we need to refactor"
- Engineering: "We're at capacity, can't do all three"
- You: "How do I say no to executives without career suicide?"

**The pattern:** Multiple stakeholders, limited capacity, political dynamics, no clear prioritization criteria.

**Without a framework:** Loudest voice wins (usually HiPPO - Highest Paid Person's Opinion).

**With a framework:** Data-driven decisions, transparent criteria, stakeholder alignment.

## Why Stakeholder Conflicts Happen

**Root causes:**
1. **No shared prioritization criteria** - Everyone uses different logic
2. **Optimizing for different metrics** - Sales wants deals, Product wants usage, CEO wants growth
3. **Information asymmetry** - Each stakeholder has partial picture
4. **Political dynamics** - Can't say no to executives
5. **Capacity invisibility** - Stakeholders don't see total demand vs. capacity

## Framework 1: Data-Driven Scoring (RICE/WSJF)

**When to use:** Multiple competing requests, need objectivity

**Why it works:** Numbers depoliticize decisions. Hard to argue with data.

**Process:**
1. Take all stakeholder requests
2. Score each using RICE or WSJF (see `04-product-feature-prioritization.md`)
3. Share scoring methodology upfront
4. Present results: "Based on RICE, here's the rank order"
5. Commit to the scores

**Example script:**
> "We have 8 requests from various stakeholders. Let's use RICE scoring so we're objective. Here's how it works: [explain]. We'll score together in this meeting, commit to the results, and prioritize top 3 this quarter."

**Key:** Get stakeholders to agree to the framework BEFORE scoring. Once they commit, harder to argue later.

## Framework 2: Amazon's "Working Backward"

**What it is:** Start with desired customer outcome, work backward to requirements.

**Why it works:** Aligns stakeholders on WHO WE'RE SERVING (the customer), not internal politics.

**Process:**
1. Define the customer problem/outcome we're solving for
2. Write the "press release" (what would we announce when done?)
3. Work backward: What's needed to achieve that outcome?
4. Stakeholder requests either serve that outcome or they don't

**Example:**
**Customer outcome:** "Enterprise customers can deploy our product in <1 day vs. current 2 weeks"

**Stakeholder requests mapped:**
- Enterprise SSO → YES (required for fast deployment)
- Consumer growth features → NO (doesn't serve this outcome)
- Technical debt → PARTIAL (only if it speeds deployment)

**Result:** Clear filter. If it doesn't serve the customer outcome, it's deprioritized.

## Framework 3: Opportunity Cost Framing

**When to use:** Executive is pushing their priority, need to surface trade-offs

**The script:**
> "If we prioritize [Executive A's request], we can't deliver [Executive B's request] this quarter. Which is more important to the company right now?"

**Why it works:** Forces executives to make the hard choice, not you.

**Example:**
> "CEO, if we focus all engineering capacity on consumer growth (your priority), we can't deliver the enterprise features VP Sales needs for the $1M deal. We have capacity for one, not both. Which should we prioritize?"

**Result:** CEO makes the call. You're not saying no - you're presenting the trade-off and letting leadership decide.

## Framework 4: Capacity Visualization

**The problem:** Stakeholders don't see total demand.

**The solution:** Make it visible.

**Create a roadmap showing:**
- Total requests (50 features)
- Total capacity (can ship 10 per quarter)  
- Current commitments (7 already locked in)
- Available capacity (3 slots remaining)

**Present it:**
> "Here's everything requested. Here's our capacity. We have 3 open slots this quarter. Which 3 should we prioritize?"

**Why it works:** Constraints become visible. Stakeholders see it's not about saying no to them - it's about capacity reality.

## Framework 5: Customer Voice

**When to use:** Internal opinions conflict, need external truth

**The power move:** Let customers decide.

**Process:**
1. Survey customers: "Which of these features would you value most?"
2. Get usage data: "Which features drive retention/revenue?"
3. Win/loss analysis: "Why do we lose deals?"
4. Present findings: "Here's what customers actually want"

**Why it's powerful:** Hard for executives to argue with customer data.

**Example:**
> "VP Sales says we need feature X. I surveyed 50 enterprise customers. Only 12% ranked it top 3. 68% ranked feature Y top 3. Customer data says Y, not X."

## Building Consensus Without Compromise

**Consensus ≠ everyone gets what they want**

**Consensus = everyone understands and accepts the decision**

**How to build it:**

**Step 1: Alignment on criteria**
Get agreement on HOW you'll decide before you decide.
> "Can we agree to use RICE scoring for prioritization?" [Get yes]

**Step 2: Transparent process**
Show the work. Don't decide in a black box.
> "Here's how we scored each request. Here are the numbers."

**Step 3: Disagree and commit (Amazon principle)**
> "I know some of you wanted different priorities. But we've made the decision based on our agreed framework. Can everyone commit to this plan, even if you disagree?"

**Step 4: Revisit quarterly**
> "This is our Q2 plan. We'll re-evaluate in Q3. Your deprioritized request can be re-scored then."

## Handling HiPPO (Highest Paid Person's Opinion)

**The problem:** CEO/VP overrides your framework because they outrank you.

**Strategies:**

**1. Pre-align one-on-one**
Don't surprise execs in a group meeting. Socialize the decision beforehand.
> "Before the roadmap meeting, can I walk you through our prioritization approach? Want to make sure you're aligned."

**2. Get them to commit to process upfront**
> "CEO, we've been inconsistent on prioritization. Can we commit to using RICE scoring this quarter? I need your support to make this work."

**3. Frame as experiment**
> "Let's try data-driven prioritization for one quarter. If it doesn't work, we'll adjust."

**4. Use customer data**
> "I know you want feature X, but customer data shows they want Y. As CEO, you've said we're customer-obsessed. This is what customers are telling us."

**5. Show the cost**
> "If we do your request, here's what we can't do: [list]. Are you comfortable with that trade-off?"

**6. Last resort: Do it, but track**
> "We're doing this because you requested it, overriding our scoring. Let's track: Did it have the impact you expected? We'll use this data for future decisions."

## Stakeholder Influence Mapping

**Not all stakeholders are equal. Map them:**

```
High Power
High Interest → MANAGE CLOSELY (CEO, VP Product)

High Power  
Low Interest → KEEP SATISFIED (CFO, Board)

Low Power
High Interest → KEEP INFORMED (Team, Users)

Low Power
Low Interest → MONITOR (Adjacent teams)
```

**Tailor your approach:**
- **Manage closely:** Weekly updates, involve in decisions
- **Keep satisfied:** Monthly updates, major decisions only
- **Keep informed:** Share outcomes, gather feedback
- **Monitor:** No active management needed

## Regular Prioritization Rituals

**Don't prioritize once and forget. Build rhythm:**

**Weekly:** Backlog grooming (internal team)
**Monthly:** Stakeholder sync (share progress, gather feedback)
**Quarterly:** Roadmap planning (set next quarter priorities with stakeholders)

**Why rituals work:**
- Expectations are set (stakeholders know when they'll be heard)
- Surprises are minimized (regular communication)
- Trust is built (consistent process)

## Scripts for Difficult Conversations

**Saying no to VP:**
> "I understand this is important to you. Based on our RICE scoring, it ranks #12. We have capacity for top 5 this quarter. Can we revisit this in Q3 planning?"

**Deprioritizing CEO pet project:**
> "I know you're passionate about this. Our customer data shows different priorities. As CEO, you've empowered us to be data-driven. This is what the data shows. Can we test your hypothesis with an experiment first before committing full resources?"

**When two VPs conflict:**
> "VP Sales wants X, VP Product wants Y. We have capacity for one. This is a business priority decision above my level. Can you two align on which serves the company strategy better, and I'll execute on that?"

**When everything is "urgent":**
> "If everything is urgent, nothing is. Let's use the Eisenhower matrix: Which of these is truly urgent AND important? Let's do those, and schedule the rest."

## Summary

**Key principles:**
1. **Use objective frameworks** (RICE, WSJF, customer data)
2. **Make constraints visible** (capacity, trade-offs)
3. **Get stakeholder buy-in upfront** (commit to process before deciding)
4. **Surface trade-offs** (opportunity cost framing)
5. **Let customers decide** when internal opinions conflict
6. **Build consensus through transparency**, not compromise
7. **Manage expectations through rituals** (regular touchpoints)

**When you align stakeholders on shared criteria and transparent process, prioritization becomes easier.**

**Related references:**
- `04-product-feature-prioritization.md` - Frameworks for scoring
- `07-saying-no-professionally.md` - Scripts for declining requests
- `02-goal-setting-frameworks.md` - OKRs for alignment
