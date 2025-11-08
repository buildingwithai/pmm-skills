# Skill Library

A curated library of Claude Skills with extensive research and resources. Currently focused on Product Marketing Management (PMM), expandable to other domains.

## What This Repository Is

This repository is a **public library of downloadable Claude Skills**:

1. **Skill Library** (`pmm-skills/`) - Download and import individual skills into Claude
2. **Research Workspace** (`resources/`) - Behind-the-scenes research that informs skill creation
3. **Self-Sustaining** - Documentation for AI to maintain and update skills over time

## What Are Claude Skills?

**Claude Skills** are folders containing instructions, reference materials, and templates that Claude can load when needed. Think of them as specialized "expert modes" that give Claude deep knowledge in specific domains.

### How to Use a Skill

1. **Download** - Grab the skill folder from `pmm-skills/[skill-name]/`
2. **Zip it** - Compress the folder into a .zip file
3. **Upload to Claude** - Go to Claude.ai Settings → Upload skill
4. **Use it** - Claude automatically loads the skill when relevant to your conversation

### Key Characteristics

- **Progressive Disclosure**: Claude only loads what it needs, when it needs it
- **Self-Contained**: Each skill includes everything needed (guides, templates, examples)
- **Reusable**: Use the same skill across different projects and conversations
- **Portable**: Skills work in Claude.ai, Claude Code, and via API

## How Claude Skills Work (Architecture)

Understanding how skills work helps you use them effectively and create new ones.

### Progressive Disclosure

Claude doesn't load the entire skill at once. Instead:

1. **First**: Claude reads `SKILL.md` (the navigation hub)
2. **Then**: Based on your request, Claude loads only relevant reference files
3. **Result**: Efficient context usage, no information overload

**Example:**

```
You: "Help me create positioning for my B2B product"

Claude's process:
1. Reads SKILL.md → sees decision tree
2. Decision tree says: "Creating positioning → load core/01-positioning-foundation.md"
3. Loads only that file
4. Works with you using that focused content

You never see the competitive positioning, crisis messaging, or other
advanced topics unless you specifically need them.
```

### Core vs Advanced Structure

Skills are organized into two levels:

#### **`references/core/`** - Sequential Workflow

- Main process most users go through
- **Numbered files** for sequence (01-, 02-, 03-...)
- Loaded in order for the primary use case
- Example: `01-positioning → 02-messaging → 03-rollout`

**When Claude loads core:**
- User asks to create/build/develop something
- Following the primary workflow
- Needs step-by-step process

#### **`references/advanced/`** - Situational Power-Ups

- Specific scenarios or edge cases
- **Named files** (not numbered) - load as needed
- Only relevant for specialized situations
- Example: `crisis-messaging.md`, `category-creation.md`

**When Claude loads advanced:**
- User mentions a specific scenario ("dealing with a crisis")
- Asks for deep dive on a specialized topic
- Needs techniques beyond the core process

### Anatomy of a Claude Skill

```
skill-name/
├── SKILL.md                    # Navigation hub with YAML frontmatter (<500 lines)
│                               # Contains decision trees, "when to use what"
│
├── references/
│   ├── core/                   # Main workflow (sequential)
│   │   ├── 01-framework.md     # Step 1 of process
│   │   ├── 02-process.md       # Step 2 of process
│   │   └── 03-execution.md     # Step 3 of process
│   │
│   └── advanced/               # Power-ups (load as needed)
│       ├── specific-scenario.md   # Only when user needs this
│       └── deep-dive-topic.md     # Only when user needs this
│
├── assets/                     # Templates, checklists, tools
│   ├── template.md             # Ready-to-use templates
│   ├── checklist.md            # Step-by-step checklists
│   └── framework.md            # Frameworks and canvases
│
└── examples/                   # Real examples, case studies
    ├── before-after.md         # Transformation examples
    └── case-study.md           # Real company examples with metrics
```

### Decision Trees in SKILL.md

SKILL.md acts as a "navigation hub" that tells Claude what to load:

```markdown
## Quick Decision Trees

**Creating [thing] from scratch:**
→ Read: core/01-framework → core/02-process → core/03-execution
→ Use: template.md, checklist.md

**Handling [specific scenario]:**
→ Read: advanced/specific-scenario.md
→ Use: scenario-template.md

**[Specific challenge]:**
→ Read: advanced/deep-dive.md
→ Also see: core/02-process.md (section on X)
```

This allows Claude to:
- Quickly find relevant content
- Load only what's needed
- Provide accurate, focused guidance

### Why This Structure Works

1. **Efficiency**: Load 5-10KB instead of 100KB of content
2. **Focus**: User gets relevant info, not everything
3. **Scalability**: Can add advanced topics without bloating core
4. **Flexibility**: Same skill works for beginners and experts

## Repository Structure

```
skill-library/                              # Repository root (GitHub: pmm-skills)
├── README.md                               # This file (library catalog)
├── CONTRIBUTING.md                         # How to create/add skills
├── MAINTENANCE.md                          # How AI maintains/updates skills
├── LICENSE
│
├── pmm-skills/                            # PMM skill library (downloadable)
│   ├── multi-audience-product-messaging/
│   │   ├── SKILL.md
│   │   ├── references/
│   │   │   ├── core/                      # Main workflow
│   │   │   └── advanced/                  # Power-ups
│   │   ├── assets/                        # Templates for this skill
│   │   └── examples/                      # Case studies
│   │
│   ├── competitive-intelligence/          # Future skill
│   ├── go-to-market-strategy/            # Future skill
│   └── pricing-packaging/                # Future skill
│
└── resources/                             # Research workspace (NOT in skill downloads)
    └── pmm/                               # PMM research
        ├── research/                      # Industry research by topic
        │   ├── messaging/
        │   ├── positioning/
        │   ├── gtm/
        │   └── [topic]/
        ├── frameworks/                    # Standalone PMM frameworks
        ├── courses/                       # Course notes and transcripts
        └── templates/                     # Generic cross-skill templates
```

### What Goes Where

**`pmm-skills/[skill-name]/`** = **Downloadable skills (public library)**
- Complete, self-contained skill
- Everything needed for that workflow
- Ready to zip and import into Claude
- User-facing

**`resources/pmm/`** = **Research workspace (behind the scenes)**
- Research done while building skills
- Frameworks and methodologies documented
- Course materials and learnings
- Helps AI build better skills
- Not included in skill downloads

## Available Skills

### 1. Multi-Audience Product Messaging
**Status**: ✅ Complete and Expanded

Create positioning and messaging that resonates with both technical and non-technical audiences, roll it out internally, and launch it successfully.

**Use this skill when you need to:**
- Create positioning and messaging for B2B SaaS products
- Communicate value to multiple stakeholders (technical buyers, economic buyers, users, champions)
- Roll out messaging internally and get cross-functional buy-in
- Run effective positioning workshops
- Test and iterate on messaging
- Adapt messaging by sales stage using MEDDIC
- Position strategically against competitors

**Location**: `/pmm-skills/multi-audience-product-messaging/`

**Download**: Download the folder and zip it for upload to Claude

**Key Components**:
- April Dunford's positioning framework
- Pain-Claim-Gain messaging methodology
- Multi-stakeholder communication strategies
- Workshop facilitation techniques (handling HiPPOs, conflict resolution)
- Message testing frameworks (Wynter, UserTesting)
- Sales stage-specific messaging (MEDDIC mapping)
- Competitive trap-setting tactics
- 12 comprehensive guides + templates

**Timeline**: 9-12 weeks for full positioning-to-launch process

**Architecture**:
- **Core references (8)**: Positioning → Messaging → Rollout → Testing → Launch
- **Advanced references (3)**: Storytelling, pricing, message decay analysis
- **Assets**: Templates, canvases, checklists
- **Version**: 1.0 (Last updated: 2024-11)

