# Strategic Decision-Making

Master the frameworks and tools for making high-quality strategic decisions with incomplete information, including MECE analysis, decision trees, and prioritization frameworks.

## Table of Contents

- [Decision-Making Principles](#decision-making-principles)
- [MECE Framework](#mece-framework)
- [Decision Trees](#decision-trees)
- [Prioritization Frameworks](#prioritization-frameworks)
- [Making Trade-offs](#making-trade-offs)
- [When to Decide vs. When to Wait](#when-to-decide-vs-when-to-wait)

## Decision-Making Principles

**Key principles for strategic decisions**:

1. **Clarity on what you're deciding**: Define the decision explicitly
2. **Defined success criteria**: How will you measure if it was the right choice?
3. **Time-bounded**: Set deadline to avoid analysis paralysis
4. **Reversibility assessment**: Is this a one-way door or two-way door?
5. **Sufficient information**: Aim for 70% of ideal information, not 100%
6. **Stakeholder alignment**: Who needs to agree, inform, or consult?

## MECE Framework

**MECE = Mutually Exclusive, Collectively Exhaustive**

Used by McKinsey, BCG, Bain for structured problem-solving.

**Mutually Exclusive**: No overlap between categories
**Collectively Exhaustive**: All possibilities covered

**How to apply MECE**:

**Step 1: Break down the problem**

Non-MECE example:
- Small businesses
- Medium businesses
- Online businesses ← Overlaps with first two!

MECE example:
- 1-10 employees
- 11-50 employees
- 51-200 employees
- 201+ employees

**Step 2: Use MECE structures**

**Common MECE frameworks**:
- **Time**: Past, Present, Future
- **Geography**: North America, Europe, Asia, Other
- **Customer type**: New, Existing, Churned
- **Process**: Awareness, Consideration, Decision, Retention
- **Financial**: Revenue, Costs, Profit

**MECE decision template**:

```
Question: Should we expand to enterprise segment?

Option 1: Yes - Full enterprise focus
  - Pros: [List]
  - Cons: [List]
  - Required resources: [List]

Option 2: No - Stay in SMB/mid-market
  - Pros: [List]
  - Cons: [List]
  - Required resources: [List]

Option 3: Hybrid - Enterprise + SMB
  - Pros: [List]
  - Cons: [List]
  - Required resources: [List]

Analysis: [Which option best achieves strategic goals?]
Decision: [Choice + rationale]
```

## Decision Trees

**When to use**: Complex decisions with multiple options and criteria

**Two types**:

### WHY Tree (Root Cause Analysis)

Find the root cause of a problem.

```
WHY is revenue growth slowing?
├─ WHY are new customer acquisitions down?
│  ├─ WHY is marketing generating fewer leads?
│  │  ├─ Budget cuts
│  │  └─ Channel effectiveness declining
│  └─ WHY is sales converting fewer leads?
│     ├─ Longer sales cycles
│     └─ More competitive pressure
└─ WHY is customer churn increasing?
   ├─ Product issues
   └─ Competitor alternatives
```

### HOW Tree (Solution Design)

Find ways to achieve a goal.

```
HOW can we achieve $10M ARR by end of year?
├─ HOW can we increase revenue from existing customers?
│  ├─ Upsell to higher tiers
│  ├─ Cross-sell additional products
│  └─ Reduce churn
├─ HOW can we acquire new customers faster?
│  ├─ Expand to new segments
│  ├─ Enter new geographies
│  └─ Increase marketing spend
└─ HOW can we increase average deal size?
   ├─ Target larger customers
   └─ Bundle products
```

**How to build decision trees**:

1. **Start with the main question** at the top
2. **Break into MECE branches** at each level
3. **Continue until actionable** (usually 3-4 levels)
4. **Quantify when possible** (size of opportunity, cost, timeline)
5. **Prioritize branches** based on impact and feasibility

## Prioritization Frameworks

### RICE Scoring

**When to use**: Feature prioritization, initiative prioritization, resource allocation

**Formula**: RICE Score = (Reach × Impact × Confidence) / Effort

**Reach**: How many people will this affect?
- Number of users/customers per time period
- Example: 1,000 customers per month = 1000

**Impact**: How much will it impact each person?
- 3 = Massive impact
- 2 = High impact
- 1 = Medium impact
- 0.5 = Low impact
- 0.25 = Minimal impact

**Confidence**: How sure are you about your estimates?
- 100% = High confidence (strong data)
- 80% = Medium confidence (some data)
- 50% = Low confidence (little data)

**Effort**: How much work is required?
- Person-months or story points
- Example: 2 person-months = 2

**Example calculation**:

```
Feature A: Enterprise SSO
- Reach: 500 customers/month
- Impact: 3 (massive - required for enterprise)
- Confidence: 100% (strong customer demand data)
- Effort: 3 person-months
- RICE Score = (500 × 3 × 1.0) / 3 = 500

Feature B: Dark mode
- Reach: 2000 customers/month
- Impact: 0.5 (low - nice to have)
- Confidence: 80% (some requests)
- Effort: 1 person-month
- RICE Score = (2000 × 0.5 × 0.8) / 1 = 800

Decision: Feature B scores higher, but strategic importance of enterprise (Feature A) may override pure RICE score
```

### ICE Scoring

**When to use**: Quick prioritization when you lack detailed data

**Formula**: ICE Score = (Impact × Confidence × Ease) / 3

**Impact**: Scale of 1-10
**Confidence**: Scale of 1-10
**Ease**: Scale of 1-10 (10 = easiest)

**Simpler than RICE**, good for rapid prioritization sessions.

### Eisenhower Matrix

**When to use**: Personal task prioritization, urgent vs. important decisions

```
             URGENT           |        NOT URGENT
         (Do immediately)     |     (Schedule/Plan)
─────────────────────────────┼─────────────────────────
IMPORTANT    │                │
(High impact)│   QUADRANT 1   │    QUADRANT 2
             │   DO FIRST     │    SCHEDULE
             │  - Crises      │  - Strategic work
             │  - Deadlines   │  - Planning
             │  - Emergencies │  - Relationship building
─────────────┼────────────────┼─────────────────────────
NOT          │                │
IMPORTANT    │   QUADRANT 3   │    QUADRANT 4
(Low impact) │   DELEGATE     │    ELIMINATE
             │  - Interrupts  │  - Time wasters
             │  - Busy work   │  - Distractions
             │  - Some emails │  - Trivial tasks
```

**Strategy**: Spend 65%+ time in Quadrant 2 (Important but Not Urgent) for strategic work.

### Value vs. Effort Matrix

**When to use**: Portfolio prioritization, project selection

```
High Value │  Quick Wins  │  Major Projects
           │  (Do first)  │  (Plan carefully)
           │      🟢      │      🟡
───────────┼──────────────┼─────────────────
           │              │
Low Value  │  Fill-ins    │  Time Sinks
           │  (Do later)  │  (Avoid)
           │      🟡      │      🔴
           │              │
           └──────────────┴─────────────────
             Low Effort      High Effort
```

**Decision framework**:
- **Quick Wins** (High Value, Low Effort): Do immediately
- **Major Projects** (High Value, High Effort): Plan and resource properly
- **Fill-ins** (Low Value, Low Effort): Do when you have spare capacity
- **Time Sinks** (Low Value, High Effort): Avoid or eliminate

## Making Trade-offs

**Principle**: Every YES is a NO to something else.

**Trade-off decision framework**:

**Step 1: Identify the trade-off**
- Option A: [Description]
- Option B: [Description]
- Why we can't do both: [Resource constraint, strategic conflict, etc.]

**Step 2: Evaluate against strategic criteria**

```
Criterion              | Weight | Option A Score | Option B Score
─────────────────────  |────────|────────────────|───────────────
Aligns with vision     |   30%  |      8         |      6
Revenue impact         |   25%  |      6         |      9
Resource available     |   20%  |      7         |      5
Competitive advantage  |   15%  |      9         |      6
Customer demand        |   10%  |      7         |      8
─────────────────────  |────────|────────────────|───────────────
Weighted Total         |  100%  |     7.4        |     6.9

Decision: Choose Option A (higher strategic alignment despite lower revenue)
```

**Step 3: Make the choice explicit**
- We choose: [Option]
- We are saying NO to: [Alternative]
- Because: [Strategic rationale]

**Common strategic trade-offs**:

- **Breadth vs. Depth**: Serve many segments lightly vs. one segment deeply
- **Growth vs. Profitability**: Invest for growth vs. optimize for margins
- **Innovation vs. Stability**: Rapid change vs. reliable execution
- **Features vs. Simplicity**: Comprehensive product vs. focused solution
- **Speed vs. Quality**: Launch fast vs. polish before launch

## When to Decide vs. When to Wait

**Decide now when**:
- ✅ You have 70%+ of information you need
- ✅ Waiting has high cost (lost opportunity, competitive risk)
- ✅ Decision is reversible (two-way door)
- ✅ Stakeholders are aligned
- ✅ Resources are available to execute

**Wait when**:
- ⏸️ Critical information is coming soon (days/weeks)
- ⏸️ Decision is irreversible (one-way door) and you're uncertain
- ⏸️ Stakeholder alignment is missing and needed
- ⏸️ Market conditions are changing rapidly
- ⏸️ You lack resources to execute either option

**Jeff Bezos: One-way vs. Two-way doors**

**One-way doors** (Type 1 decisions):
- Irreversible or very hard to reverse
- Require careful deliberation
- Examples: Entering new market, major acquisition, rebranding

**Two-way doors** (Type 2 decisions):
- Reversible with minimal cost
- Should be made quickly
- Examples: Feature experiments, marketing tests, pricing tests

**Decision velocity framework**:

```
                        High Reversibility
                               ↑
                               │
                    FAST       │      FAST
                    DECIDE     │      DECIDE
                    (Days)     │      (Weeks)
                               │
Low Impact  ←──────────────────┼──────────────────→  High Impact
                               │
                    SLOW       │      VERY SLOW
                    DECIDE     │      DECIDE
                    (Weeks)    │      (Months)
                               │
                               ↓
                        Low Reversibility
```

## Practical Exercise: Strategic Decision Worksheet

Use this template for major decisions:

```
DECISION: [State the decision clearly]

DEADLINE: [When must we decide?]

DECISION TYPE:
□ One-way door (irreversible)
□ Two-way door (reversible)

OPTIONS (MECE):
1. [Option 1]
2. [Option 2]
3. [Option 3]

EVALUATION CRITERIA:
- [Criterion 1]: Weight [%]
- [Criterion 2]: Weight [%]
- [Criterion 3]: Weight [%]

OPTION ANALYSIS:
[Use RICE, ICE, or weighted scoring]

RISKS:
Option 1:
- Risk: [Description]
- Mitigation: [How to reduce]

Option 2:
- Risk: [Description]
- Mitigation: [How to reduce]

STAKEHOLDERS:
- Must approve: [Names]
- Must be informed: [Names]
- Should be consulted: [Names]

DECISION: [Choice]

RATIONALE: [Why this option?]

TRADE-OFFS: [What are we saying NO to?]

NEXT STEPS:
1. [Action] by [Date] - Owner: [Name]
2. [Action] by [Date] - Owner: [Name]

REVIEW DATE: [When will we review this decision?]
```

## Next Steps

1. **Practice MECE thinking** on current problems
2. **Apply RICE or ICE** to your feature/initiative backlog
3. **Use trade-off framework** for next major decision
4. **Move to module 05**: Learn how to implement your strategic decisions with OKRs
