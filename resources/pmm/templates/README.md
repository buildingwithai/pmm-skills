# Generic Templates

Cross-skill templates used across multiple PMM workflows.

## What Goes Here

Only **generic, reusable templates** that apply to multiple skills:

✅ **Put here:**
- Generic persona templates (work for any skill)
- Market research templates (TAM/SAM/SOM)
- Generic launch planning templates

❌ **Don't put here:**
- Skill-specific templates → Put in `[skill]/assets/`
- Workflow-specific tools → Put in `[skill]/assets/`

## Structure

```
templates/
├── persona-templates/        # Buyer persona templates
├── market-research/         # Market sizing, competitive analysis
└── launch-plans/           # Generic launch planning
```

## Template Subdirectories

### `persona-templates/`
Generic buyer persona and ICP templates.

**Examples:**
- B2B buyer persona canvas
- User persona template
- ICP definition template
- Stakeholder mapping template

### `market-research/`
Market sizing and analysis templates.

**Examples:**
- TAM/SAM/SOM calculator
- Competitive matrix template
- Market segmentation canvas
- Win/loss interview script (generic)

### `launch-plans/`
Generic launch and planning templates.

**Examples:**
- Launch checklist template
- Launch timeline template
- Stakeholder communication plan
- Launch retrospective template

## Template Format

Each template should include:

```markdown
# Template Name

**Purpose:** [What this helps you accomplish]
**When to use:** [Scenarios]
**Time to complete:** [Estimate]

## Instructions

1. [How to use this template]
2. [What to fill in]
3. [Success criteria]

## Template

---

[The actual template with placeholders]

---

## Example

[Filled-in example]

## Tips

- [Tip 1]
- [Tip 2]
```
