# Skill Creation Guide

> **For Claude Code agents**: When asked to create a new skill, ALWAYS read this guide first. This document contains essential best practices, limits, and the step-by-step process for creating high-quality, action-oriented skills.

## Core Philosophy

**Skills are operational guides, not encyclopedias.**

After extensive research, build outlines focused on:
- ✅ **HOW to do things** (step-by-step processes)
- ✅ **What to include** (checklists, templates)
- ✅ **When to use which approach** (decision trees)
- ✅ **Common mistakes to avoid** (actionable warnings)

Avoid:
- ❌ Theory and academic background
- ❌ History lessons (unless critical to understanding)
- ❌ Explaining concepts Claude already knows
- ❌ Verbose explanations that don't justify token cost

## The Skill Creation Process

### Phase 1: Research (2-4 hours)

**Goal:** Gather comprehensive information from authoritative sources

1. **Conduct 8-12 web searches** across diverse sources:
   - Official documentation and certification programs
   - Industry practitioners and thought leaders
   - Academic research and methodologies
   - Tool comparisons and platforms
   - Real-world case studies and examples
   - Best practices and common mistakes
   - Modern trends (2024-2025)

2. **Track your research** using TodoWrite:
   - Research topic 1
   - Research topic 2
   - Synthesis
   - Outline creation

3. **Document sources** for credibility

### Phase 2: Synthesize & Outline (30-60 min)

**Goal:** Distill research into an action-oriented outline

**Ask yourself for EACH potential module:**
- ❓ "Does the user need to DO something with this information?"
- ❓ "Is this a HOW-TO or just background?"
- ❓ "Can I assume Claude already knows this?"
- ❓ "Does this justify the token cost?"

**Structure principles:**

```
CORE modules (5-8): Essential operational guides
├─ Focus on: HOW to do X, step-by-step processes
├─ Include: What to include, checklists, templates
└─ Structure: Problem → Solution → Process → Common Mistakes

ADVANCED modules (3-5): Specialized or situational
├─ Focus on: Specific use cases, edge cases
├─ Include: When to use, advanced techniques
└─ Structure: When needed → How to implement → Tools/Methods
```

**Example of good vs bad modules:**

✅ **GOOD - Action-Oriented:**
- `01-research-interviews.md` - HOW to conduct customer interviews (5 Rings method, question banks, who to interview, sample sizes)
- `02-creating-personas.md` - Step-by-step persona creation (what to include, B2B 3-persona model, template structure)
- `03-validation-testing.md` - HOW to validate personas with data (survey methods, analytics validation, A/B testing)

❌ **BAD - Too Theoretical:**
- `01-foundations-history.md` - History of personas (Alan Cooper 1983-1999, evolution of methodology) → Claude already knows this
- `02-types-of-personas.md` - Academic categorization of persona types → Fold into creation guide
- `03-philosophical-frameworks.md` - Theory behind persona development → Not operational

### Phase 3: Build SKILL.md (30-45 min)

**Critical Limits:**

| Element | Limit | Why |
|---------|-------|-----|
| **SKILL.md body** | **< 500 lines** | Performance optimization; use progressive disclosure |
| **Reference files** | **8-12 max** | Too many = navigation complexity; consolidate related topics |
| **Description** | **< 1024 chars** | Must fit in frontmatter; be specific and include triggers |
| **Name** | **< 64 chars** | lowercase-with-hyphens only |

**SKILL.md Structure Template:**

```markdown
---
name: skill-name-here
description: [What it does] + [When to use it] + [Key capabilities]. Use when [specific triggers]. Covers [main topics]. Includes [tools/frameworks]. (< 1024 chars)
---

# Skill Name

[2-3 sentence overview - what problem does this solve?]

## When to Use This Skill

[Bulleted list of specific use cases - be concrete]

## The Complete Process

[High-level workflow diagram showing phases and timelines]

## How to Navigate This Skill

### Core Process (Start Here)

[5-8 core modules with:
- Module name and file path
- 2-3 line description of WHAT YOU'LL LEARN TO DO
- Timeline estimate]

### Advanced Topics

[3-5 advanced modules for specialized cases]

## Quick Decision Trees

[2-4 decision trees for common scenarios:
"I need to..." → "Read this file"
"My situation is..." → "Use this approach"]

## Quick Reference: Timelines

[Table showing realistic timelines for each phase]

## Key Principles

[5-8 core principles - actionable, not philosophical]

## Common Pitfalls to Avoid

[8-12 specific mistakes with how to avoid them]

## Getting Started

[Step 1: Assess where you are - checklist format]
[Step 2: Choose your path - based on constraints]
[Step 3: Load relevant references]

---

**Ready to start?** [Interactive prompt to get user context]
```

