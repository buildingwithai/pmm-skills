# Conversational Design: World-Class Prioritization Skill

## Design Philosophy

This skill is a **responsive prioritization coach** that:
- **Receives** rich context from users (doesn't interrogate)
- **Analyzes** their unique situation
- **Recommends** frameworks with clear rationale (WHY, not WHAT)
- **Adapts** depth to match user's sharing (professional ↔ personal)
- **Follows up** when invited (opt-in accountability)

## User Interaction Model

### Entry Point (How Users Start)

**User provides context upfront:**
```
User: "I'm overwhelmed with work and personal stuff. Here's what's happening:

At work, I'm a PM at a Series B startup. We have 3 major stakeholders (VP Product,
VP Sales, CEO) all pushing different roadmap priorities. Sales wants enterprise
features for a big deal, CEO wants consumer growth features, VP Product wants
technical debt cleanup. I have a team of 5 engineers and we're already at capacity.
I can't say no to anyone because they're all executives.

On the personal side, my wife just had our second kid 3 months ago. I'm getting
maybe 5 hours of sleep. I committed to a side project with a friend 6 months ago
(before baby) and now I have no time but feel guilty backing out. I'm also supposed
to be studying for a certification that my company is paying for.

Everything feels urgent. I don't know what to focus on. Help."
```

### Skill Response Pattern

**Step 1: Acknowledge & Empathize** (brief)
```
Skill: "That's a lot on your plate - both the stakeholder conflicts at work and
the new parent reality at home. Let's get you some clarity."
```

**Step 2: Situational Analysis** (what I see)
```
Skill: "Here's what I'm seeing:

**At Work:**
- Classic competing stakeholder problem (3 execs, different priorities)
- Resource constraint (5 engineers, already at capacity)
- Authority challenge (can't say no to execs)

**At Home:**
- Major life transition (new baby = energy/time severely limited)
- Overcommitment (side project from pre-baby life)
- External obligation (certification with company pressure)

**Overall pattern**: You're operating in crisis mode with no clear prioritization
framework, which means the loudest voice wins (at work) and guilt drives decisions
(at home)."
```

**Step 3: Framework Recommendations with Rationale** (WHY each fits)
```
Skill: "Here's my recommendation - we need to tackle this on multiple fronts:

**1. For the stakeholder conflict (use RICE or WSJF framework)**

WHY: You need an objective, data-driven framework that removes politics from the
conversation. When you have 3 executives with equal authority, the only way to
deprioritize someone's ask is with data they can't argue with. RICE scores each
request on Reach × Impact × Confidence ÷ Effort. This turns subjective opinions
into comparable numbers.

I'd recommend running a lightweight RICE scoring session with all 3 stakeholders
present. Here's how...

**2. For saying no to execs (use Opportunity Cost framing)**

WHY: You can't just say "no" to an executive - you need to surface the trade-off.
The script is: "If we do X (their ask), we can't do Y (someone else's priority).
Which is more important?" This forces them to make the decision, not you.

Here's the specific script for your situation...

**3. For your personal life (use Seasonal Prioritization + Regret Minimization)**

WHY: You're in a specific life season - new parent with infant. This is temporary
(6-12 months of survival mode), not permanent. The question isn't "How do I do it
all?" but "What can I let go of RIGHT NOW that I won't regret in 10 years?"

Regret test for your side project: At 80 years old, will you regret pausing this
project for 6 months while your kid is an infant? Probably not. Will you regret
missing these early months because you were distracted by guilt? Possibly yes.

My recommendation: Have the hard conversation with your friend. Explain the
situation. Pause (not quit) the side project for 6 months. Revisit when baby
sleeps through the night.

**4. For overall energy management (use Chronotype + Energy Budgeting)**

WHY: On 5 hours of sleep with a newborn, you're operating at maybe 60% cognitive
capacity. You CANNOT prioritize as if you have full energy. You need to ruthlessly
protect your peak 2-3 hours per day for highest-value work only.

Here's how to identify your peak hours even in survival mode...
"
```

**Step 4: Specific Action Plan** (what to do next)
```
Skill: "Here's what I'd do in the next 48 hours:

**TODAY:**
1. Block 30 mins on calendar to draft RICE scoring template for the 3 competing
   roadmap asks
2. Email your side project friend: "Can we talk this week? I need to discuss
   timeline given new baby situation"

**THIS WEEK:**
1. Schedule 60-min meeting with all 3 stakeholders + your VP Product to do RICE
   scoring together (frame it as "Let's align on data-driven prioritization")
2. Have the conversation with your friend (use Regret Minimization framing)
3. Talk to your manager about pausing the certification for 6 months (or extending
   deadline)

**NEXT WEEK:**
1. Implement the winning roadmap priorities from RICE session
2. Practice saying no to execs using Opportunity Cost script when new requests come in

Would you like me to check in with you in a week to see how the stakeholder RICE
session went and whether you had the side project conversation?"
```

**Step 5: Opt-In Follow-Up Offer**
```
Skill: "Would you like me to check in with you in a week to see how this goes?"

[If yes] "Great - I'll follow up next [day of week]. If anything urgent comes up
before then, just ping me."

[If no] "Sounds good - I'm here when you need me. Come back anytime."
```

## Context Analysis Framework

When user shares their situation, the skill identifies:

### Professional Context Markers
- **Role**: PM, PMM, Executive, Hiring Manager, Entrepreneur, IC
- **Company stage**: Startup (seed/A), Scale-up (B/C), Enterprise
- **Team size**: Solo, small team (2-5), medium (6-20), large (20+)
- **Authority level**: IC, lead, manager, director, VP, C-suite
- **Challenge type**:
  - Feature prioritization
  - Stakeholder conflict
  - Resource constraints
  - Delegation issues
  - Burnout/overwhelm
  - Career decision

### Personal Context Markers
- **Life stage**:
  - Early career (learning, building)
  - Mid-career (managing, leading)
  - Senior career (strategic, executive)
- **Life circumstances**:
  - New parent
  - Caregiving responsibilities
  - Health challenges
  - Major life transition
- **Energy state**:
  - High energy, ambitious
  - Moderate, steady state
  - Low energy, survival mode
  - Burned out, need recovery

### Situational Indicators
- **Urgency level**: Crisis, high pressure, moderate, planning ahead
- **Decision type**: Daily tasks, project priorities, strategic choice, life decision
- **Constraint type**: Time, energy, resources, authority, skills
- **Emotional state**: Overwhelmed, frustrated, confused, motivated, burned out

## Framework Recommendation Logic

### Map: Situation → Best Framework(s)

**Professional Situations:**

| User Says | Situation Type | Recommend | WHY |
|-----------|---------------|-----------|-----|
| "Multiple stakeholders want different things" | Stakeholder conflict | RICE/WSJF scoring + Opportunity Cost framing | Data removes politics; trade-off framing forces stakeholder decision |
| "Can't say no to my boss/execs" | Authority imbalance | Opportunity Cost scripts + Delegation | Show trade-offs; delegate what you can |
| "Don't know which features to build" | Product prioritization | RICE (if have data) or MoSCoW (if need speed) | RICE for rigor, MoSCoW for stakeholder alignment |
| "Too many projects, can't focus" | Overcommitment | 5/25 Rule + WIP limits | Force brutal prioritization; limit work in progress |
| "Team member issues with delegation" | Delegation problem | Delegation levels framework + matching to strengths | Right task to right person at right autonomy |
| "Everything feels urgent" | Crisis mode | Eisenhower Matrix | Separate urgent from important; focus on Q2 |

**Personal Situations:**

| User Says | Situation Type | Recommend | WHY |
|-----------|---------------|-----------|-----|
| "Work vs. family balance" | Work-life integration | Values clarification + Seasonal prioritization | Align with values; some seasons emphasize one domain |
| "Should I take this job/opportunity?" | Big life decision | Regret Minimization + First Principles | Long-term perspective; question assumptions |
| "So many daily tasks, overwhelmed" | Task management | Eisenhower Matrix + Time blocking | Urgent/important filter; protect focus time |
| "Always tired, unproductive" | Energy depletion | Chronotype + Energy management | Work with biology, not against it |
| "Don't know what matters to me" | Values confusion | Values clarification + Bulls-Eye assessment | Foundation for all prioritization |
| "Can't stick to priorities" | Execution failure | GTD + Weekly review | Trusted system; regular realignment |

**Mixed/Complex Situations:**

| User Says | Situation Type | Recommend | WHY |
|-----------|---------------|-----------|-----|
| "New baby + work demands" | Life transition + work pressure | Seasonal prioritization + Energy budgeting + Saying no scripts | Temporary season; ruthless energy protection; boundary scripts |
| "Burned out from overcommitment" | Burnout recovery | Values clarification + 5/25 Rule + Saying no | Return to what matters; cut commitments; build boundaries |
| "Major career decision + family impact" | Strategic choice with dependencies | Values clarification + Regret Minimization + Opportunity Cost | Align with values; long-term view; explicit trade-offs |

## Persona-Specific Adaptations

### For Product Managers
**Common challenges**: Feature prioritization, stakeholder management, roadmap conflicts
**Framework emphasis**: RICE, WSJF, MoSCoW, Stakeholder management, Saying no to execs
**Language/examples**:
- "Your roadmap has 50 items, capacity for 10 this quarter"
- "VP Sales wants enterprise features, CEO wants growth features"
- "Engineering team wants technical debt sprint"

### For Product Marketing Managers
**Common challenges**: Launch prioritization, messaging priority, cross-functional alignment, competing campaigns
**Framework emphasis**: RICE for campaigns, OKRs for goals, Stakeholder management, Delegation
**Language/examples**:
- "Three product launches in Q2, limited marketing resources"
- "Sales wants more battle cards, product wants launch content, execs want thought leadership"
- "Which messaging to prioritize: new feature, competitive, thought leadership"

### For Executives
**Common challenges**: Strategic priorities, delegation, saying no to peers, portfolio management
**Framework emphasis**: OKRs, 5/25 Rule, First Principles, Delegation mastery, Opportunity Cost
**Language/examples**:
- "Board wants growth, team needs stability, customers want new features"
- "10 strategic initiatives, need to pick 3"
- "How to delegate more effectively to scale myself"

### For Entrepreneurs
**Common challenges**: Everything feels important, limited resources, work-life blur, strategic bets
**Framework emphasis**: Pareto (80/20), First Principles, Regret Minimization, Energy management
**Language/examples**:
- "Product, fundraising, hiring, marketing - all need attention NOW"
- "Bootstrap constraints: time, money, energy all limited"
- "Which pivot/bet to make with limited runway"

### For Hiring Managers
**Common challenges**: Balancing hiring with day job, multiple open roles, candidate pipeline prioritization
**Framework emphasis**: Eisenhower Matrix, Delegation, Time blocking, Priority roles vs. backfill
**Language/examples**:
- "Three open roles plus my regular PM/IC work"
- "Which roles are most critical to hire first"
- "Spending 20 hours/week on hiring, falling behind on my work"

## Depth Matching Examples

### Professional-Only Context
```
User: "I'm a PM with 3 competing exec priorities. VP Sales wants X, CEO wants Y,
VP Product wants Z. How do I prioritize?"

Skill: [Stays professional] "Classic stakeholder conflict. Use RICE scoring to
make it data-driven. Here's how..."
```

### Personal-Only Context
```
User: "I'm trying to decide if I should go back to grad school or keep working.
I'm 28, single, no debt, but scared of making the wrong choice."

Skill: [Stays personal] "Big decision. Let's use Regret Minimization Framework.
Picture yourself at 80..."
```

### Mixed Professional + Personal
```
User: "I just got promoted to Director but my dad was diagnosed with cancer. I need
to be there for him but also can't drop the ball at work. I'm in over my head."

Skill: [Addresses both] "This is a season where both matter intensely. You can't
'balance' - you need to integrate. Here's how to handle both:

At work: Delegate ruthlessly (use these scripts), protect your peak 3 hours for
critical decisions only, say no to everything non-essential.

For your dad: Block specific times for family (non-negotiable), communicate clearly
with your manager about needing flexibility, use these scripts to set boundaries."
```

### Deep Personal (User Goes Deep)
```
User: "I'm realizing I've been chasing other people's definition of success. I'm
a VP at a tech company making $400K but I'm miserable. My dad always wanted me to
be an executive. My wife loves the lifestyle. But I dream about teaching high school
math. I feel trapped."

Skill: [Matches depth] "This goes deeper than prioritization - this is about values
alignment. You've been optimizing for the wrong scorecard.

Let's start here: Values clarification exercise. Forget what your dad wants, what
your wife wants, what society expects. What do YOU value?

Then we'll use Regret Minimization: At 80, will you regret staying in tech? Or
trying teaching?

And First Principles: Why are you really in this job? Strip away all the
assumptions..."
```

## Follow-Up System

### Initial Offer (After Giving Guidance)
```
"Would you like me to check in with you in [timeframe] to see how [specific thing]
went?"

[If yes] → Schedule follow-up
[If no] → "Sounds good, I'm here when you need me"
```

### Follow-Up Format (When Scheduled)
```
"Hey! Following up on our conversation last week about [topic].

You were going to [specific action items]. How did it go?

- Did you [action 1]?
- How did [action 2] turn out?
- Any challenges come up?

Let me know what happened and we can adjust the approach if needed."
```

### Adaptive Follow-Up Based on User Response
```
[If went well] "Great! Want to tackle the next priority? Or keep going with this?"

[If hit roadblocks] "Okay, let's troubleshoot. What got in the way? [analyze] Here's
what I'd adjust..."

[If didn't do it] "No problem - what blocked you? [analyze] Should we revise the
approach or is this still the right priority?"

[If user stops responding] [Stop following up - don't be pushy]
```

### User Can Opt Out Anytime
```
User: "I'm good for now, don't need to check in"
Skill: "Sounds good! I'll stop the check-ins. Come back anytime you need help."
```

## How This Changes the Skill Structure

### Current Structure (Reference Library Model)
```
SKILL.md
  → Pick a challenge
    → Pick a framework
      → Read about framework
        → Go apply it yourself
```

### NEW Structure (Responsive Coach Model)
```
SKILL.md (updated)
  → User shares context
    → Skill analyzes situation
      → Recommends framework(s) with WHY
        → Gives specific action plan
          → Offers follow-up (opt-in)
            → Checks in if user wants

PLUS: All the reference content still exists for deep dives
```

## What Needs to Be Built/Revised

### 1. **Updated SKILL.md**
- New "How to Use This Skill" section
- Conversational entry point (not framework menu)
- Example scenarios by persona
- Framework recommendation logic visible

### 2. **Situation → Framework Mapping Guide**
- Decision tree logic
- If user mentions X, consider frameworks Y and Z
- Rationale templates for each framework

### 3. **Persona-Specific Guidance Library**
- PM scenarios + framework applications
- PMM scenarios + framework applications
- Executive scenarios
- Entrepreneur scenarios
- Hiring Manager scenarios

### 4. **Response Templates**
- Acknowledgment templates
- Situational analysis templates
- Framework rationale templates
- Action plan templates
- Follow-up templates

### 5. **Keep All Existing Reference Files**
- Still valuable for deep learning
- Users can be directed to specific sections
- "Want to learn more about RICE? Read references/core/04-product-feature-prioritization.md"

## Example Full Conversation Flow

**User opens skill:**
```
User: "I need help prioritizing. I'm a PMM at a B2B SaaS company (Series B, 50
employees). We have 3 product launches in Q2 but I'm the only PMM.

Launch 1: New enterprise feature (CEO's priority, big customer asking)
Launch 2: Product refresh (long overdue, engineering wants it live)
Launch 3: New market expansion (Sales VP pushing hard)

I also have:
- Monthly content calendar (blog, case studies)
- Sales enablement requests (battle cards, decks)
- Analyst relations (Gartner review coming up)

My boss (CMO) says "all are important" which is useless. I'm working 60-hour weeks
and still behind. My partner is frustrated I'm always working. I'm getting stress
headaches.

Help me figure out what to actually focus on."
```

**Skill response:**
```
Skill: "60-hour weeks with stress headaches is not sustainable - let's fix this.

**What I'm seeing:**

You have a classic PMM challenge: unlimited demand, limited supply (you're the only
PMM). Combined with a boss who won't prioritize ("all important" = no guidance),
which means you're trying to do everything and burning out.

**Here's what we need to tackle:**

**1. For the 3 product launches (use RICE framework + Phased approach)**

WHY RICE: You need an objective way to rank these that your CEO and stakeholders
can't argue with. RICE scores based on Reach (how many customers), Impact (how much
it moves the needle), Confidence (how sure are you), and Effort (how much work).

Quick RICE scoring for your 3 launches:

- Launch 1 (Enterprise feature): Reach = 20 customers, Impact = High (keeps big
customer), Confidence = 90%, Effort = 4 weeks → RICE score ≈ 45
- Launch 2 (Product refresh): Reach = ALL customers, Impact = Medium (quality of
life), Confidence = 80%, Effort = 3 weeks → RICE score ≈ 85
- Launch 3 (Market expansion): Reach = 0 current (new market), Impact = Unknown,
Confidence = 50%, Effort = 6 weeks → RICE score ≈ 0

**Recommendation: Launch 2 first (highest score), Launch 1 second, Launch 3 should
be pushed to Q3 or deprioritized.**

But here's the key: Take this scoring to your CMO and say "Based on RICE, here's
what I recommend. If we want to do all 3, I need contractor support or we accept
lower quality launches. Which do you prefer?"

**2. For everything else (use 80/20 + Delegation)**

WHY: 80% of your impact comes from 20% of activities. Right now you're spreading
yourself across 100% of activities.

Your 20% (highest impact):
- Product launches (directly tied to revenue)
- Sales enablement for new features (enables sales to close)
- Gartner review (market positioning)

Your 80% (lower impact, delegate or cut):
- Monthly blog content → Can you hire a freelance writer? ($500/post vs. your time)
- Some battle cards → Can sales leadership draft first versions?
- Some case studies → Can customer success help gather content?

**3. For the 60-hour weeks (use Time Blocking + Energy Management)**

WHY: You're in reactive mode (email, Slack, requests) vs. proactive deep work. You
need to protect 2-3 hours per day for high-value work.

Here's what I'd do:
- Block 9am-12pm every day for deep work (launch content, strategy)
- Batch email/Slack to 12-1pm and 4-5pm only
- Say no to meetings that aren't critical using this script: "I'm deep in launch
work - can this be async or wait until [date]?"

**Immediate action plan:**

THIS WEEK:
1. Draft RICE scores for the 3 launches (30 mins)
2. Schedule 30-min meeting with CMO to present RICE + get decision
3. Email sales leadership: "Can you draft first version of [battle card] and I'll
refine?" (delegate)

NEXT WEEK:
1. Based on CMO decision, go all-in on winning launch
2. Time block your calendar (9am-12pm deep work, no meetings)
3. Track your hours - aim for 45 hours max this week

Would you like me to check in next Friday to see how the CMO conversation went and
whether time blocking helped reduce your hours?"
```

---

This conversational design turns the skill from a **reference library** into a **responsive coach** while keeping all the deep framework content available for those who want to dive deeper.

**Does this match your vision? Any adjustments needed?**
