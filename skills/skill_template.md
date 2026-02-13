# Skill Template

Use this template when creating new skills.

---

## Minimal Template

```markdown
---
name: skill-name
description: What this skill does. Use when: (1) trigger condition, (2) another trigger, (3) keywords that activate it. Be comprehensive here — this is what determines when the skill gets used.
---

# Skill Name

One-line description of what this does.

## Workflow

1. **Step 1** - What to do first
2. **Step 2** - Next action
3. **Step 3** - Final step

## How To Use

[Core instructions — keep concise, the AI is smart]

### Example

**Input:**
[Example user request]

**Output:**
[Example response]

## Output Format

```
[Template of expected output structure]
```

## Parameters (optional)

- **param1**: option1 | option2 | option3
- **param2**: default value
```

---

## Key Principles

| Do | Don't |
|----|-------|
| ✅ Put ALL triggers in `description` | ❌ "When to use" sections in body |
| ✅ Keep body under 500 lines | ❌ Verbose explanations |
| ✅ Show examples over explaining | ❌ README, CHANGELOG files |
| ✅ Use structured output templates | ❌ Assume AI needs hand-holding |
| ✅ One clear workflow | ❌ Multiple competing approaches |

---

## Folder Structure

```
skill-name/
├── SKILL.md              ← Required (main instructions)
├── scripts/              ← Optional: executable code
├── references/           ← Optional: docs loaded as needed
└── assets/               ← Optional: templates, images, files
```

---

## Description Writing Tips

The `description` field is **critical** — it's the only thing loaded to decide if the skill triggers.

**Good description:**
```yaml
description: Validate and verify postal addresses for accuracy. Use when: (1) user asks to "validate", "verify", or "check" an address, (2) user needs to standardize address format, (3) user says "address validation". Supports US, Canada, UK formats.
```

**Bad description:**
```yaml
description: Address validation tool.
```

---

## Progressive Disclosure

For complex skills, split content:

```markdown
## Quick Start
[Essential info here]

## Advanced
For detailed X, see [REFERENCE.md](references/REFERENCE.md)
```

This keeps SKILL.md lean while making details available when needed.

---

## Checklist Before Publishing

- [ ] Name is lowercase with hyphens (e.g., `my-skill`)
- [ ] Description includes all trigger words/phrases
- [ ] Body is under 500 lines
- [ ] At least one example provided
- [ ] Output format is clear
- [ ] No extra files (README, CHANGELOG, etc.)