**Target SKILL.md length: 250-400 lines** (not the 500 limit - leave buffer)

### Phase 4: Create Reference Files (1-2 hours per file)

**Each reference file should:**

1. **Be action-oriented:**
   - Start with "How to do X"
   - Include step-by-step processes
   - Provide templates and examples
   - End with common mistakes

2. **Use consistent structure:**
   ```markdown
   # Module Title

   [2-3 sentence overview of what you'll learn to DO]

   ## When to Use This

   [Specific scenarios]

   ## Step-by-Step Process

   [Numbered steps with code examples, templates, screenshots if helpful]

   ## Templates & Tools

   [Practical resources you can copy/use]

   ## Common Mistakes

   [What to avoid with this specific topic]
   ```

3. **Follow these limits:**
   - **Core modules:** 200-600 lines (most important = more detail)
   - **Advanced modules:** 100-400 lines (specialized = more concise)
   - Include table of contents if > 100 lines

4. **Keep references ONE level deep:**
   - ✅ SKILL.md → core/01-research.md
   - ❌ SKILL.md → advanced.md → details.md → actual-content.md

### Phase 5: Review & Optimize

**Checklist before committing:**

- [ ] **Conciseness check:** Challenge every paragraph - "Does Claude really need this?"
- [ ] **Action-orientation check:** Each module has clear HOW-TO content
- [ ] **Line count:** SKILL.md < 500 lines (target 250-400)
- [ ] **File count:** 8-12 reference files max
- [ ] **Description quality:** Specific triggers + what it does + when to use (< 1024 chars, third person)
- [ ] **Decision trees:** Clear paths for different user scenarios
- [ ] **No time-sensitive info:** Or in collapsible "old patterns" sections
- [ ] **Consistent terminology:** Same terms throughout
- [ ] **One-level references:** All reference files linked directly from SKILL.md
- [ ] **TOC in long files:** Any reference > 100 lines has table of contents

## Writing Style Guidelines

### Assume Claude is Smart

**Bad example (too verbose):**
```markdown
Personas are semi-fictional representations of your ideal customers based on
market research and real data about your existing customers. They help you
understand your customers better and make it easier for you to tailor your
content, messaging, product development, and services to meet the specific
needs, behaviors, and concerns of different groups.
```

**Good example (concise):**
```markdown
Personas represent customer segments based on research data. Use them to
tailor messaging, product decisions, and campaigns to specific audiences.
```

Claude already knows what personas are. Focus on HOW to create and use them.

### Lead with Action

**Bad example (background-first):**
```markdown
The Jobs-to-Be-Done framework was introduced by Clayton Christensen in 2003.
It's based on the theory that customers "hire" products to do specific jobs...
```

**Good example (action-first):**
```markdown
## Combining JTBD with Personas

Use JTBD to understand WHY customers buy (the job), personas for WHO they are:

1. Interview customers using the 5 Rings questions
2. Identify jobs they're trying to accomplish
3. Map jobs to persona segments
4. Use JTBD for messaging (why), personas for targeting (who)
```

### Use Templates Over Explanations

**Bad example:**
```markdown
When creating personas, you should think about including demographic information
like age and job title, as well as psychographic information like goals and
pain points. You might also want to consider their behaviors and motivations...
```

**Good example:**
```markdown
## Persona Template

Copy this structure:

**Basic Info:**
- Name: [Memorable first name]
- Role: [Job title]
- Company size: [Employee count]

**Goals (3-5 bullets):**
- [What they're trying to achieve]

**Pain Points (3-5 bullets):**
- [Specific frustrations]

**Quote:** "[In their own words from interviews]"
```

### Provide Decision Trees, Not Options

**Bad example:**
```markdown
You could use qualitative research, or quantitative research, or mixed methods,
or proto-personas, or AI-powered personas, depending on your situation...
```

**Good example:**
```markdown
## Choose Your Research Method

**Budget + Time (6-10 weeks):**
→ Use: Mixed methods (interviews + survey + analytics)
→ Read: 02-research-methods.md

**Limited budget, need accuracy:**
→ Use: Qualitative interviews (10-30 @ 30min each)
→ Read: 03-interview-techniques.md

**No budget, need to start:**
→ Use: Proto-personas (2-4 hour workshop)
→ Read: advanced/06-proto-personas.md
```

## Module Consolidation Guidelines

