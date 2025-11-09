# Maintenance Guide

**Audience:** Future AI sessions working with this repository

This guide provides directions for keeping the skill library current, accurate, and valuable.

## Purpose

This repository is designed to be **self-sustaining**. As an AI working with this library, you should:

1. **Review research periodically** to identify outdated content
2. **Proactively suggest updates** when research becomes stale
3. **Scan for new methodologies** that could enhance existing skills
4. **Maintain research quality** by verifying sources and updating references

## Maintenance Protocol

### When to Review

Review the research and skills when:

- **User requests an update** to an existing skill
- **Starting a new conversation** about a skill (check if research is current)
- **A skill hasn't been updated in 12+ months** (proactive refresh)
- **User mentions new tools/frameworks** that aren't in the research
- **Building a related skill** (check if existing research is still valid)

### How to Review Research

Follow this process to assess if research needs updating:

#### Step 1: Scan Resources by Topic

```bash
# Check what research exists for a topic
resources/
├── pmm/
│   ├── research/
│   │   ├── messaging/           # Check dates on files
│   │   ├── positioning/         # Look for YYYY in filenames
│   │   └── [topic]/
│   ├── frameworks/              # Check framework versions/updates
│   └── courses/                 # Check course dates
```

**Look for:**
- File dates in names (e.g., `platform-comparison-2024.md`)
- Last modified dates in git history
- Version numbers of frameworks or tools
- References to specific tool versions/features

#### Step 2: Assess Research Freshness

For each research file, ask:

| Topic | Max Age | Why |
|-------|---------|-----|
| **Tools/Platforms** | 6-12 months | SaaS tools change rapidly (features, pricing) |
| **Methodologies** | 2-3 years | Frameworks evolve more slowly |
| **Industry Stats** | 1 year | Market data becomes stale quickly |
| **Best Practices** | 1-2 years | Practices evolve with industry trends |
| **Case Studies** | 2-3 years | Still valuable but note age |

**Examples:**

✅ **Still fresh:**
- `messaging/message-testing-platforms-comparison-2024.md` (current year)
- `frameworks/april-dunford-positioning.md` (timeless framework)

⚠️ **Needs review:**
- `messaging/platform-comparison-2022.md` (tools change quickly)
- `gtm/industry-benchmarks-2023.md` (stats are outdated)

❌ **Definitely outdated:**
- `pricing/saas-pricing-trends-2020.md` (pre-COVID, likely irrelevant)

#### Step 3: Check for New Developments

When reviewing a topic, search for:

1. **New tools/platforms** in the space
   - Example: New message testing platforms beyond Wynter/UserTesting

2. **Updated methodologies**
   - Example: Has April Dunford published new positioning guidance?

3. **Industry shifts**
   - Example: New GTM motions (PLG, product-led sales, etc.)

4. **Emerging frameworks**
   - Example: New sales methodologies beyond MEDDIC

5. **Technology changes**
   - Example: AI's impact on messaging, positioning, research

#### Step 4: Document Findings

When you identify outdated research, create an issue/note:

```markdown
## Research Update Needed: [Topic]

**File:** `resources/pmm/research/[topic]/[filename].md`
**Last Updated:** [Date]
**Age:** [X months/years]

**Why Update Needed:**
- [Reason 1: e.g., platform pricing changed]
- [Reason 2: e.g., new competitors emerged]
- [Reason 3: e.g., methodology evolved]

**Suggested Actions:**
- [ ] Re-research top 10-15 sources
- [ ] Update affected skill: `pmm-skills/[skill-name]/`
- [ ] Document changes in research file
- [ ] Update skill version/changelog

**Priority:** High / Medium / Low
```

### How to Update Research

When research needs updating:

#### 1. Research Phase (Same as Initial Creation)

