# Shared Resources

This directory contains **cross-skill research and resources** that inform skill creation. This is the AI's workspace - **not included in downloadable skills**.

## Purpose

Resources serve as a "research lab notebook" that:

✅ **Documents how skills were built** - research sources, frameworks, decisions
✅ **Enables future updates** - AI can review and identify outdated content
✅ **Provides context** - even in new conversations, understand research trail
✅ **Speeds up related skills** - reuse research across similar skills
✅ **Shows reasoning** - why we structured things a certain way

## Structure

```
resources/
├── README.md           # This file
└── pmm/               # Product Marketing research
    ├── research/      # Industry research by topic
    ├── frameworks/    # Standalone PMM frameworks
    ├── courses/       # Course notes and transcripts
    └── templates/     # Generic cross-skill templates
```

**Future expansion:**
```
resources/
├── pmm/               # Product Marketing research
├── sales/             # Sales research (future)
├── engineering/       # Engineering research (future)
└── shared/            # Cross-domain resources (future)
```

## What Goes Here vs. In Skills

**Put it in `resources/pmm/` if:**
- It's research that informed a skill
- It's referenced by multiple skills
- It's a standalone framework or methodology
- It's course materials or learnings
- It helps AI understand how to build/update skills

**Put it in `pmm-skills/[skill-name]/` if:**
- It's specific to one skill's workflow
- It's a step-by-step guide for that skill
- It's a template for that specific workflow
- It goes in the downloadable skill

## Directory Details

### `/pmm/research/`
Industry research and analysis organized by topic.

**See**: [pmm/research/README.md](./pmm/research/README.md)

**Topics:**
- `messaging/` - Message testing, copywriting, frameworks
- `positioning/` - Positioning methodologies, category creation
- `gtm/` - Go-to-market strategy, launch planning
- `competitive-intelligence/` - Competitive analysis, win/loss
- `pricing/` - Pricing strategy and research
- `customer-research/` - User research, JTBD, interviews

### `/pmm/frameworks/`
Standalone frameworks referenced by multiple skills.

**See**: [pmm/frameworks/README.md](./pmm/frameworks/README.md)

**Examples:**
- April Dunford's positioning framework
- MEDDIC/MEDDICC sales methodology
- Jobs-to-be-done research framework
- Pain-Claim-Gain messaging method

### `/pmm/courses/`
Notes and transcripts from PMM courses.

**See**: [pmm/courses/README.md](./pmm/courses/README.md)

**Structure**: Each course gets its own directory with module notes and key takeaways.

### `/pmm/templates/`
Generic templates used across multiple skills.

**See**: [pmm/templates/README.md](./pmm/templates/README.md)

**Note:** Only cross-skill generic templates go here. Skill-specific templates go in `pmm-skills/[skill-name]/assets/`.

## For AI: How to Use Resources

### When Building a New Skill

1. **Check existing research** - `pmm/research/[topic]/`
2. **Review related frameworks** - `pmm/frameworks/`
3. **Conduct new research** - Add findings to `pmm/research/`
4. **Document decisions** - Why you chose certain frameworks, sources
5. **Build the skill** - Use research to create comprehensive skill
6. **Keep research separate** - Don't include research files in skill downloads

### When Updating an Existing Skill

1. **Review original research** - `pmm/research/[topic]/`
2. **Check dates** - Is research current?
3. **Re-research if needed** - Update with new findings
4. **Update skill** - Reflect new research in skill content
5. **Document changes** - Note what changed in research files

### When Starting a New Conversation

1. **Read MAINTENANCE.md** - Understand upkeep protocols
2. **Check research freshness** - Review dates on research files
3. **Proactively flag outdated content** - Suggest updates to user
4. **Review before using** - Don't assume research is current

## Maintenance

See [MAINTENANCE.md](../MAINTENANCE.md) for detailed protocols on:
- How to assess research freshness
- When to update content
- How to document new research
- Self-sustaining maintenance practices

## Contributing

See [CONTRIBUTING.md](../CONTRIBUTING.md) for:
- How to add research
- How to document frameworks
- How to organize course materials
- Content quality standards

---

**Remember:** Resources are the foundation that makes skills comprehensive and valuable. Document thoroughly!