[See the skill's README →](./pmm-skills/multi-audience-product-messaging/SKILL.md)

---

### Future Skills (Planned)

**2. Competitive Intelligence & Market Analysis**
- Competitive research frameworks
- Win/loss analysis
- Market sizing and segmentation
- Battle card creation

**3. Go-to-Market Strategy**
- GTM planning and execution
- Launch orchestration
- Channel strategy
- Sales and CS enablement

**4. Pricing & Packaging**
- Pricing strategy frameworks
- Value-based pricing
- Packaging optimization
- Pricing research and testing

**5. Product Launch & Adoption**
- Launch planning and checklists
- Beta programs
- Customer adoption strategies
- Launch analytics

**6. Customer Research & Insights**
- User interview frameworks
- Jobs-to-be-done research
- Win/loss interviews
- Voice of customer programs

**7. Content Strategy for PMM**
- Case study development
- White papers and reports
- Demo scripts and narratives
- Product marketing content calendar

## How to Use This Repository

### For PMM Practitioners

1. **Browse available skills** in `pmm-skills/`
2. **Download the skill folder** you need
3. **Zip the folder**
4. **Upload to Claude.ai** (Settings → Skills)
5. **Start a conversation** - Claude will use the skill automatically

**Example:**
```
1. Download: pmm-skills/multi-audience-product-messaging/
2. Zip it: multi-audience-product-messaging.zip
3. Upload to Claude.ai
4. Chat: "Help me create positioning for our new developer platform"
5. Claude automatically loads the skill and guides you through the process
```

### For Skill Creators

1. **See what research exists** in `resources/pmm/`
2. **Follow CONTRIBUTING.md** to create a new skill
3. **Build with progressive disclosure** (core vs advanced)
4. **Add to `pmm-skills/`** with complete documentation
5. **Update this README** with your skill

### For AI Assistants (Future Sessions)

1. **Read MAINTENANCE.md** for upkeep protocols
2. **Check research freshness** before using skills
3. **Proactively suggest updates** when research is stale
4. **Document new research** in `resources/` while building skills

## Skill Design Principles

Skills in this library follow these principles:

### 1. Progressive Disclosure
- **SKILL.md**: Navigation hub (<500 lines)
- **Core references**: Main workflow (sequential, numbered)
- **Advanced references**: Power-ups (named, load as needed)
- **Decision trees**: Tell Claude what to load when

### 2. Self-Contained
- Everything needed is in the skill folder
- No dependencies on external files
- Ready to download and use immediately

### 3. Research-Backed
- Built from 10-15+ authoritative sources
- Industry best practices and timelines
- Real examples with metrics
- Current frameworks and methodologies

### 4. Template-Rich
- Ready-to-use templates and checklists
- Canvases and frameworks
- Interview scripts and guides
- Workshop agendas

### 5. Real Examples
- Before/after transformations
- Case studies with specific metrics
- Company examples (named or anonymized)
- Real results from real implementations

### 6. Timeline-Aware
- Industry-standard timelines for each phase
- Realistic duration estimates
- What can be compressed vs what can't
- Typical vs fast-track vs comprehensive timelines

### 7. Use-Case Driven
- Clear "When to Use This Skill" section
- Decision trees for different scenarios
- Multiple entry points for different needs
- Anti-patterns (when NOT to use)

## Contributing

Want to add a skill or update existing ones?

**See [CONTRIBUTING.md](./CONTRIBUTING.md) for:**
- Step-by-step skill creation guide
- Content guidelines and quality standards
- Structure requirements
- Research protocols

**Quick process:**
1. Propose the skill (open an issue)
2. Research extensively (10-15+ sources)
3. Build the skill (follow structure in CONTRIBUTING.md)
4. Document research (add to `resources/`)
5. Submit (PR with skill + research)

## Maintenance

This library is designed to be **self-sustaining**.

**See [MAINTENANCE.md](./MAINTENANCE.md) for:**
- How AI should review and update skills
- When research needs refreshing
- How to identify outdated content
- Protocols for keeping skills current

**Future AI sessions:** Read MAINTENANCE.md before working with skills.

## Philosophy

This repository operates on these principles:

1. **Skills over prompts**: Reusable, structured knowledge beats one-off prompts
2. **Progressive disclosure**: Load what you need, when you need it (not everything upfront)
3. **Templates over theory**: Actionable assets beat abstract advice
4. **Research-backed**: Built from 10-15+ authoritative sources, not guesswork
5. **Real examples**: Show, don't just tell (with metrics and outcomes)
6. **Self-sustaining**: AI maintains and updates skills over time
7. **Public library**: Anyone can download and use these skills

## FAQ

**Q: How do I use a skill from this library?**
A: Download the skill folder from `pmm-skills/[skill-name]/`, zip it, and upload to Claude.ai Settings → Skills.

**Q: Do I need to download the whole repository?**
A: No, just download the specific skill folder you want to use.

**Q: What's in the `resources/` folder? Do I need it?**
A: Resources contain the research and frameworks that informed skill creation. You don't need them - they're for AI to reference when building/updating skills.

**Q: Can I customize a skill for my company?**
A: Yes! Download it, modify for your needs, and upload your custom version.

**Q: How do I know if a skill is up-to-date?**
A: Check the `version` and `last_updated` fields in the skill's SKILL.md YAML frontmatter.

**Q: Can I contribute a skill?**
A: Yes! See [CONTRIBUTING.md](./CONTRIBUTING.md) for the process.

**Q: Why separate core/ and advanced/ references?**
A: Progressive disclosure - Claude loads core for main workflows, advanced only when needed. Keeps context efficient.

**Q: Can I create skills for non-PMM topics?**
A: Yes! The structure works for any domain. Fork this repo and create skills for your field.

**Q: How does Claude know when to load core vs advanced?**
A: Decision trees in SKILL.md tell Claude what to load based on the user's request.

**Q: What makes a good skill?**
A: Research-backed (10-15+ sources), template-rich, real examples, clear timelines, progressive disclosure structure.

## Tech Stack & Tools

This repository uses:
- **Markdown** for all content (`.md` files)
- **YAML frontmatter** for skill metadata
- **Git** for version control
- **Claude AI** for skill consumption
- **No build process** - just files and folders

## Expanding Beyond PMM

This repository is structured to expand beyond PMM:

```
skill-library/
├── pmm-skills/              # Product Marketing skills
├── sales-skills/            # Future: Sales skills
├── engineering-skills/      # Future: Engineering skills
└── resources/
    ├── pmm/                 # PMM research
    ├── sales/               # Future: Sales research
    └── shared/              # Cross-domain resources
```

Interested in adding skills from other domains? See [CONTRIBUTING.md](./CONTRIBUTING.md).

## License

[MIT License](./LICENSE)

## Acknowledgments

**PMM Frameworks & Methodologies:**
- **April Dunford** - Positioning framework ([Obviously Awesome](https://www.aprildunford.com/))
- **Anthony Pierri** - Pain-Claim-Gain messaging methodology
- **MEDDIC/MEDDICC** - Sales qualification frameworks
- **Product Marketing Alliance** - PMM education and community
- **Lenny Rachitsky** - Product and growth insights

**Claude Skills:**
- **Anthropic** - Claude Skills architecture and platform

## Maintainer

This is a curated knowledge repository. Feel free to fork and adapt for your own skill library.

---

## Getting Started

### As a PMM Practitioner

1. **Explore** → Browse `pmm-skills/` to see available skills
2. **Download** → Grab the skill folder you need
3. **Import** → Zip and upload to Claude.ai Settings
4. **Use** → Start a conversation, Claude loads the skill automatically
5. **Customize** → Modify for your company/context as needed

### As a Skill Creator

1. **Research** → Check `resources/` for existing research
2. **Create** → Follow [CONTRIBUTING.md](./CONTRIBUTING.md) step-by-step
3. **Document** → Add research to `resources/` as you build
4. **Submit** → Add your skill to `pmm-skills/`
5. **Share** → Update this README with your skill

### As a Future AI Session

1. **Read** → [MAINTENANCE.md](./MAINTENANCE.md) for maintenance protocols
2. **Check** → Review research freshness before using skills
3. **Update** → Proactively refresh outdated content
4. **Document** → Add new research as you discover it
5. **Improve** → Suggest enhancements based on usage patterns

---

**Questions or ideas?** Open an issue or submit a pull request.

**Ready to use a skill?** Go to `pmm-skills/` and download what you need!