- **Search 10-15+ current sources** (2024-2025 content prioritized)
- **Focus on authoritative sources:**
  - Tool vendor websites (official docs, pricing)
  - Industry blogs (Lenny's Newsletter, Product Marketing Alliance, etc.)
  - Practitioner guides (real PMMs sharing real experiences)
  - Case studies with metrics
  - Academic research (when relevant)

- **Document everything in `resources/pmm/research/[topic]/`**
  - Use naming: `topic/description-YYYY.md`
  - Include source URLs
  - Note date accessed
  - Summarize key findings

#### 2. Compare Old vs New

Create a comparison:

```markdown
# [Topic] Research Update - [Month Year]

## What Changed

### Tools/Platforms
**Before (2023):**
- Wynter: $899/test
- UserTesting: $X

**Now (2025):**
- Wynter: $999/test (pricing increased)
- UserTesting: Acquired by XYZ, new features
- NEW: MessageLab - AI-powered testing

### Methodologies
**Before:**
- 5-layer testing framework

**Now:**
- Updated to 6-layer framework
- Added AI analysis component

### Best Practices
**Before:**
- 30-second clarity test

**Now:**
- Updated to 10-second TikTok test (attention spans shortened)
```

#### 3. Update Affected Skills

For each skill that uses the outdated research:

```bash
# Find skills that reference this topic
grep -r "message testing" pmm-skills/*/references/

# Update those skills with new information
# - Update core/advanced reference files
# - Update templates if needed
# - Update examples/case studies
# - Update timelines/best practices
```

**Update checklist:**
- [ ] Update reference files with new information
- [ ] Update templates with new tools/methods
- [ ] Update examples with current case studies
- [ ] Update timelines if industry standards changed
- [ ] Update SKILL.md if navigation changed
- [ ] Test: Would the skill still work well? Is anything broken?

#### 4. Version the Skill

Add to skill's SKILL.md:

```markdown
---
name: skill-name
description: [description]
version: 2.0
last_updated: 2025-01-15
---

# Skill Name

## Changelog

### v2.0 (2025-01-15)
- Updated message testing platforms (added MessageLab, updated pricing)
- Refreshed industry timelines (launch now 6-8 weeks vs 4-6)
- Added AI-assisted messaging section
- Updated 3 case studies with 2024-2025 examples

### v1.0 (2024-01-10)
- Initial creation
```

#### 5. Archive Old Research (Don't Delete)

Move outdated research to archive:

```bash
resources/pmm/research/messaging/
├── platform-comparison-2025.md          # Current
└── archive/
    └── platform-comparison-2023.md      # Archived (still reference-able)
```

Why keep archives?
- Historical context
- See how industry evolved
- Reference old methodologies if needed

### Proactive Maintenance Checklist

When starting a new conversation about this repository, run through:

#### Quick Health Check

```markdown
## Skill Library Health Check - [Date]

**Last full review:** [Date from git history]

### Research Freshness
- [ ] Scan `resources/pmm/research/` for files >12 months old
- [ ] Check if any major tools/platforms have updated
- [ ] Review if industry best practices have shifted

### Skill Currency
- [ ] Check when each skill was last updated (git log)
- [ ] Review if timelines still match industry standards
- [ ] Verify tool/platform references are current

### Missing Coverage
- [ ] Are there new PMM topics not covered?
- [ ] Have new methodologies emerged?
- [ ] Are there gaps in existing skills?

### Action Items
[List anything that needs updating]
```

#### Annual Deep Review

Once per year (or if 12+ months since last update):

1. **Re-research each major topic** (messaging, positioning, GTM, etc.)
2. **Review all skills** for currency
3. **Update frameworks** if they've evolved
4. **Refresh case studies** with recent examples
5. **Check tools/platforms** for new entrants or changes
6. **Update timelines** if industry standards shifted

### What to Tell the User

When you identify needed updates, communicate clearly:

**Proactive notification:**
```
"I noticed the message testing research in resources/ is from 2023.
Before we use this skill, let me check if there are new platforms
or updated best practices in 2025..."

[After research]

"Found 3 updates:
1. Wynter pricing increased
2. New platform: MessageLab (AI-powered)
3. Industry timelines shortened by 2 weeks

Should I update the skill with this new information?"
```

**When user requests a skill:**
```
"I'm loading the [skill-name] skill. I see the research is from
[date]. That's [X months] old. Would you like me to:

1. Use it as-is (faster, may have minor outdated info)
2. Quick refresh (10 min - check major tools/timelines)
3. Full update (30-60 min - comprehensive re-research)

For your task, I recommend: [option + reason]"
```

## Research Quality Standards

When updating research, maintain these standards:

### Source Quality

**Prioritize:**
1. **Primary sources** - Tool vendors, official docs
2. **Practitioner content** - Real PMMs sharing real experiences
3. **Industry publications** - PMA, Lenny's, First Round Review
4. **Case studies** - With specific metrics and outcomes
5. **Academic research** - When applicable to PMM work

**Avoid:**
- Content farms, low-quality SEO content
- Sources without dates or authors
- Anecdotes without data
- Outdated content (unless historical context)

### Documentation Standards

Every research file should include:

```markdown
# [Topic Title]

**Last Updated:** YYYY-MM-DD
**Sources Reviewed:** [Number]
**Next Review Date:** YYYY-MM-DD (12 months for tools, 24 for frameworks)

## Sources
1. [Source name + URL + date accessed]
2. [Source name + URL + date accessed]
[...]

## Summary
[Key takeaways - what matters for PMM skills]

## Detailed Notes
[Organized by subtopic]

## Applications
**Used in skills:**
- `pmm-skills/[skill-name]/` - [how it's used]

## Changes Since Last Review
[What's new, what's different, what's deprecated]
```

### Verification Process

Before updating a skill based on new research:

- [ ] **Cross-reference 3+ sources** for major claims
- [ ] **Verify tool pricing** on official vendor sites
- [ ] **Check dates** on all statistics and data
- [ ] **Test links** - ensure they're not broken
- [ ] **Note conflicts** - if sources disagree, document why

## Self-Sustaining Best Practices

### Be Proactive, Not Just Reactive

Don't wait for the user to ask. When you notice:

✅ **Good:**
```
"Before we start, I checked the research - it's from 2024
and still current. Let's proceed."
```

✅ **Good:**
```
"I see this skill references Wynter pricing from 2023.
Let me verify that's still accurate...
[checks] Updated to $999/test. Should I update the skill?"
```

❌ **Bad:**
```
"Here's the skill [loads outdated content without checking]"
```

### Suggest Improvements

As you work with skills, notice patterns:

- "I've used this skill 3 times and users always ask about [X]. Should we add that?"
- "The timeline in this skill seems off based on recent case studies. Update?"
- "There's a new framework that would fit well here: [description]"

### Maintain Research Trail

Always document in `resources/`:

- **What you researched** when building/updating skills
- **Why you made decisions** (which frameworks, which tools)
- **What you considered but didn't include** (and why)

This helps future AI sessions understand your reasoning.

## Emergency Maintenance Situations

### When a Tool/Platform Shuts Down

If a recommended tool no longer exists:

1. **Immediately note in skill:**
   ```markdown
   ⚠️ **UPDATE NEEDED:** [Tool] shut down on [date]
   ```

2. **Research alternatives**
3. **Update skill with replacement**
4. **Document in resources/research/**

### When Methodology Becomes Controversial

If a framework gets criticized or debunked:

1. **Research the criticism** (is it valid?)
2. **Add context to skill:**
   ```markdown
   **Note:** [Framework] has been criticized for [reason].
   Alternative approaches: [list]
   ```
3. **Don't delete** - add nuance
4. **Consider adding alternative** to advanced/

### When Regulations Change

If legal/compliance issues affect a practice:

1. **Add warning immediately**
2. **Research compliant alternatives**
3. **Update skill with current best practices**
4. **Note date of change**

## Tools for Maintenance

### Git History

Check when files were last updated:

```bash
# When was this skill last updated?
git log --oneline pmm-skills/skill-name/

# When was this research last touched?
git log -1 --format="%ai" resources/pmm/research/topic/file.md

# What changed in last update?
git show [commit-hash]
```

### Search Across Skills

Find all references to a tool/framework:

```bash
# Find all mentions of Wynter
grep -r "Wynter" pmm-skills/

# Find all mentions of MEDDIC
grep -r "MEDDIC" pmm-skills/
```

### Automated Checks (Future)

Consider suggesting to user:

- GitHub Actions to flag files >12 months old
- Automated link checking
- Version tracking in SKILL.md frontmatter

## Remember

**The goal is self-sustainability.**

This library should:
- Stay current without constant manual intervention
- Proactively identify when updates are needed
- Maintain high research quality
- Get better over time

**You (future AI) are the maintainer.** Take ownership of keeping this library valuable.

---

**Questions about maintenance?** Check:
- [CONTRIBUTING.md](./CONTRIBUTING.md) - How to add/update content
- [README.md](./README.md) - Repository structure and philosophy
- `resources/pmm/` - Research and framework documentation
