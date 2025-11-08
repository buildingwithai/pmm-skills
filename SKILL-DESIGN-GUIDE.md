# Skill Design Guide

**Audience:** Anyone creating skills for this library

This guide provides architectural patterns, organizational best practices, and file limits based on Claude's official documentation and our experience building comprehensive PMM skills.

## Table of Contents

- [Folder Structure Reference](#folder-structure-reference)
- [Token Costs & Limits](#token-costs--limits)
- [File & Folder Limits](#file--folder-limits)
- [Organizational Patterns](#organizational-patterns)
- [When to Use Which Structure](#when-to-use-which-structure)
- [Structure Comparison: Core/Advanced vs Phase-Based](#structure-comparison-coreadvanced-vs-phase-based)
- [Decision Framework](#decision-framework)
- [Common Pitfalls](#common-pitfalls)

---

## Folder Structure Reference

Quick reference for what goes in each folder and when to use it.

### Required Folders

#### `SKILL.md` (file, not folder)
**Purpose:** Navigation hub and skill entry point

**What goes here:**
- YAML frontmatter (`name`, `description`)
- Overview of the skill
- When to use this skill
- Decision trees ("if you need X → read Y")
- Navigation guide to reference files
- Quick reference cards

**Size limit:** <500 lines (target 400-450)

**What NOT to put here:**
- Detailed instructions (those go in `references/`)
- Long explanations or tutorials
- Examples or case studies
- Complete frameworks

**Why:**
- SKILL.md loads when skill is triggered (Level 2)
- Should be fast to scan
- User needs to quickly understand and navigate

---

#### `references/` (required)
**Purpose:** Detailed instructions, guides, and workflows

**What goes here:**
- Step-by-step process guides
- Framework explanations
- Methodology deep dives
- Workflow orchestration
- Best practices

**Organization within:** Use one of the patterns below
- `core/` + `advanced/` (default)
- `phase-1/`, `phase-2/`, `phase-3/` (for phased processes)
- `for-[audience]/` (for multi-audience skills)
- See [Organizational Patterns](#organizational-patterns) for full list

**File naming:**
- Core/sequential: `01-name.md`, `02-name.md`, `03-name.md`
- Advanced/named: `descriptive-name.md`

**Size guidelines:**
- Individual files: 200-600 lines
- Files per subfolder: 5-15 files
- Total in references/: Most of your skill content

**What NOT to put here:**
- Templates (those go in `assets/`)
- Glossary definitions (those go in `glossary/`)
- Case studies (those go in `examples/`)

**Why:**
- Progressive loading (Claude reads via bash as needed)
- Can contain extensive content without context penalty
- Organizes related content together

---

#### `assets/` (required)
**Purpose:** Ready-to-use templates, checklists, and tools

**What goes here:**
- Templates (messaging canvas, personas, etc.)
- Checklists (launch checklist, workshop prep)
- Scripts (Python, bash for automation)
- Blank forms or worksheets

**Organization within:**
- **Flat** (5 or fewer assets): `assets/template-name.md`
- **Organized** (6+ assets):
  ```
  assets/
  ├── templates/
  ├── checklists/
  └── scripts/
  ```

**File naming:**
- Descriptive: `messaging-canvas-template.md`
- Include type: `launch-checklist.md`, `workshop-prep-checklist.md`

**Size guidelines:**
- Templates can be any size (users copy and fill in)
- Each template should be standalone

**What NOT to put here:**
- Instructions on HOW to use templates (put in `references/`)
- Explanations or tutorials
- Completed examples (those go in `examples/`)

**Why:**
- Clear separation: guides vs tools
- Easy to find templates quickly
- Templates don't bloat instruction files

---

### Optional Folders (Add When Needed)

#### `glossary/` (optional)
**Purpose:** Definitions, acronyms, and terminology reference

**What goes here:**
- Acronym definitions (MEDDIC, JTBD, ICP, TAM/SAM/SOM)
- Framework quick references
- Industry terminology
- Concept definitions

**Organization within:**
```
glossary/
├── acronyms.md        # All acronyms in one file
└── frameworks.md      # Framework summaries
```

**When to add:**
- Skill uses **10+ specialized terms or acronyms**
- Same terms are referenced across multiple files
- Users frequently need terminology lookup

**File format:**
```markdown
**ICP** - Ideal Customer Profile
- Definition: The specific type of company that gets most value
- Example: "Mid-market B2B SaaS with 50-200 employees"
- Used in: references/core/01-positioning.md
```

**What NOT to put here:**
- Detailed framework explanations (put in `references/`)
- How to apply frameworks (put in `references/`)

**Why:**
- Prevents repeating definitions across files
- Quick reference for Claude and users
- Single source of truth

**Example from our messaging skill:**
- `glossary/acronyms.md` - MEDDIC, P1/P2/P3, ICP, TAM/SAM/SOM, HiPPO
- `glossary/pmm-frameworks.md` - April Dunford, Pain-Claim-Gain, JTBD

---

#### `examples/` (optional)
**Purpose:** Case studies, real-world applications, before/after examples

**What goes here:**
- Case studies with metrics ("Appcues improved 73%")
- Before/after comparisons
- Real company examples
- Workshop transcripts (anonymized)
- Sample outputs

**Organization within:**
```
examples/
├── case-study-[company].md
├── before-after-messaging.md
└── workshop-transcript.md
```

**When to add:**
- You have **3+ case studies or lengthy examples**
- Examples are 200+ lines each
- Want to separate "show" from "tell"

**File format:**
```markdown
# Example: [Company Name]

## Context
- Company: [name]
- Challenge: [what they faced]
- Timeline: [how long]

## What They Did
[Specific actions]

## Results
- Metric 1: [X% improvement]
- Metric 2: [specific outcome]

## Key Takeaways
[Lessons learned]
```

**What NOT to put here:**
- Instructions or how-tos (put in `references/`)
- Templates (put in `assets/`)

**Why:**
- Keeps instruction files focused on "how"
- Examples can be long without bloating guides
- Easy to add new examples over time

---

#### `workflows/` (optional)
**Purpose:** End-to-end process guides that combine multiple techniques

**What goes here:**
- Complete process orchestration
- How to combine multiple reference files
- Timeline showing which techniques to use when
- "Playbooks" for full execution

**Organization within:**
```
workflows/
├── full-[skill-name]-process.md
├── quick-[abbreviated]-workflow.md
└── [specific-scenario]-workflow.md
```

**When to add:**
- Skill teaches **individual techniques** in references/
- Users need guidance on **combining techniques**
- Multiple valid "paths" through the skill exist

**Difference from references/:**
- **references/**: Individual techniques (positioning, messaging, testing)
- **workflows/**: How to combine them ("Week 1: positioning, Week 2: messaging, Week 3: testing")

**File format:**
```markdown
# Workflow: Full Positioning to Launch

## Timeline: 9-12 weeks

### Phase 1: Positioning (Week 1)
→ Use: references/core/01-positioning.md
→ Output: Completed positioning

### Phase 2: Messaging (Week 2-3)
→ Use: references/core/02-messaging.md
→ Output: Message architecture

### Phase 3: Testing (Week 4)
→ Use: references/core/07-testing.md
→ Output: Validated messages
```

**What NOT to put here:**
- Detailed technique explanations (put in `references/`)
- Templates (put in `assets/`)

**Why:**
- references/ stay focused on single techniques
- Workflows show real combination
- Users can follow end-to-end OR pick à la carte

**Example use in messaging skill:**
- `workflows/full-positioning-to-launch.md` - Complete 12-week process
- `workflows/quick-messaging-refresh.md` - Fast 2-week update
- `workflows/competitive-repositioning.md` - Responding to competitor

---

#### `playbooks/` (optional)
**Purpose:** Pre-built guides for specific recurring scenarios

**What goes here:**
- Scenario-specific guides with context
- Pre-tested approaches for common situations
- Customized combinations of techniques for specific goals

**Organization within:**
```
playbooks/
├── [scenario-1].md
├── [scenario-2].md
└── [scenario-3].md
```

**When to add:**
- Users have **specific, recurring scenarios**
- Scenarios require **customized combination** of techniques
- You can provide **pre-tested playbooks**

**Difference from workflows/:**
- **Workflows:** Generic process (works for any situation)
- **Playbooks:** Specific scenario with context and tactics

**Example:**
```
Workflow: Full Positioning to Launch
[Generic: works for any product in any market]

Playbook: New Product Launch in Crowded Market
[Specific: new product, high competition, need differentiation]
- Includes specialized positioning for crowded markets
- Messaging focused on differentiation
- Launch tactics for breaking through noise
```

**File format:**
```markdown
# Playbook: [Scenario Name]

## When to Use This Playbook
- Situation: [specific context]
- Signs you need this: [indicators]

## Context
[What makes this scenario unique]

## Approach
### Step 1: [Phase]
→ Use: [which references]
→ Customize: [specific to this scenario]

## Tactics Specific to This Scenario
[What's different from generic workflow]

## Expected Outcomes
[What success looks like]

## Timeline
[Realistic timeline for this scenario]
```

**What NOT to put here:**
- Generic processes (put in `workflows/`)
- Detailed techniques (put in `references/`)

**Why:**
- Faster than building from scratch
- Pre-tested for specific contexts
- Shows best practices for common scenarios

**Example use in messaging skill:**
- `playbooks/new-product-launch.md` - New product, cold market
- `playbooks/repositioning-existing.md` - Established product, need refresh
- `playbooks/crisis-response.md` - Negative event, need fast response
- `playbooks/competitive-threat.md` - New competitor entered market

---

### Folder Summary Table

| Folder | Required? | Purpose | When to Use | Max Files |
|--------|-----------|---------|-------------|-----------|
| `SKILL.md` | ✅ Yes | Navigation hub | Always | 1 file, <500 lines |
| `references/` | ✅ Yes | Detailed guides | Always | Most content, 5-15 per subfolder |
| `assets/` | ✅ Yes | Templates & tools | Always | Unlimited (organize at 6+) |
| `glossary/` | ⚠️ Optional | Definitions | 10+ acronyms/terms | 2-3 files |
| `examples/` | ⚠️ Optional | Case studies | 3+ examples | Unlimited |
| `workflows/` | ⚠️ Optional | Process combos | Multiple paths | 3-5 workflows |
| `playbooks/` | ⚠️ Optional | Scenario guides | Recurring scenarios | 5-10 playbooks |

---

### Decision: Which Folders to Include?

**Minimum viable skill:**
```
skill-name/
├── SKILL.md
├── references/
│   └── core/
└── assets/
```

**Simple skill (3-8 files):**
```
skill-name/
├── SKILL.md
├── references/
│   ├── core/
│   └── advanced/
└── assets/
```

**Moderate skill (9-15 files):**
```
skill-name/
├── SKILL.md
├── glossary/          # If 10+ terms
├── references/
│   ├── core/
│   └── advanced/
├── assets/
└── examples/          # If 3+ case studies
```

**Complex skill (16-25 files):**
```
skill-name/
├── SKILL.md
├── glossary/
├── references/
│   ├── phase-1/
│   ├── phase-2/
│   ├── phase-3/
│   └── advanced/
├── workflows/         # Show how to combine
├── assets/
│   ├── templates/
│   └── checklists/
└── examples/
```

**Rule of thumb:**
- Start minimal (SKILL.md + references/ + assets/)
- Add folders only when you hit the threshold
- Don't over-organize simple skills

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

## Structure Comparison: Core/Advanced vs Phase-Based

The two most common structures for PMM skills are **Core/Advanced** and **Phase-Based**. Here's how to choose between them.

### Pattern 1: Core + Advanced (Default)

**Structure:**
```
skill-name/
├── SKILL.md
├── references/
│   ├── core/              # Sequential workflow (01-, 02-, 03-)
│   │   ├── 01-step-one.md
│   │   ├── 02-step-two.md
│   │   └── 03-step-three.md
│   └── advanced/          # Named files (situational)
│       ├── edge-case.md
│       └── power-tip.md
└── assets/
```

**Best for:**
- ✅ Linear, sequential workflows
- ✅ Simple to moderate complexity (3-15 files)
- ✅ Clear "main path" that most users follow
- ✅ Advanced features are truly optional

**Characteristics:**
- **core/**: Numbered files (01-, 02-) showing sequence
- **advanced/**: Named files loaded as needed
- Most users go through core/ in order
- Advanced/ only when specific need arises

**SKILL.md decision trees:**
```markdown
**Main workflow (most users):**
→ Read: core/01-positioning.md → 02-messaging.md → 03-rollout.md

**Specific advanced needs:**
→ Crisis messaging: advanced/crisis-messaging.md
→ Pricing messaging: advanced/pricing-messaging.md
```

**Example: Our Current Messaging Skill**
```
multi-audience-product-messaging/
├── SKILL.md
├── glossary/
├── references/
│   ├── core/        # 8 files (positioning → messaging → rollout → testing)
│   └── advanced/    # 3 files (storytelling, pricing, decay analysis)
└── assets/

Total: 12 files
Works well - clear main path, optional extras
```

---

### Pattern 2: By Phase/Stage

**Structure:**
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
└── assets/
```

**Best for:**
- ✅ Clear phase boundaries (discovery → strategy → execution)
- ✅ Moderate to complex (12-25 files)
- ✅ Each phase has multiple steps
- ✅ Users might start at different phases

**Characteristics:**
- **Phases**: Organized by timeline or project stage
- **Multiple files per phase**: Each phase is its own mini-workflow
- Users can jump to their current phase
- Natural grouping of related content

**SKILL.md decision trees:**
```markdown
**Full process (start to finish):**
→ Phase 1: phase-1-discovery/ (all files)
→ Phase 2: phase-2-strategy/ (all files)
→ Phase 3: phase-3-execution/ (all files)

**Jump to specific phase:**
→ Already did discovery: phase-2-strategy/planning.md
→ Need execution only: phase-3-execution/implementation.md
```

**Example: Messaging Skill Reorganized for Phases**
```
multi-audience-product-messaging/
├── SKILL.md
├── glossary/
├── references/
│   ├── phase-1-positioning/      # Week 1
│   │   ├── 01-dunford-framework.md
│   │   └── 02-positioning-workshop.md
│   ├── phase-2-messaging/        # Week 2-3
│   │   ├── 03-pain-claim-gain.md
│   │   ├── 04-multi-audience.md
│   │   └── 05-message-architecture.md
│   ├── phase-3-rollout/          # Week 4-7
│   │   ├── 06-internal-rollout.md
│   │   ├── 07-buy-in.md
│   │   ├── 08-testing.md
│   │   └── 09-launch.md
│   └── advanced/
│       ├── competitive/
│       └── specialized/
└── assets/

Total: Same 12 files, organized differently
Better for: Skills growing to 16-20+ files
```

---

### When to Use Core/Advanced

**Choose Core/Advanced when:**

1. **Linear workflow** - There's a clear A → B → C path
   - Example: "First positioning, then messaging, then rollout"

2. **Simple to moderate** - 3-15 files total
   - Core/advanced is simpler to navigate at this size

3. **Most users follow same path** - 80%+ go through core in order
   - Advanced features are situational

4. **Natural core vs optional split** - Clear what's "main" vs "extra"
   - Example: Crisis messaging is clearly optional/advanced

5. **Quick to understand** - Users can scan and know where to go
   - "Core = main workflow, advanced = extras"

**Real examples:**
- Document processing (core: read, write, format; advanced: OCR, batch)
- Code review (core: review process; advanced: security audits, performance)
- Commit messages (core: conventional commits; advanced: monorepo, squashing)

**Signs you're outgrowing core/advanced:**
- core/ folder has 10+ files and feels crowded
- Files in core/ cluster into natural groups
- Users commonly only need "part" of core/

**When to switch:** If you hit 15-18 files, consider reorganizing by phase

---

### When to Use Phase-Based

**Choose Phase-Based when:**

1. **Clear phase boundaries** - Natural stages in the process
   - Example: "Discovery → Strategy → Execution → Measurement"

2. **Moderate to complex** - 12-25 files total
   - Phases help organize larger skills

3. **Multiple steps per phase** - Each phase has 3-5+ files
   - Phases group related content

4. **Users might skip phases** - Some start mid-process
   - Example: "I already have positioning, just need rollout strategy"

5. **Timeline-based** - Skill follows a time sequence
   - Example: "Week 1: positioning, Week 2-3: messaging"

**Real examples:**
- Product launch (plan → build → test → launch → measure)
- GTM strategy (research → positioning → launch → scale)
- Customer research (plan → recruit → conduct → analyze → report)

**Signs you need phase-based:**
- You find yourself saying "Phase 1" and "Phase 2"
- Files naturally cluster by project stage
- Each cluster has 3-5+ related files
- Users ask "Which phase should I start at?"

**When to use:** If skill has 12+ files and clear stages

---

### Decision Matrix

| Factor | Core/Advanced | Phase-Based |
|--------|---------------|-------------|
| **Total files** | 3-15 | 12-25 |
| **Workflow** | Linear (A→B→C) | Staged (Phase 1→2→3) |
| **File distribution** | Most in core/ | Balanced across phases |
| **User entry point** | 80% start at beginning | Users might skip phases |
| **Clustering** | Core vs optional | By project stage |
| **Timeline** | One continuous flow | Distinct time periods |
| **Flexibility** | Follow sequence | Jump to relevant phase |

---

### Migrating from Core/Advanced to Phase-Based

**When to reorganize:**
- Skill grows from 12 to 18+ files
- You're adding another "section" to core/
- Files naturally cluster by stage
- Users are confused about where to start

**How to migrate:**

**Step 1: Identify phases**
- Look at your numbered files (01, 02, 03...)
- Find natural breaks/clusters
- Name the phases based on project stage

**Example:**
```
Before:
core/01-positioning.md
core/02-positioning-workshop.md
core/03-messaging.md
core/04-multi-audience.md
core/05-message-arch.md
core/06-rollout.md
core/07-buy-in.md
core/08-testing.md
core/09-launch.md

After:
phase-1-positioning/01-framework.md
phase-1-positioning/02-workshop.md
phase-2-messaging/03-messaging.md
phase-2-messaging/04-multi-audience.md
phase-2-messaging/05-architecture.md
phase-3-rollout/06-internal.md
phase-3-rollout/07-buy-in.md
phase-3-rollout/08-testing.md
phase-3-rollout/09-launch.md
```

**Step 2: Update SKILL.md**
- Change decision trees from "core files" to "phases"
- Add phase-based navigation

**Step 3: Test navigation**
- Can users find what they need?
- Are phases clear and logical?
- Do decision trees still work?

---

### Case Study: Our Messaging Skill

**Current state (Core/Advanced):**
```
references/
├── core/              # 8 files
│   ├── 01-positioning-foundation.md
│   ├── 02-pain-claim-gain-messaging.md
│   ├── 03-multi-audience-messaging.md
│   ├── 04-message-architecture.md
│   ├── 05-internal-rollout-guide.md
│   ├── 07-testing-iteration-EXPANDED.md
│   ├── 10-workshop-facilitation-master-guide.md
│   └── 11-sales-stage-competitive-strategy.md
└── advanced/          # 3 files
    ├── storytelling-frameworks.md
    ├── pricing-messaging.md
    └── message-decay-analysis.md

Total: 12 files
Status: ✅ Works well with current structure
```

**Assessment:**
- ✅ Linear flow exists (positioning → messaging → rollout)
- ✅ Only 12 files (not crowded yet)
- ✅ Clear core vs advanced distinction
- ✅ Most users follow sequence

**Decision: Keep Core/Advanced for now**

**When to reconsider:**
- If we add 6+ more files (reaching 18+)
- If we add another "section" (e.g., measurement/analytics with 5 files)
- If users start asking "Where do I start if I already have messaging?"

**Potential future reorganization (if we expand):**
```
references/
├── phase-1-positioning/
│   ├── 01-dunford-framework.md
│   └── 02-positioning-workshop.md
├── phase-2-messaging/
│   ├── 03-pain-claim-gain.md
│   ├── 04-multi-audience.md
│   ├── 05-message-architecture.md
│   ├── 10-workshop-facilitation.md      # Move here (it's about messaging workshop)
│   └── 11-sales-stage-messaging.md
├── phase-3-rollout-and-launch/
│   ├── 06-internal-rollout.md
│   ├── 07-testing-iteration.md
│   └── 08-launch-strategy.md             # Would add
└── advanced/
    ├── competitive/
    │   └── positioning-trap-setting.md    # Would add
    ├── specialized/
    │   ├── storytelling-frameworks.md
    │   ├── pricing-messaging.md
    │   └── crisis-messaging.md            # Would add
    └── optimization/
        └── message-decay-analysis.md

Total: 15+ files
Would reorganize at this point
```

---

### Summary: How to Choose

**Decision flowchart:**

```
START: How many total files in references/?

├─ 3-11 files
│  └─ Use CORE + ADVANCED (Pattern 1)
│     Simple, clear, easy to navigate
│
├─ 12-15 files
│  └─ Does workflow have clear phases?
│      ├─ Yes → Consider PHASE-BASED (Pattern 2)
│      └─ No → Use CORE + ADVANCED (Pattern 1)
│
└─ 16-25 files
   └─ Use PHASE-BASED (Pattern 2)
      Helps manage complexity

26+ files → Consider splitting into multiple skills
```

**Quick checklist:**

- [ ] **3-11 files?** → Core/Advanced
- [ ] **12-15 files + no clear phases?** → Core/Advanced
- [ ] **12-15 files + clear phases?** → Consider Phase-Based
- [ ] **16+ files?** → Phase-Based
- [ ] **Files cluster naturally by stage?** → Phase-Based
- [ ] **Users skip sections?** → Phase-Based
- [ ] **Linear workflow?** → Core/Advanced
- [ ] **Most users follow same path?** → Core/Advanced

---

### Both Approaches Use Same Principles

**Regardless of structure:**

1. **Progressive disclosure** - Claude loads files as needed via bash
2. **Decision trees in SKILL.md** - Guide Claude to right files
3. **Numbered for sequence** - Use numbers when order matters
4. **Named when situational** - Descriptive names for optional content
5. **Group related content** - Keep similar files together
6. **Limit folder depth** - Max 3 levels deep
7. **Limit files per folder** - 5-15 files max per folder

The structure is about **organization for humans** - Claude navigates via SKILL.md decision trees either way.

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
