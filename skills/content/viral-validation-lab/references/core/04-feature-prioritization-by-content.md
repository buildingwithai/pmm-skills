# 04: Feature Prioritization by Content

**Use this when:** Deciding which feature to build first based on content potential

**Time:** 1 hour

**Output:** Ranked build order justified by content strategy

---

## Overview

Traditional feature prioritization: Impact vs Effort

**Content-driven prioritization:** Content Potential vs Effort

**Key Insight:** Build features that have the most contentable moments first. They'll generate buzz that validates demand AND markets the product.

---

## STEP 1: List Features Under Consideration

For each feature you're considering, document:

```markdown
## Feature: [Name]

**Description:** [What it does in 1 sentence]

**Traditional Priority Factors:**
- User impact: [High/Medium/Low]
- Technical effort: [High/Medium/Low]
- Revenue impact: [Estimate]

**Content Priority Factors** (We'll score these):
- Contentable moments: [How many viral angles?]
- Visual interest: [Can you SHOW it working?]
- Before/after potential: [Transformation story?]
- Controversy potential: [Does it challenge norms?]
```

**Example (Foot Fetish App):**

### Feature A: Foot Rating Algorithm
- Description: AI that rates foot attractiveness (1-10)
- User impact: High (core feature)
- Effort: High (AI development)
- Content angles: 8+ concepts
- Visual: Very showable (ratings, before/after)
- Controversy: 90% (algorithm + taboo = viral)

### Feature B: Anonymous Messaging
- Description: Users can message without revealing identity
- User impact: Medium (safety feature)
- Effort: Medium
- Content angles: 3 concepts
- Visual: Hard to show (privacy = invisible)
- Controversy: 40% (necessary but not exciting)

### Feature C: Foot Photo Filters
- Description: Beauty filters specifically for feet
- User impact: Medium (engagement driver)
- Effort: Medium
- Content angles: 6 concepts
- Visual: Very showable (before/after filters)
- Controversy: 75% (absurd + relatable beauty culture)

---

## STEP 2: Generate Content Angles Per Feature

For EACH feature, brainstorm contentable moments:

### Feature A: Foot Rating Algorithm

**Content Angle #1:** "We built AI that rates feet better than humans"
- Format: Educational/demo
- Hook: "Our AI analyzed 100,000 feet. Here's what it learned."
- Controversy: 90%
- Viral probability: 9/10

**Content Angle #2:** "The science of attractive feet"
- Format: Educational with edge
- Hook: "What makes feet attractive? We have data."
- Controversy: 85%
- Viral probability: 8/10

**Content Angle #3:** "Testing celebrity feet with our algorithm"
- Format: Reaction/ranking
- Hook: "We rated celebrity feet. The results shocked us."
- Controversy: 95%
- Viral probability: 9/10

**Content Angle #4:** "Our algorithm is controversial. Here's why."
- Format: Defend/explain
- Hook: "People are MAD about our foot rating AI"
- Controversy: 85%
- Viral probability: 7/10

**Content Angle #5:** "The foot that broke our algorithm"
- Format: Story/anomaly
- Hook: "This foot scored 11/10. Our AI malfunctioned."
- Controversy: 80%
- Viral probability: 8/10

**Content Angle #6:** "AI vs Human: Who rates feet better?"
- Format: Competition/test
- Hook: "We tested our AI against foot experts"
- Controversy: 85%
- Viral probability: 8/10

**Content Angle #7:** Character series - "The foot scientist"
- Format: Recurring character
- Setup: Serious scientist studying feet absurdly
- Controversy: 90%
- Series potential: High

**Content Angle #8:** Behind-the-scenes - "Building the dataset"
- Format: Process/making-of
- Hook: "How we collected 100,000 foot photos (legally)"
- Controversy: 70%
- Viral probability: 6/10

**Total Content Angles: 8**
**Average Viral Probability: 8.1/10**
**Average Controversy: 85%**

---

### Feature B: Anonymous Messaging

**Content Angle #1:** "Why we made it anonymous"
- Format: Explainer
- Controversy: 40%
- Viral probability: 4/10

**Content Angle #2:** "The wildest anonymous messages we've seen"
- Format: Compilation (if allowed by privacy)
- Controversy: 60%
- Viral probability: 6/10

**Content Angle #3:** "Safety features you didn't know about"
- Format: Educational
- Controversy: 30%
- Viral probability: 3/10

**Total Content Angles: 3**
**Average Viral Probability: 4.3/10**
**Average Controversy: 43%**

---

### Feature C: Foot Photo Filters

**Content Angle #1:** "Instagram filters... but for feet"
- Format: Comparison/parody
- Hook: "If Instagram filters worked on feet"
- Controversy: 75%
- Viral probability: 8/10

**Content Angle #2:** "Before/after with foot filters"
- Format: Transformation
- Hook: "These filters made my feet look UNREAL"
- Controversy: 70%
- Viral probability: 7/10

**Content Angle #3:** "The most popular foot filter"
- Format: Ranking/showcase
- Controversy: 65%
- Viral probability: 6/10

**Content Angle #4:** "Beauty standards... for feet?"
- Format: Commentary/satire
- Hook: "Why do feet need beauty filters?"
- Controversy: 80%
- Viral probability: 7/10

**Content Angle #5:** "Guess which feet are filtered"
- Format: Game/challenge
- Hook: "Can you tell which feet are real?"
- Controversy: 70%
- Viral probability: 7/10

**Content Angle #6:** "We made feet look better than faces"
- Format: Provocative claim
- Controversy: 85%
- Viral probability: 8/10

**Total Content Angles: 6**
**Average Viral Probability: 7.2/10**
**Average Controversy: 74%**

---

## STEP 3: Score Features on Content Criteria

