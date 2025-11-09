# Contributing to PMM Skills

Thank you for contributing to this repository! This guide will help you add new skills, research, and resources.

## Table of Contents

- [Adding a New Skill](#adding-a-new-skill)
- [Adding Research & Resources](#adding-research--resources)
- [Content Guidelines](#content-guidelines)
- [Structure Requirements](#structure-requirements)
- [Quality Standards](#quality-standards)

## Adding a New Skill

### Before You Start

**Ask yourself:**
1. Is this a **workflow** that you do repeatedly? (Good for a skill)
2. Is it **specific enough** to be actionable? (Not too broad)
3. Does it have **clear use cases** and outcomes?
4. Can you provide **templates and examples**?

If yes to all four, it's a good skill candidate!

### Step 1: Plan Your Skill

Create a simple outline:

```markdown
## Skill Name
[Your skill name - use kebab-case for folder]

## Description
[One sentence: what it does and when to use it]

## Key Components
- Framework/methodology 1
- Framework/methodology 2
- Template 1
- Template 2

## Typical Timeline
[How long does this process take?]

## Content Structure
- Core references (essential guides)
- Advanced references (optional deep dives)
- Assets (templates, scripts, checklists)
```

### Step 2: Create the Folder Structure

```bash
# Create the skill directory
mkdir your-skill-name

# Create subdirectories
mkdir -p your-skill-name/references/core
mkdir -p your-skill-name/references/advanced
mkdir -p your-skill-name/assets
mkdir -p your-skill-name/examples

# Create the main SKILL.md file
touch your-skill-name/SKILL.md
```

**Recommended structure:**
```
your-skill-name/
├── SKILL.md                    # Main entry point (REQUIRED)
├── references/
│   ├── core/                   # Essential guides (start here)
│   │   ├── 01-framework-name.md
│   │   ├── 02-methodology.md
│   │   └── 03-process-guide.md
│   └── advanced/               # Advanced topics (load as needed)
│       ├── specific-scenario.md
│       └── deep-dive-topic.md
├── assets/                     # Templates and tools
│   ├── template-name.md
│   ├── checklist.md
│   └── canvas-template.md
└── examples/                   # Real examples and case studies
    ├── example-1-company.md
    └── before-after-case.md
```

### Step 3: Write SKILL.md

This is the **entry point** for your skill. It must include YAML frontmatter.

**Template:**

```markdown
---
name: your-skill-name
description: Brief description (1-2 sentences) of what this skill does and when to use it. Should be clear enough that Claude knows when to load it.
---

# Your Skill Name

[Opening paragraph: what this skill helps you accomplish]

## When to Use This Skill

Use this skill when you need to:

- **Specific use case 1** - Brief explanation
- **Specific use case 2** - Brief explanation
- **Specific use case 3** - Brief explanation

**NOT for:** [Anti-patterns or out-of-scope scenarios]

## The Complete Process

[Optional: visual workflow or timeline]

```
PHASE 1 → PHASE 2 → PHASE 3 → PHASE 4
(timeline) (timeline) (timeline) (timeline)
```

**Total timeline:** [X weeks/months for full process]

## How to Navigate This Skill

This skill uses **progressive disclosure** - only the content you need is loaded based on your request.

### Core Process (Start Here)

1. **`references/core/01-framework-name.md`**
   - What it covers
   - When to use it
   - Timeline: X weeks/days

2. **`references/core/02-methodology.md`**
   - What it covers
   - Key concepts
   - Timeline: X weeks/days

[Continue for each core reference...]

### Advanced Topics (Load as Needed)

- **`references/advanced/specific-scenario.md`** - When you encounter X situation
- **`references/advanced/deep-dive.md`** - For expert-level work on Y

## Quick Decision Trees

### "What do I need help with?"

**[Scenario A]:**
→ Read: 01-framework → 02-methodology
→ Use: template-name, checklist

**[Scenario B]:**
→ Read: 02-methodology → advanced/deep-dive
→ Use: canvas-template

**[Scenario C]:**
→ Read: 03-process-guide
→ Use: checklist

## Assets & Templates

All templates are ready to use:

**Core Working Documents:**
- `template-name` - What it's for
- `checklist` - When to use it

**Reference Materials:**
- `canvas-template` - How to use it

## Key Principles

[3-5 core principles that guide this skill]

### 1. Principle Name

Explanation of the principle and why it matters.

### 2. Principle Name

Explanation of the principle and why it matters.

## Common Pitfalls to Avoid

1. **Pitfall name** → Why it's bad and what to do instead
2. **Pitfall name** → Why it's bad and what to do instead
3. **Pitfall name** → Why it's bad and what to do instead

## Quick Reference: Typical Timelines

[If applicable - table of activities and durations]

| Activity | Duration | Can be compressed? |
|----------|----------|-------------------|
| Activity 1 | X weeks | ✓ Yes / ⚠️ Not recommended |
| Activity 2 | X weeks | ✓ Yes / ⚠️ Not recommended |

## Getting Started

1. **Assess where you are:** [Questions to determine starting point]
2. **Load the relevant references** for your situation
3. **Use the templates** to organize your work
4. **Follow the process** - don't skip steps
5. **Test and iterate** - [what to measure]

## Support & Customization

This skill is designed to be adapted to your specific situation:

- **Adjust timelines** based on your constraints
- **Skip phases** that don't apply
- **Add company-specific sections** to templates
- **Scale process** to company size

---

**Ready to start?** Tell me what you're working on and I'll guide you to the right resources.
```

### Step 4: Create Reference Guides

Each reference guide should be a standalone Markdown file.

**Reference guide template:**

```markdown
# Guide Title

[Brief description of what this guide covers]

## When to Use This Guide

- Scenario 1
- Scenario 2
- Related to: [other guides in the skill]

## Overview

[High-level explanation of the framework/methodology]

## The Framework/Process

### Step 1: [Name]

**What:** [What you're doing]
**Why:** [Why it matters]
**How:** [Specific instructions]
**Output:** [What you should have at the end]

**Example:**
[Real example of this step in action]

### Step 2: [Name]

[Same structure as Step 1]

## Tools & Templates

For this guide, use these assets:
- `asset-name.md` - How to use it
- `template-name` - What it's for

## Common Mistakes

1. **Mistake:** [What people often do wrong]
   **Instead:** [What to do]

2. **Mistake:** [What people often do wrong]
   **Instead:** [What to do]

## Real Examples

### Example 1: [Company/Scenario]

**Context:** [Situation]
**What they did:** [Actions taken]
**Results:** [Outcomes with metrics]
**Key takeaway:** [Lesson learned]

## Next Steps

After completing this guide:
- **If [condition]** → Go to `reference-name.md`
- **If [condition]** → Use `template-name`
- **If [condition]** → See `advanced/topic.md`

## Further Reading

- [External resource 1]
- [External resource 2]
```

### Step 5: Create Assets & Templates

Templates should be **ready to use** with clear instructions.

**Template structure:**

```markdown
# Template Name

**Purpose:** What this template helps you accomplish
**When to use:** Specific scenarios
**Time to complete:** Estimated duration

## Instructions

1. [Step-by-step how to use this template]
2. [What to fill in]
3. [How to know when you're done]

## Template

---

[The actual template content with clear placeholders]

**[Section Name]**

[Placeholder with instructions]
- Example: [Your product name]
- Example: [Your target customer]

**[Section Name]**

| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| [Guidance] | [Guidance] | [Guidance] |

---

## Example

[Filled-in example so users can see what "good" looks like]

## Tips

- Tip 1
- Tip 2
- Tip 3
```

### Step 6: Add Examples

Real examples make skills actionable. Include:

- **Before/after comparisons**: Show the transformation
- **Case studies**: Real companies, real results (with metrics)
- **Filled templates**: What "good" looks like

**Example structure:**

```markdown
# Example: [Company/Scenario Name]

## Context

**Company:** [Name or "Anonymous B2B SaaS"]
**Industry:** [Sector]
**Challenge:** [What they were facing]
**Timeline:** [How long it took]

## What They Did

### Phase 1: [Name]
[Specific actions taken]

### Phase 2: [Name]
[Specific actions taken]

## Results

- **Metric 1:** [Specific improvement with %]
- **Metric 2:** [Specific improvement with %]
- **Key insight:** [Main takeaway]

## Key Takeaways

1. **Lesson 1:** [What we learn from this]
2. **Lesson 2:** [What we learn from this]

## What You Can Steal

- [Specific technique/approach to copy]
- [Specific technique/approach to copy]
```

### Step 7: Update Repository README

Add your skill to `/README.md`:

```markdown
### [Number]. [Your Skill Name]
**Status**: 🚧 In Progress / ✅ Complete

[One-paragraph description]

**Use this skill when you need to:**
- Use case 1
- Use case 2
- Use case 3

**Location**: `/your-skill-name/`

**Key Components**:
- Component 1
- Component 2
- Component 3

**Timeline**: [X weeks for typical process]

[See the skill's README for full details →](./your-skill-name/SKILL.md)
```

### Step 8: Test Your Skill

Before committing, test it:

1. **Load it with Claude:**
   ```
   "Use the [your-skill-name] skill to help me [specific task]"
   ```

2. **Check navigation:** Can you easily find what you need?

3. **Use templates:** Are they clear and actionable?

4. **Review timelines:** Are they realistic?

5. **Verify links:** Do all internal links work?

### Step 9: Commit and Document

```bash
# Add your skill
git add your-skill-name/

# Commit with clear message
git commit -m "Add [skill-name] skill

- Add core references (X guides)
- Add advanced references (Y guides)
- Include Z templates and assets
- Add example case studies
"

# Push to repository
git push origin main
```

## Adding Research & Resources

### Research (`resources/research/`)

Add industry research, analysis, and best practices:

```bash
# Create topic directory if needed
mkdir -p resources/research/[topic-name]

# Add research file with descriptive name
# Format: topic/descriptive-name-source-date.md
touch resources/research/messaging/platform-comparison-2025.md
```

**Research file template:**

```markdown
# [Title of Research]

**Source:** [Where this came from]
**Date:** [When published/accessed]
**Relevance:** [Why this matters for PMM work]

## Summary

[Key takeaways in 3-5 bullet points]

## Full Notes

[Detailed notes, organized by section]

## Application to PMM Skills

**Applies to skills:**
- [Skill name 1]: [How it relates]
- [Skill name 2]: [How it relates]

**Key frameworks/methods:**
- [What you can extract and use]

## References

- [Link to original source]
- [Related research]
```

### Frameworks (`resources/frameworks/`)

Add standalone frameworks referenced by multiple skills:

```bash
touch resources/frameworks/framework-name-creator.md
```

**Framework file template:**

```markdown
# [Framework Name]

**Creator:** [Who developed it]
**Source:** [Book/article/course]
**Best for:** [What situations this framework excels in]

## Overview

[What the framework is and why it exists]

## The Framework

[Detailed explanation of the framework components]

### Component 1: [Name]

**Definition:** [What it is]
**Purpose:** [Why it matters]
**How to apply:** [Practical steps]

[Repeat for each component]

## When to Use This Framework

- **Use when:** [Scenarios]
- **Don't use when:** [Anti-patterns]

## Example Application

[Real example of framework in action]

## Related Frameworks

- [Framework 1]: [How they relate]
- [Framework 2]: [How they complement each other]

## Used in Skills

- [Skill 1]: [How it's applied]
- [Skill 2]: [How it's applied]

## Further Reading

- [Original source]
- [Related resources]
```

### Course Materials (`resources/courses/`)

Add notes and transcripts from courses:

```bash
# Create course directory
mkdir -p resources/courses/course-name

# Add course files
touch resources/courses/course-name/README.md
touch resources/courses/course-name/module-01-notes.md
```

**Course README template:**

```markdown
# [Course Name]

**Instructor:** [Name]
**Platform:** [Where you took it]
**Date Completed:** [When]
**Recommend?** ✅ Yes / ⚠️ With caveats / ❌ No

## Course Overview

[What the course covers]

## Key Takeaways

1. [Major insight 1]
2. [Major insight 2]
3. [Major insight 3]

## Module Notes

- [module-01-notes.md](./module-01-notes.md) - [Module topic]
- [module-02-notes.md](./module-02-notes.md) - [Module topic]

## Actionable Frameworks

- **[Framework 1]**: [Brief description] → Added to `resources/frameworks/`
- **[Framework 2]**: [Brief description] → Applied in `[skill-name]` skill

## Would I Recommend?

**Pros:**
- Pro 1
- Pro 2

**Cons:**
- Con 1
- Con 2

**Best for:** [Who should take this course]
```

### Templates (`resources/templates/`)

Only add **generic, cross-skill templates** here:

```markdown
# [Template Name]

**Type:** Generic template usable across multiple PMM functions
**Used in skills:** [Skill 1], [Skill 2]

[Template content]
```

## Content Guidelines

### Writing Style

- **Clear and actionable**: Every guide should have specific steps
- **Progressive disclosure**: Don't dump everything upfront
- **Decision trees**: Help users navigate to what they need
- **Real examples**: Show, don't just tell
- **Timelines**: Include realistic time estimates

### Formatting Standards

- **Headers**: Use clear hierarchy (H2 for sections, H3 for subsections)
- **Code blocks**: Use ` ```markdown ` for templates
- **Tables**: For timelines, comparisons, frameworks
- **Lists**: For steps, use cases, examples
- **Bold**: For emphasis on key terms
- **Links**: Use relative links for internal navigation

### File Naming

- **Folders**: `kebab-case` (e.g., `go-to-market-strategy`)
- **Files**: `kebab-case.md` (e.g., `positioning-framework.md`)
- **Numbers for sequence**: `01-first-step.md`, `02-second-step.md`

### Markdown Standards

- Use ATX-style headers (`#` not `===`)
- One blank line between sections
- Use fenced code blocks (` ``` `) not indentation
- Use `**bold**` not `__bold__`
- Use `-` for unordered lists (not `*`)
- Use relative links: `[text](./path/file.md)` not absolute

## Structure Requirements

### Required Files

Every skill MUST have:
- ✅ `SKILL.md` with YAML frontmatter
- ✅ At least one reference guide
- ✅ At least one template or asset

### Recommended Structure

Skills SHOULD have:
- Clear "When to Use" section
- Decision trees or navigation guides
- Progressive disclosure (core → advanced)
- Real examples or case studies
- Realistic timelines

### YAML Frontmatter Requirements

```yaml
---
name: skill-name           # REQUIRED: kebab-case, matches folder name
description: "Clear, specific description of what this skill does and when to use it. Should be 1-2 sentences max. Focus on outcomes and use cases."  # REQUIRED: helps Claude know when to load this skill
---
```

## Quality Standards

### Before Submitting

**Content Checklist:**
- [ ] SKILL.md has valid YAML frontmatter
- [ ] Clear "When to Use This Skill" section
- [ ] Navigation guide or decision trees included
- [ ] At least one template or asset
- [ ] Real examples or case studies (if applicable)
- [ ] Realistic timelines included
- [ ] All internal links work
- [ ] No placeholder content (or marked as WIP)

**Structure Checklist:**
- [ ] Follows recommended folder structure
- [ ] Files use kebab-case naming
- [ ] Core vs. advanced references separated
- [ ] Assets in `/assets/` folder
- [ ] Examples in `/examples/` folder (if applicable)

**Documentation Checklist:**
- [ ] Added skill to main README.md
- [ ] Updated "Available Skills" section
- [ ] Included timeline and key components
- [ ] Links to SKILL.md work

### Review Process

1. **Self-review**: Use checklists above
2. **Test with Claude**: Load the skill and verify it works
3. **Peer review** (if applicable): Have another PMM review
4. **Commit**: Use clear commit messages

## Tips for Great Skills

### Do's ✅

- **Start with use cases**: Make it immediately clear when to use this skill
- **Provide templates**: Give users something to work with
- **Include real examples**: Show what "good" looks like
- **Add timelines**: Help users estimate effort
- **Use progressive disclosure**: Don't overwhelm with info upfront
- **Link internally**: Connect related guides and assets
- **Keep it focused**: One skill, one main workflow

### Don'ts ❌

- **Don't create mega-skills**: If it does too much, split it
- **Don't skip templates**: Theory alone isn't helpful
- **Don't forget navigation**: Users need help finding content
- **Don't use jargon**: Explain acronyms and concepts
- **Don't leave placeholders**: Mark incomplete sections as WIP
- **Don't duplicate**: Check if content belongs in shared `resources/`

## Getting Help

Questions about contributing?

1. **Look at existing skills**: `multi-audience-product-messaging` is a great example
2. **Check the main README**: Philosophy and structure guidance
3. **Open an issue**: Ask questions before investing time
4. **Start small**: Create a minimal skill first, expand later

## Versioning and Updates

### Updating Existing Skills

To update a skill:

```bash
# Edit the files you need to change
vi your-skill-name/references/core/01-guide.md

# Commit with descriptive message
git commit -am "Update [skill-name]: Add section on [topic]

- Added new framework to 01-guide.md
- Updated template with additional fields
- Refreshed examples with 2025 data
"
```

### Deprecating Content

If content becomes outdated:

1. **Move to `deprecated/` folder** within the skill
2. **Update SKILL.md** to remove references
3. **Add deprecation notice** in the old file:

```markdown
# [Deprecated] Old Guide Name

⚠️ **This guide has been deprecated and replaced by [new-guide.md](./new-guide.md)**

**Deprecated:** [Date]
**Reason:** [Why it's no longer relevant]
**Replacement:** [Link to new content]
```

## License

By contributing, you agree that your contributions will be licensed under the same license as the repository (MIT License).

---

**Ready to contribute?** Start by exploring existing skills, then create your own!

If you have questions, open an issue before investing significant time.