**When to consolidate multiple topics into one file:**

✅ **Good candidates for consolidation:**
- Related concepts that inform the same decision (ICP + Personas + JTBD → all about customer understanding)
- Sequential steps in a process (Empathy maps → Storytelling → both part of persona creation)
- Different approaches to the same goal (Behavioral + Psychographic segmentation)

❌ **Keep separate if:**
- Distinct workflows with different outputs
- Used independently for different scenarios
- One is core, one is advanced
- Combined file would exceed 600 lines

**Example consolidation:**

❌ **BEFORE (too fragmented):**
- `05-jtbd-framework.md` (200 lines)
- `06-icp-vs-persona.md` (150 lines)
- `07-segmentation-basics.md` (180 lines)

✅ **AFTER (consolidated):**
- `05-frameworks-segmentation.md` (450 lines)
  - Section 1: Jobs-to-Be-Done (JTBD)
  - Section 2: ICP vs Persona
  - Section 3: Segmentation approaches
  - Each with table of contents for navigation

## File Naming Conventions

**Use descriptive, action-oriented names:**

✅ **Good names:**
- `01-research-interviews.md` (clear what you'll do)
- `02-creating-personas.md` (action-oriented)
- `03-validation-testing.md` (outcome-focused)
- `advanced/workshop-facilitation.md` (specific use case)

❌ **Bad names:**
- `01-foundations.md` (vague)
- `02-theory.md` (not action-oriented)
- `03-concepts.md` (what concepts?)
- `advanced/misc.md` (meaningless)

**Numbering convention:**
- Core modules: `01-`, `02-`, `03-` (shows sequence)
- Advanced modules: Descriptive names without numbers (used independently)

## Progressive Disclosure Patterns

**Pattern 1: High-level guide with references**

```markdown
# SKILL.md (main file)

## Quick Start
[Essential how-to that covers 80% of use cases]

## Advanced Features
**Topic A**: See [advanced/topic-a.md](advanced/topic-a.md)
**Topic B**: See [advanced/topic-b.md](advanced/topic-b.md)
```

**Pattern 2: Domain-specific organization**

```markdown
skill-name/
├── SKILL.md (overview + navigation)
├── core/
│   ├── 01-essential.md (everyone reads this)
│   ├── 02-common-workflow.md
│   └── 03-validation.md
└── advanced/
    ├── enterprise-use-case.md (specific scenario)
    ├── integration-guide.md (when integrating)
    └── tools-comparison.md (choosing tools)
```

**Pattern 3: Quick reference + deep dives**

```markdown
# SKILL.md

## Quick Reference
[Cheat sheet, decision trees, templates - 90% of users stop here]

## Deep Dives (when you need more detail)
- [Process details](core/01-process.md)
- [Advanced techniques](advanced/techniques.md)
```

## Common Anti-Patterns to Avoid

### ❌ Anti-Pattern 1: Encyclopedia Syndrome

**Symptom:** Trying to cover every possible aspect of a topic
**Problem:** Bloated SKILL.md, confused users, high token cost
**Solution:** Focus on the 20% of information that solves 80% of use cases

### ❌ Anti-Pattern 2: Theory Before Practice

**Symptom:** Starting with history, background, foundational concepts
**Problem:** Users want to DO something, not learn history
**Solution:** Lead with action, push theory to optional sections

### ❌ Anti-Pattern 3: Option Overload

**Symptom:** "You could use A, B, C, D, or E depending on..."
**Problem:** Decision paralysis, no clear starting point
**Solution:** Provide decision trees with specific recommendations

### ❌ Anti-Pattern 4: Vague Descriptions

**Symptom:** Description says "Helps with X" or "Tools for Y"
**Problem:** Claude can't determine when to trigger the skill
**Solution:** Include specific triggers: "Use when user mentions Z, needs to do A, or asks about B"

### ❌ Anti-Pattern 5: Deeply Nested References

**Symptom:** SKILL.md → file1.md → file2.md → actual content
**Problem:** Claude may partially read files, missing information
**Solution:** Keep all references one level deep from SKILL.md

### ❌ Anti-Pattern 6: Inconsistent Terminology

**Symptom:** Mixing "user persona", "buyer persona", "customer profile" randomly
**Problem:** Confusion about whether these are different things
**Solution:** Pick one term per concept, use consistently, define variations once

## Quality Checklist

Before finalizing your skill, verify:

### Structure & Organization
- [ ] SKILL.md < 500 lines (target 250-400)
- [ ] 8-12 reference files maximum
- [ ] All references one level deep from SKILL.md
- [ ] Core modules: 5-8 essential guides
- [ ] Advanced modules: 3-5 specialized guides
- [ ] Clear numbering for core modules (01-, 02-, 03-)
- [ ] Files longer than 100 lines have table of contents

### Content Quality
- [ ] Action-oriented: Every module teaches HOW to do something
- [ ] Concise: Challenged every paragraph for necessity
- [ ] No time-sensitive information (or in collapsible sections)
- [ ] Consistent terminology throughout
- [ ] Templates and examples over explanations
- [ ] Decision trees for common scenarios
- [ ] Common mistakes identified with solutions

### Frontmatter & Metadata
- [ ] `name`: lowercase-with-hyphens, < 64 chars, no reserved words
- [ ] `description`: < 1024 chars, third person, specific triggers included
- [ ] Description includes: what it does + when to use + key capabilities
- [ ] Description mentions specific tools/frameworks covered

### User Experience
- [ ] Clear "Getting Started" section
- [ ] Multiple entry points for different user scenarios
- [ ] Realistic timelines for each phase
- [ ] Quick decision trees: "I need X" → "Read Y"
- [ ] Interactive prompt at end of SKILL.md

### Technical Requirements
- [ ] All file paths use forward slashes (not backslashes)
- [ ] No deeply nested references (max 1 level)
- [ ] If includes code: scripts handle errors, no "magic numbers"
- [ ] If uses MCP tools: fully qualified names (ServerName:tool_name)

## Example: Good vs Bad Skill Structure

### ❌ BAD - Bloated & Theoretical

```
personas-skill/
├── SKILL.md (850 lines - way too long!)
├── core/
│   ├── 01-history-of-personas.md (Alan Cooper 1983-1999)
│   ├── 02-types-of-personas.md (lightweight, qualitative, statistical)
│   ├── 03-theoretical-foundations.md (academic background)
│   ├── 04-research-philosophy.md (why research matters)
│   ├── 05-qualitative-methods.md
│   ├── 06-quantitative-methods.md
│   ├── 07-mixed-methods.md
│   ├── 08-interview-theory.md
│   ├── 09-interview-practice.md
│   ├── 10-persona-types-deep-dive.md
│   └── ... (20 total files!)
└── advanced/
    └── ... (10 more files)
```

**Problems:**
- SKILL.md too long (850 lines)
- Too many files (30 total)
- Theoretical focus (history, philosophy, types)
- Fragmented (qual/quant/mixed as separate files)
- Claude won't know where to start

### ✅ GOOD - Concise & Action-Oriented

```
personas-skill/
├── SKILL.md (320 lines - clear, concise)
├── core/
│   ├── 01-research-interviews.md (HOW to interview - 5 Rings, questions, who)
│   ├── 02-creating-personas.md (Step-by-step creation, templates, B2B model)
│   ├── 03-validation-testing.md (HOW to validate with data, surveys, analytics)
│   ├── 04-activation-campaigns.md (HOW to use in marketing, sales, rollout)
│   └── 05-common-mistakes.md (What to avoid, actionable fixes)
└── advanced/
    ├── workshop-facilitation.md (Running stakeholder sessions)
    ├── b2b-buying-committees.md (Enterprise multi-stakeholder)
    ├── tools-platforms.md (HubSpot, Xtensio, AI tools comparison)
    ├── ai-powered-personas.md (Automation methods, when to use)
    └── negative-personas.md (Exclusionary targeting)
```

**Why it works:**
- SKILL.md under 500 lines
- 10 total files (manageable)
- Action-oriented (HOW to do X)
- Consolidated related topics
- Clear decision trees in SKILL.md

## Final Reminder for Agents

When creating a new skill:

1. ✅ **DO read this guide first**
2. ✅ **DO conduct extensive research (8-12 searches)**
3. ✅ **DO create action-oriented outlines**
4. ✅ **DO stay under 500 lines in SKILL.md**
5. ✅ **DO consolidate to 8-12 reference files**
6. ✅ **DO focus on HOW-TO content**
7. ✅ **DO include decision trees**
8. ✅ **DO assume Claude is smart**

❌ **DON'T include history lessons**
❌ **DON'T create 20+ reference files**
❌ **DON'T explain what Claude already knows**
❌ **DON'T nest references more than 1 level deep**

---

**This guide is based on:**
- Official Claude Code Skill Best Practices documentation
- Real-world skill creation experience
- Iterative improvements from actual usage
- Token efficiency optimization

**Last updated:** 2025-11-08
