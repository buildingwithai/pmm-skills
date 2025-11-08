# Skill Design Guide

**Audience:** Anyone creating skills for this library

This guide provides architectural patterns, organizational best practices, and file limits based on Claude's official documentation and our experience building comprehensive PMM skills.

## Table of Contents

- [Token Costs & Limits](#token-costs--limits)
- [File & Folder Limits](#file--folder-limits)
- [Organizational Patterns](#organizational-patterns)
- [When to Use Which Structure](#when-to-use-which-structure)
- [Decision Framework](#decision-framework)
- [Common Pitfalls](#common-pitfalls)

---

## Token Costs & Limits

Understanding how Claude loads skills helps you design efficient structures.

### Progressive Loading Levels

From Claude's documentation, skills load in three levels:

| Level | Content | When Loaded | Token Cost | Example |
|-------|---------|-------------|------------|---------|
| **Level 1** | Metadata (YAML frontmatter) | Always (at startup) | ~100 tokens/skill | `name` and `description` |
| **Level 2** | SKILL.md body | When skill triggered | **Target: <5k tokens** | Main instructions, decision trees |
| **Level 3+** | Referenced files | As needed via bash | Effectively unlimited | `references/`, `assets/`, `examples/` |

**Key insight:** Files in Level 3+ don't consume context until Claude reads them via bash. This means you can bundle extensive content without penalty.

### SKILL.md Size Limits

**Official limits:**
- `name`: Max 64 characters
- `description`: Max 1024 characters
- SKILL.md body: **No official limit, but keep under 5k tokens**

**Practical guidance:**
- **400-500 lines** for SKILL.md is comfortable
- If your SKILL.md approaches **600+ lines**, consider:
  - Moving verbose instructions to separate files
  - Simplifying decision trees
  - Breaking skill into multiple skills

**Why keep SKILL.md lean:**
- Level 2 loading (when skill triggers) should be fast
- User scans SKILL.md to understand skill quickly
- Complex navigation suggests poor organization

### File Size Recommendations

**Individual reference files:**
- **Sweet spot:** 200-400 lines per file
- **Maximum:** 600-800 lines before considering split
- **Minimum:** 50+ lines (otherwise, merge with related content)

**Why these limits:**
- Claude loads entire file when referenced
- Large files (1000+ lines) slow down context loading
- Small files (<50 lines) create navigation overhead

---

## File & Folder Limits

### Files Per Folder

**Recommended limits:**

| Files in Folder | Assessment | Action |
|----------------|------------|--------|
| **1-5 files** | ✅ Optimal | Easy to navigate, scannable |
| **6-10 files** | ✅ Good | Still manageable |
| **11-15 files** | ⚠️ Getting crowded | Consider organizing into subfolders |
| **16+ files** | ❌ Too many | Break into logical subfolders |

**Example of too many files:**
```
references/
├── 01-file.md
├── 02-file.md
├── 03-file.md
...
├── 18-file.md        # ❌ Hard to find what you need
```

**Better organization:**
```
references/
├── phase-1-discovery/
│   ├── 01-research.md
│   ├── 02-analysis.md
│   └── 03-synthesis.md
├── phase-2-execution/
│   ├── 04-planning.md
│   └── 05-implementation.md
└── advanced/
    └── edge-cases.md
```

### Folder Depth

**Maximum depth:** 3 levels (skill root → category → subcategory → file)

```
✅ Good (2-3 levels):
skill-name/
├── SKILL.md
└── references/
    └── core/
        └── 01-file.md

⚠️ Acceptable (3 levels):
skill-name/
├── SKILL.md
└── references/
    └── phase-1/
        └── discovery/
            └── research.md

❌ Too deep (4+ levels):
skill-name/
├── SKILL.md
└── references/
    └── category/
        └── subcategory/
            └── sub-subcategory/
                └── file.md    # ❌ Hard to reference in SKILL.md
```

**Why limit depth:**
- SKILL.md references become unwieldy: `references/cat/subcat/subsubcat/file.md`
- Users get lost in deep hierarchies
- Maintenance becomes difficult

### Total Files Per Skill

**Skill size guidelines:**

| Total Files | Complexity | Guidance |
|-------------|------------|----------|
| **3-8 files** | Simple skill | Single capability, straightforward workflow |
| **9-15 files** | Moderate skill | Multi-step process, some advanced scenarios |
| **16-25 files** | Complex skill | Comprehensive workflow, many power-ups |
| **26+ files** | Very complex | Consider splitting into multiple skills |

**Example: Our messaging skill**
- Current: **12 files** (8 core + 3 advanced + SKILL.md)
- Assessment: ✅ **Moderate-to-complex**, well-organized
- Action: No split needed, good balance

**When to split a skill:**
- Skill tries to do too many unrelated things
- SKILL.md decision trees become overwhelming (>50 lines)
- Users commonly need only one section (signals they're separate skills)
- Navigation becomes confusing

**Example of skill that should split:**
```
❌ "all-of-pmm" skill with:
- Positioning (12 files)
- Competitive intelligence (8 files)
- Pricing strategy (10 files)
- GTM planning (15 files)
Total: 45 files - way too many!

✅ Split into 4 separate skills:
- multi-audience-product-messaging (12 files)
- competitive-intelligence (8 files)
- pricing-packaging (10 files)
- go-to-market-strategy (15 files)
```

---

## Organizational Patterns

Beyond basic `core/` and `advanced/`, here are proven organizational patterns for different skill types.

### Pattern 1: Core + Advanced (Default)

**Best for:** Linear workflows with optional power-ups

```
skill-name/
├── SKILL.md
├── references/
│   ├── core/              # Main sequential workflow
│   │   ├── 01-step-one.md
│   │   ├── 02-step-two.md
│   │   └── 03-step-three.md
│   └── advanced/          # Situational extras
│       ├── edge-case-handling.md
│       └── power-user-tips.md
├── assets/
└── examples/
```

**When to use:**
- Clear sequential workflow
- Most users follow the same path
- Advanced features are truly optional

**Example skills:**
- Document processing
- Code review
- Commit message generation

---

### Pattern 2: By Phase/Stage

**Best for:** Multi-phase processes with distinct stages

```
skill-name/
├── SKILL.md
├── references/
│   ├── phase-1-discovery/
│   │   ├── research.md
│   │   ├── analysis.md
│   │   └── synthesis.md
│   ├── phase-2-strategy/
│   │   ├── planning.md
│   │   └── prioritization.md
│   ├── phase-3-execution/
│   │   ├── implementation.md
│   │   └── validation.md
│   └── advanced/
│       └── optimization.md
├── assets/
└── examples/
```

**When to use:**
- Natural phase boundaries exist
- Each phase has multiple steps
- Users might start at different phases

**SKILL.md decision tree:**
```markdown
**Phase 1 (Discovery):**
→ Read: phase-1-discovery/research.md → analysis.md → synthesis.md

**Phase 2 (Strategy):**
→ Read: phase-2-strategy/planning.md

**Jumping to Phase 3:**
→ Read: phase-3-execution/implementation.md
```

**Example skills:**
- Product launch (discovery → strategy → execution → measure)
- GTM strategy (market research → positioning → launch → scale)
- Customer research (plan → recruit → conduct → analyze)

---

### Pattern 3: By Audience/Persona

**Best for:** Skills that serve multiple distinct audiences

```
skill-name/
├── SKILL.md
├── references/
│   ├── for-technical-buyers/
│   │   ├── evaluation-criteria.md
│   │   ├── technical-messaging.md
│   │   └── security-compliance.md
│   ├── for-economic-buyers/
│   │   ├── roi-business-case.md
│   │   └── executive-messaging.md
│   ├── for-end-users/
│   │   ├── ease-of-use-messaging.md
│   │   └── feature-benefits.md
│   └── shared/
│       └── core-positioning.md
├── assets/
└── examples/
```

**When to use:**
- Multiple distinct audiences with different needs
- Messaging/approach varies significantly by audience
- Users typically focus on one audience at a time

**SKILL.md decision tree:**
```markdown
**Messaging for technical buyers:**
→ Read: shared/core-positioning.md → for-technical-buyers/technical-messaging.md

**Messaging for economic buyers:**
→ Read: shared/core-positioning.md → for-economic-buyers/roi-business-case.md

**All-audience campaign:**
→ Read: shared/core-positioning.md → all audience folders
```

**Example skills:**
- Multi-audience product messaging (our current skill could use this!)
- Sales enablement (reps, managers, execs)
- Documentation (developers, admins, end-users)

---

### Pattern 4: By Framework/Methodology

**Best for:** Skills that teach/apply multiple distinct frameworks

```
skill-name/
├── SKILL.md
├── references/
│   ├── frameworks/
│   │   ├── april-dunford-positioning.md
│   │   ├── pain-claim-gain-messaging.md
│   │   ├── jobs-to-be-done.md
│   │   └── meddic-qualification.md
│   ├── workflows/
│   │   ├── positioning-workshop.md
│   │   ├── message-testing.md
│   │   └── sales-enablement.md
│   └── integration/
│       └── combining-frameworks.md
├── assets/
└── examples/
```

**When to use:**
- Multiple established frameworks/methodologies
- Frameworks can be used independently or combined
- Users might know some frameworks, not others

**SKILL.md decision tree:**
```markdown
**Learn positioning framework:**
→ Read: frameworks/april-dunford-positioning.md

**Apply Pain-Claim-Gain:**
→ Read: frameworks/pain-claim-gain-messaging.md

**Run positioning workshop:**
→ Read: workflows/positioning-workshop.md (references April Dunford framework)

**Combine frameworks:**
→ Read: integration/combining-frameworks.md
```

**Example skills:**
- Product marketing frameworks
- Sales methodologies
- Design systems (multiple frameworks for different use cases)

---

### Pattern 5: Quickstart + Comprehensive + Advanced

**Best for:** Skills where users have different time/depth needs

```
skill-name/
├── SKILL.md
├── references/
│   ├── quickstart/           # Fast track (30 min)
│   │   ├── essential-only.md
│   │   └── minimal-template.md
│   ├── comprehensive/        # Full process (2-4 weeks)
│   │   ├── 01-discovery.md
│   │   ├── 02-strategy.md
│   │   ├── 03-execution.md
│   │   └── 04-measurement.md
│   └── advanced/            # Expert-level
│       ├── optimization.md
│       └── edge-cases.md
├── assets/
│   ├── quickstart-template.md
│   └── comprehensive-template.md
└── examples/
```

**When to use:**
- Some users need quick results, others need depth
- Legitimate "fast track" vs "comprehensive" approaches exist
- Process can be compressed without sacrificing quality

**SKILL.md decision tree:**
```markdown
**Quick MVP (30 min):**
→ Read: quickstart/essential-only.md
→ Use: quickstart-template.md

**Full process (2-4 weeks):**
→ Read: comprehensive/01-discovery.md → 02-strategy.md → 03-execution.md → 04-measurement.md
→ Use: comprehensive-template.md

**Advanced optimization:**
→ Read: advanced/optimization.md
```

**Example skills:**
- Product launch (quick vs comprehensive)
- Competitive research (quick scan vs deep analysis)
- Message testing (quick validation vs rigorous study)

---

### Pattern 6: By Use Case/Scenario

**Best for:** Skills with distinct use cases that share some foundations

```
skill-name/
├── SKILL.md
├── references/
│   ├── foundations/
│   │   ├── core-principles.md
│   │   └── best-practices.md
│   ├── use-case-new-product/
│   │   ├── positioning-new.md
│   │   └── messaging-new.md
│   ├── use-case-repositioning/
│   │   ├── change-management.md
│   │   └── existing-customer-comms.md
│   ├── use-case-feature-launch/
│   │   └── feature-messaging.md
│   └── advanced/
├── assets/
└── examples/
```

**When to use:**
- Multiple distinct use cases share foundations
- Workflow differs significantly by use case
- Users typically have one specific use case

**SKILL.md decision tree:**
```markdown
**Launching new product:**
→ Read: foundations/core-principles.md → use-case-new-product/positioning-new.md

**Repositioning existing product:**
→ Read: foundations/core-principles.md → use-case-repositioning/change-management.md

**Launching feature:**
→ Read: use-case-feature-launch/feature-messaging.md
```

**Example skills:**
- Product messaging (new product vs feature vs repositioning)
- Customer onboarding (new vs expansion vs upsell)
- Content creation (blog vs whitepaper vs case study)

---

### Pattern 7: Hybrid (Phase + Advanced by Category)

**Best for:** Complex skills with phases AND multiple advanced categories

```
skill-name/
├── SKILL.md
├── references/
│   ├── core/
│   │   ├── phase-1-positioning/
│   │   │   ├── 01-framework.md
│   │   │   └── 02-workshop.md
│   │   ├── phase-2-messaging/
│   │   │   ├── 03-messaging-dev.md
│   │   │   └── 04-multi-audience.md
│   │   └── phase-3-rollout/
│   │       ├── 05-internal.md
│   │       └── 06-external.md
│   └── advanced/
│       ├── competitive/
│       │   ├── trap-setting.md
│       │   └── battle-cards.md
│       ├── testing/
│       │   ├── message-testing.md
│       │   └── platforms.md
│       └── crisis/
│           └── crisis-messaging.md
├── assets/
└── examples/
```

**When to use:**
- Core workflow has clear phases
- Many advanced topics that cluster by category
- Want to keep core clean but organize advanced topics

**SKILL.md decision tree:**
```markdown
**Phase 1 (Positioning):**
→ Read: core/phase-1-positioning/01-framework.md → 02-workshop.md

**Phase 2 (Messaging):**
→ Read: core/phase-2-messaging/03-messaging-dev.md

**Competitive positioning:**
→ Read: advanced/competitive/trap-setting.md

**Message testing:**
→ Read: advanced/testing/message-testing.md
```

**Example skills:**
- Multi-audience product messaging (could reorganize this way!)
- Full GTM strategy (phases + advanced topics)
- Customer research program (phases + specialized methods)

---

## Additional Folders to Consider

Beyond `references/`, consider these additional top-level folders:

### 1. `glossary/` - Definitions & Acronyms

**Purpose:** Quick reference for terminology, acronyms, frameworks

```
skill-name/
├── SKILL.md
├── glossary/
│   ├── acronyms.md          # PMM, GTM, ICP, TAM, SAM, SOM, etc.
│   ├── frameworks.md         # MEDDIC, JTBD, Pain-Claim-Gain
│   └── industry-terms.md     # Champion, economic buyer, P1/P2/P3
├── references/
└── assets/
```

**When to use:**
- Skill uses 10+ acronyms or specialized terms
- Terms are used across multiple reference files
- New users need quick terminology lookup

**SKILL.md reference:**
```markdown
**Not sure what MEDDIC means?**
→ See: glossary/frameworks.md

**Acronym reference:**
→ See: glossary/acronyms.md
```

**Benefits:**
- Prevents repetition of definitions across files
- One source of truth for terminology
- Claude can quickly clarify unfamiliar terms

---

### 2. `examples/` - Case Studies & Real-World Applications

**Purpose:** Separate from instructions, show real implementations

```
skill-name/
├── SKILL.md
├── references/
├── examples/
│   ├── case-study-appcues.md
│   ├── case-study-cognism.md
│   ├── before-after-messaging.md
│   └── real-workshop-transcript.md
└── assets/
```

**When to use:**
- You have 3+ real case studies or examples
- Examples are lengthy (200+ lines each)
- Users benefit from seeing real-world applications

**SKILL.md reference:**
```markdown
**Real example of this in action:**
→ See: examples/case-study-appcues.md (73% messaging improvement)
```

**Benefits:**
- Keeps instructions clean and prescriptive
- Examples don't bloat reference files
- Easy to add new examples over time

---

### 3. `assets/` - Templates, Checklists, Scripts

**Purpose:** Actionable tools and templates

```
skill-name/
├── SKILL.md
├── references/
├── assets/
│   ├── templates/
│   │   ├── messaging-canvas.md
│   │   ├── persona-matrix.md
│   │   └── timeline-template.md
│   ├── checklists/
│   │   ├── launch-checklist.md
│   │   └── workshop-prep.md
│   └── scripts/
│       ├── analyze_data.py
│       └── generate_report.py
└── examples/
```

**When to use:**
- Skill provides 5+ templates or tools
- Want to organize by type (templates vs checklists vs scripts)
- Users need quick access to specific template types

**Alternative (flat assets/):**
```
assets/
├── messaging-canvas-template.md
├── persona-matrix-template.md
├── launch-checklist.md
└── workshop-prep-checklist.md
```

**When flat is better:**
- 5 or fewer total assets
- No clear clustering by type
- All assets are similar (all templates, for example)

---

### 4. `workflows/` - End-to-End Process Guides

**Purpose:** Complete workflow orchestration that combines multiple references

```
skill-name/
├── SKILL.md
├── references/
│   ├── core/            # Individual techniques
│   └── advanced/
├── workflows/           # How to combine techniques
│   ├── full-positioning-to-launch.md
│   ├── quick-messaging-refresh.md
│   └── competitive-repositioning.md
└── assets/
```

**When to use:**
- Skill teaches individual techniques (in references/)
- Users need guidance on combining techniques for specific goals
- Multiple valid "paths" through the skill exist

**Example:**
```markdown
# references/core/01-positioning.md
[How to do positioning - standalone technique]

# references/core/02-messaging.md
[How to do messaging - standalone technique]

# workflows/full-positioning-to-launch.md
Week 1: Use 01-positioning.md to develop positioning
Week 2-3: Use 02-messaging.md to create messages
Week 4: Use 05-rollout.md to launch internally
[Complete orchestration of multiple techniques]
```

**Benefits:**
- References stay focused on single techniques
- Workflows show real-world combination
- Users can follow end-to-end or pick techniques à la carte

---

### 5. `playbooks/` - Specific Scenario Guides

**Purpose:** Pre-built guides for common scenarios

```
skill-name/
├── SKILL.md
├── references/         # General techniques
├── playbooks/         # Specific scenarios
│   ├── new-product-launch.md
│   ├── existing-product-repositioning.md
│   ├── crisis-response.md
│   └── competitive-threat.md
└── assets/
```

**When to use:**
- Users have specific, recurring scenarios
- Scenarios require customized combination of techniques
- You can provide pre-tested playbooks for common situations

**Difference from workflows:**
- **Workflows:** General process orchestration
- **Playbooks:** Specific scenario with context and tactics

**Example:**
```markdown
# Workflow: Full Positioning to Launch
[Generic: works for any product in any situation]

# Playbook: New Product Launch
[Specific: new product, no existing market presence, need awareness]
Includes:
- Positioning for net-new product
- Messaging for cold audience
- Launch sequence for unknown brand
- Metrics specific to new product
```

---

## When to Use Which Structure

Decision framework to choose the right organizational pattern:

### Start Here: Questions to Ask

**1. Is the workflow primarily sequential or branching?**
- **Sequential (A → B → C):** Use **Core + Advanced** or **By Phase**
- **Branching (if X then Y, if Z then W):** Use **By Use Case** or **By Audience**

**2. How many distinct user types or audiences?**
- **One primary user:** Use **Core + Advanced** or **By Phase**
- **2-3 distinct audiences:** Use **By Audience/Persona**
- **Many scenarios:** Use **By Use Case**

**3. How complex is the skill?**
- **Simple (3-8 files):** Use **Core + Advanced**
- **Moderate (9-15 files):** Use **By Phase** or **Core + Advanced**
- **Complex (16-25 files):** Use **Hybrid** or **By Framework**

**4. Are there multiple valid "speeds" through the skill?**
- **Yes:** Use **Quickstart + Comprehensive + Advanced**
- **No:** Use standard patterns

**5. Does the skill teach frameworks or apply them?**
- **Teaches frameworks:** Use **By Framework/Methodology**
- **Applies techniques:** Use **Core + Advanced** or **By Phase**

### Decision Tree

```
START: How many total files will this skill have?

├─ 3-8 files → Use CORE + ADVANCED (Pattern 1)
│
├─ 9-15 files → Does it have clear phases?
│   ├─ Yes → Use BY PHASE (Pattern 2)
│   └─ No → Are there distinct audiences?
│       ├─ Yes → Use BY AUDIENCE (Pattern 3)
│       └─ No → Use CORE + ADVANCED (Pattern 1)
│
└─ 16-25 files → Is there a sequential workflow + many advanced topics?
    ├─ Yes → Use HYBRID (Pattern 7)
    └─ No → Multiple frameworks or use cases?
        ├─ Frameworks → Use BY FRAMEWORK (Pattern 4)
        ├─ Use cases → Use BY USE CASE (Pattern 6)
        └─ Speed tiers → Use QUICKSTART + COMPREHENSIVE (Pattern 5)

26+ files → Consider splitting into multiple skills
```

---

## Decision Framework

Use this checklist when designing a new skill:

### Phase 1: Scope the Content

**Questions:**
- [ ] What's the primary workflow/capability?
- [ ] How many total files will I need? (rough estimate)
- [ ] Are there clear phases or stages?
- [ ] Are there multiple distinct audiences?
- [ ] Does the skill teach frameworks or apply techniques?
- [ ] Do users need different "speeds" (quick vs comprehensive)?

**Initial estimate:**
- Total files: ___
- Organizational pattern: ___
- Additional folders needed: ___

### Phase 2: Organize Core Content

**For references/ folder:**

| If you have... | Use this structure |
|---------------|-------------------|
| 1-10 files, linear workflow | `core/` + `advanced/` |
| 11+ files, clear phases | `phase-1/`, `phase-2/`, `phase-3/`, `advanced/` |
| Multiple audiences | `for-[audience]/`, `shared/` |
| Multiple frameworks | `frameworks/`, `workflows/`, `integration/` |
| Different speeds | `quickstart/`, `comprehensive/`, `advanced/` |
| Distinct scenarios | `foundations/`, `use-case-[name]/` |

**Check:**
- [ ] No folder has 16+ files
- [ ] Folder depth is 2-3 levels max
- [ ] Structure is scannable (user can guess where to look)
- [ ] SKILL.md decision trees are clear

### Phase 3: Add Supporting Folders

**Check which apply:**

- [ ] **glossary/** - Do I have 10+ acronyms or specialized terms?
- [ ] **examples/** - Do I have 3+ case studies or lengthy examples?
- [ ] **workflows/** - Do I need to show how to combine techniques?
- [ ] **playbooks/** - Do I have pre-tested guides for specific scenarios?
- [ ] **assets/** - Already required for templates

**Organize assets/ if needed:**
- [ ] 5 or fewer assets → Keep flat: `assets/template-name.md`
- [ ] 6+ assets → Organize: `assets/templates/`, `assets/checklists/`, `assets/scripts/`

### Phase 4: Validate Design

**SKILL.md check:**
- [ ] Description mentions when to use skill (max 1024 chars)
- [ ] Decision trees clearly route to files
- [ ] SKILL.md is under 500 lines
- [ ] References use relative paths: `references/core/01-file.md`

**File organization check:**
- [ ] Each reference file is 200-600 lines
- [ ] No folder has 16+ files
- [ ] Folder depth is 3 levels or less
- [ ] Total files is under 25

**Navigation check:**
- [ ] User can guess where content is by folder name
- [ ] Related content is grouped together
- [ ] Decision trees guide to right files quickly

### Phase 5: Document Structure

In SKILL.md, add a navigation guide:

```markdown
## How to Navigate This Skill

### Core Process (Start Here)
1. **references/core/01-positioning.md** - Positioning framework
2. **references/core/02-messaging.md** - Creating messages
3. **references/core/03-rollout.md** - Internal launch

### Advanced Topics (Load as Needed)
- **references/advanced/competitive.md** - Competitive positioning
- **references/advanced/crisis.md** - Crisis messaging

### Additional Resources
- **glossary/acronyms.md** - Quick reference for terms
- **examples/case-study-*.md** - Real-world applications
- **assets/templates/** - Ready-to-use templates
```

---

## Common Pitfalls

Avoid these mistakes when organizing skills:

### 1. Too Many Files at Root

**Bad:**
```
skill-name/
├── SKILL.md
├── 01-file.md
├── 02-file.md
├── 03-file.md
... [15 more files at root]
├── 18-file.md
└── assets/
```

**Why it's bad:** Hard to scan, no logical grouping

**Fix:** Group into folders by phase, audience, or category

---

### 2. Too Deep Folder Hierarchy

**Bad:**
```
references/
└── core/
    └── phase-1/
        └── discovery/
            └── research/
                └── qualitative/
                    └── interviews.md  # 6 levels deep!
```

**Why it's bad:**
- SKILL.md references are unwieldy
- Users get lost
- Hard to maintain

**Fix:** Max 3 levels: `references/phase-1-discovery/research-interviews.md`

---

### 3. Unclear Folder Names

**Bad:**
```
references/
├── part-a/        # What's in part-a?
├── part-b/
├── extras/        # What kind of extras?
└── other/
```

**Why it's bad:** Users can't guess where content is

**Fix:** Descriptive names: `phase-1-positioning/`, `advanced-competitive/`, `for-technical-buyers/`

---

### 4. Mixing Organizational Patterns

**Bad:**
```
references/
├── 01-positioning.md       # Sequential numbering
├── 02-messaging.md
├── for-technical-buyers/   # Suddenly by-audience
├── phase-3-launch/         # Now by-phase
└── advanced/
```

**Why it's bad:** Inconsistent logic, hard to navigate

**Fix:** Pick one pattern and stick with it

---

### 5. Over-Engineering Simple Skills

**Bad (for a 5-file skill):**
```
skill-name/
├── SKILL.md
├── references/
│   ├── core/
│   │   └── basics/
│   │       └── 01-intro.md
│   ├── intermediate/
│   │   └── techniques/
│   │       └── 02-advanced.md
│   └── expert/
│       └── mastery/
│           └── 03-pro.md
├── glossary/
├── examples/
├── workflows/
└── playbooks/
```

**Why it's bad:** Organizational overhead exceeds content value

**Fix:**
```
skill-name/
├── SKILL.md
├── references/
│   ├── core/
│   │   ├── 01-intro.md
│   │   └── 02-techniques.md
│   └── advanced/
│       └── 03-pro-tips.md
└── assets/
```

**Rule:** If you have <10 files, use simple Core + Advanced

---

### 6. Bloated SKILL.md

**Bad:**
```yaml
---
name: skill-name
description: ...
---

# Skill Name

[600 lines of detailed instructions in SKILL.md]
[All content duplicated in reference files]
```

**Why it's bad:**
- SKILL.md loaded every time skill triggers
- Wastes context on duplicated content
- Hard to scan

**Fix:**
- Keep SKILL.md under 500 lines
- Put detailed instructions in reference files
- SKILL.md = navigation hub, not instruction manual

---

### 7. Inconsistent File Naming

**Bad:**
```
references/
├── 01-positioning.md
├── messaging-guide.md        # No number
├── 03_rollout_internal.md    # Underscores
├── 04-TESTING.md             # Caps
└── launchExternal.md         # camelCase
```

**Why it's bad:** Hard to predict file names, looks unprofessional

**Fix:** Consistent naming convention:
- Core (sequential): `01-name.md`, `02-name.md`
- Advanced (named): `descriptive-name.md`
- All lowercase, hyphens for spaces

---

### 8. Missing Navigation in SKILL.md

**Bad:**
```yaml
---
name: skill-name
description: Does everything for PMM
---

# Skill Name

Here are all the things this skill does...

[No guidance on where to find anything]
```

**Why it's bad:** Claude doesn't know which file to load for which request

**Fix:** Add decision trees:
```markdown
## Quick Decision Trees

**Creating positioning from scratch:**
→ Read: references/core/01-positioning.md

**Testing messaging:**
→ Read: references/advanced/testing.md
```

---

## Improvement Checklist

Use this to evaluate and improve existing skills:

### Structure Review

- [ ] **File count per folder:** None have 16+ files
- [ ] **Folder depth:** Max 3 levels
- [ ] **Total files:** Under 25 (or skill is split)
- [ ] **SKILL.md size:** Under 500 lines
- [ ] **Consistent pattern:** One organizational pattern throughout

### Navigation Review

- [ ] **Clear decision trees** in SKILL.md
- [ ] **Descriptive folder names** (user can guess content)
- [ ] **Relative paths** in all references
- [ ] **Navigation guide** section in SKILL.md

### Content Organization Review

- [ ] **Related content grouped** together
- [ ] **No duplication** between SKILL.md and references
- [ ] **Glossary** if 10+ specialized terms
- [ ] **Examples** separated if 3+ case studies
- [ ] **Assets** organized if 6+ templates/tools

### Discoverability Review

- [ ] **Description** mentions when to use (not just what)
- [ ] **Keywords** in description match user language
- [ ] **Use cases** clearly listed
- [ ] **Anti-patterns** documented (when NOT to use)

---

## Examples by Skill Type

### Example 1: Simple Skill (3-8 files)

**Use case:** Git commit message generation

```
commit-message-helper/
├── SKILL.md                 # <500 lines
├── references/
│   ├── core/
│   │   ├── conventional-commits.md
│   │   └── best-practices.md
│   └── advanced/
│       └── monorepo-commits.md
└── assets/
    └── commit-template.md

Total: 6 files
Pattern: Core + Advanced (Pattern 1)
```

---

### Example 2: Moderate Skill (9-15 files)

**Use case:** API documentation

```
api-docs/
├── SKILL.md
├── references/
│   ├── phase-1-planning/
│   │   ├── api-inventory.md
│   │   └── audience-analysis.md
│   ├── phase-2-writing/
│   │   ├── endpoint-docs.md
│   │   ├── authentication.md
│   │   └── examples.md
│   ├── phase-3-publishing/
│   │   ├── openapi-spec.md
│   │   └── developer-portal.md
│   └── advanced/
│       └── versioning-strategy.md
├── assets/
│   ├── endpoint-template.md
│   └── openapi-starter.yaml
└── examples/
    └── stripe-api-example.md

Total: 13 files
Pattern: By Phase (Pattern 2)
```

---

### Example 3: Complex Skill (16-25 files)

**Use case:** Multi-audience product messaging (our current skill!)

**Current structure:**
```
multi-audience-product-messaging/
├── SKILL.md
├── references/
│   ├── core/        (8 files)
│   └── advanced/    (3 files)
└── assets/          (to be added)

Total: 12 files
Pattern: Core + Advanced
```

**Potential reorganization (if we expand to 20+ files):**

```
multi-audience-product-messaging/
├── SKILL.md
├── glossary/
│   ├── acronyms.md                 # MEDDIC, JTBD, ICP, TAM/SAM/SOM
│   └── frameworks.md                # Pain-Claim-Gain, April Dunford
├── references/
│   ├── core/
│   │   ├── phase-1-positioning/
│   │   │   ├── 01-dunford-framework.md
│   │   │   └── 02-positioning-workshop.md
│   │   ├── phase-2-messaging/
│   │   │   ├── 03-pain-claim-gain.md
│   │   │   ├── 04-multi-audience.md
│   │   │   └── 05-message-architecture.md
│   │   └── phase-3-rollout/
│   │       ├── 06-internal-rollout.md
│   │       ├── 07-getting-buy-in.md
│   │       ├── 08-testing.md
│   │       └── 09-launch.md
│   └── advanced/
│       ├── competitive/
│       │   ├── positioning-strategies.md
│       │   └── trap-setting.md
│       ├── sales/
│       │   ├── meddic-mapping.md
│       │   └── enablement.md
│       └── specialized/
│           ├── storytelling.md
│           ├── pricing-messaging.md
│           └── crisis-messaging.md
├── workflows/
│   ├── full-positioning-to-launch.md
│   └── quick-messaging-refresh.md
├── assets/
│   ├── templates/
│   │   ├── messaging-canvas.md
│   │   ├── persona-matrix.md
│   │   └── timeline.md
│   └── checklists/
│       ├── workshop-prep.md
│       └── launch-checklist.md
└── examples/
    ├── case-study-appcues.md
    ├── case-study-cognism.md
    └── before-after-examples.md

Total: 28 files (might split into 2 skills)
Pattern: Hybrid (Pattern 7)
```

**Alternative: Split into 2 skills:**
1. **positioning-and-messaging** (positioning + message creation)
2. **message-rollout-and-launch** (internal rollout + testing + launch)

---

## Summary

**Key Takeaways:**

1. **SKILL.md:** Keep under 500 lines, use as navigation hub
2. **Files per folder:** 5-10 ideal, 15 max before reorganizing
3. **Folder depth:** 2-3 levels maximum
4. **Total files:** Under 25 per skill
5. **Organization:** Pick one pattern and stick with it
6. **Navigation:** Always include decision trees in SKILL.md
7. **Glossary:** Add if 10+ specialized terms
8. **Examples:** Separate if 3+ case studies
9. **Workflows:** Add if combining multiple techniques

**When in doubt:**
- Start with **Core + Advanced** (Pattern 1)
- Add folders only when needed
- Reorganize when folders exceed 15 files
- Split skill when total exceeds 25 files

---

**Questions or improvements to this guide?** Open an issue or submit a PR.
