---
name: agent-skill-authoring
description: Create, refactor, and validate portable Agent Skills for the TensorCheck project using concise trigger descriptions, progressive disclosure, focused workflows, references, scripts, and measurable definitions of done.
metadata:
  version: "1.0.0"
---

# Agent Skill Authoring

## Goal

Turn repeated procedures into small reusable skills rather than giant permanent prompts.

## Structure

```text
skill-name/
  SKILL.md
  references/   # optional
  scripts/      # optional
  assets/       # optional
```

## Frontmatter

Require:
- lowercase kebab-case name matching folder
- specific description that says what the skill does and when to use it

## Body

Prefer:
1. mission
2. inputs
3. workflow
4. guardrails
5. output format
6. definition of done

Move large reference material out of SKILL.md.

## Quality

A skill should:
- own one coherent workflow,
- avoid conflicting with neighboring skills,
- tell the agent when NOT to use it,
- favor verifiable outputs,
- avoid vague personas like "be world-class".

Test skills on realistic tasks before relying on them.