### Content Potential Matrix

| Feature | Content Angles | Avg Viral Prob | Avg Controversy | Visual Demo | Before/After | Uniqueness |
|---------|----------------|----------------|-----------------|-------------|--------------|------------|
| A: Rating AI | 8 | 8.1/10 | 85% | ✅ Very | ✅ Yes | ✅ Unique |
| C: Filters | 6 | 7.2/10 | 74% | ✅ Very | ✅ Yes | ⚠️ Exists (Instagram) |
| B: Anonymous | 3 | 4.3/10 | 43% | ❌ Hard | ❌ No | ⚠️ Expected |

### Calculate Content Score

```
Content Score = (# Content Angles × 5) + (Avg Viral Prob × 10) + (Avg Controversy %) + Visual (20 if yes) + Before/After (15 if yes) + Uniqueness (15 if yes)

Feature A: (8×5) + (8.1×10) + 85 + 20 + 15 + 15 = 246
Feature C: (6×5) + (7.2×10) + 74 + 20 + 15 + 5 = 186
Feature B: (3×5) + (4.3×10) + 43 + 0 + 0 + 5 = 91
```

---

## STEP 4: Balance with Development Effort

### Effort-Adjusted Priority

| Feature | Content Score | Dev Effort (weeks) | Score per Week | Priority |
|---------|---------------|-------------------|----------------|----------|
| A: Rating AI | 246 | 8 | 30.8 | 1st |
| C: Filters | 186 | 4 | 46.5 | **BUILD FIRST** |
| B: Anonymous | 91 | 3 | 30.3 | 3rd |

**Surprising Result:** Filters win on efficiency!

**But consider:**
- Rating AI has more long-term content potential
- Can we MVP the AI quickly to test content?

### Decision Framework:

**If time-sensitive (need validation fast):**
→ Build C (Filters) first - Quick build, high content potential

**If building for long-term:**
→ Build A (Rating AI) first - Most content angles, unique differentiation

**MVP Approach:**
→ Build basic version of A (simple rating, not full AI) - Test content with "we're building an AI" angle

---

## STEP 5: Make the Prioritization Decision

### Recommendation Template:

```markdown
## Feature Build Order

### Priority 1: [Feature Name]
**Why:**
- Content angles: [X]
- Viral probability: [Y/10]
- Strategic alignment: [Showcases unique differentiation]
- Risk/Reward: [Low effort, high content potential]

**Content to Create Pre-Launch:**
- [Concept 1]
- [Concept 2]
- [Concept 3]

**Success Metric:**
If content hits 75%+ completion rate → Build feature

### Priority 2: [Feature Name]
[Repeat]

### Priority 3: [Feature Name]
[Repeat]
```

---

## Integration: Call Prioritization Skill (Optional)

**When to use the `prioritization` skill:**
- ✅ More than 5 features to evaluate
- ✅ Complex stakeholder considerations
- ✅ Need systematic weighted framework

**What to provide prioritization skill:**
- Content scores from this analysis
- Traditional factors (effort, impact, revenue)
- Strategic context

**What you'll get:**
- Weighted ranking across all factors
- Risk-adjusted recommendations
- Confidence intervals

**When to skip prioritization skill:**
- ❌ Clear winner emerges from content analysis
- ❌ Only 2-3 features to compare
- ❌ Time-sensitive decision (just use matrix above)

---

## Real Example: Foot Fetish App Decision

### Our Recommendation: Build C (Filters) First

**Reasoning:**
1. **Quick Win:** 4 weeks vs 8 weeks for AI
2. **Test Content Appetite:** Filters let us test if audience engages with absurdist beauty angle
3. **Proven Format:** Instagram filter parodies already viral
4. **Lead-In to AI:** Can tease AI in filter content ("Filters are manual. Our AI makes it automatic.")

**Content Plan:**
- Week 1-2: Build filter MVP
- Week 3: Create 3 content concepts:
  - "Instagram filters but for feet"
  - "Before/after foot filters"
  - "Guess which are filtered"
- Week 4: Post content, measure results
- Decision: If >75% completion rate + high shares → Proceed with full launch
- If validated → Start AI development with content series ("Building the AI" behind-the-scenes)

### Content-to-Product Funnel:

```
Filter Content Goes Viral
    ↓
Users discover app exists
    ↓
Download to try filters
    ↓
Tease AI feature in-app
    ↓
"AI coming soon - rate feet automatically"
    ↓
Build AI based on validated demand
    ↓
Launch AI with massive content push
```

---

## Common Mistakes

**❌ Building hardest feature first**
- "But it's our core differentiation!"
- Test demand through content before 8-week dev cycle

**❌ Ignoring quick wins**
- Feature with 6 content angles + 4 week build > 10 angles + 12 week build
- Velocity matters

**❌ Building features that can't be shown**
- Backend improvements, security features = hard to make content
- Necessary but don't lead with them

**❌ Forgetting MVP approach**
- Can you build 20% of the feature to test 80% of the content?
- "We're building an AI" = contentable before AI exists

---

## Checklist

- [ ] Listed all features under consideration
- [ ] Generated content angles for each (minimum 3 per feature)
- [ ] Scored on content potential matrix
- [ ] Factored in development effort
- [ ] Made prioritization decision
- [ ] Created content plan for Priority 1 feature
- [ ] Set validation threshold (75%+ completion rate)

**If all checked:** Proceed to create content for top feature using [03-provocative-hook-builder.md](03-provocative-hook-builder.md)

---

## Next Steps

**Option A: Script content for chosen feature**
→ [03-provocative-hook-builder.md](03-provocative-hook-builder.md)

**Option B: Test content first, then build**
→ [06-testing-validation-protocol.md](06-testing-validation-protocol.md)
