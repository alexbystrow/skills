# skills

This repository contains a collection of custom AI skills.
Each skill is documented in its own file and is intended to be reusable,
focused, and easy to compose with other skills.

## Purpose

This repository is for:

- Defining domain-specific and workflow-specific AI skills.
- Keeping skill instructions modular and maintainable.
- Providing a central place for experimentation and iteration.

## Repository Structure

- One file per skill (for example, `opencode.md`).
- Every skill file should include:
  - A clear name and description.
  - When to use the skill.
  - When not to use the skill.
  - Practical execution guidance.

## Skill Design Principles

- Keep each skill narrowly scoped.
- Prefer explicit criteria over vague guidance.
- Optimize for predictable, testable behavior.
- Avoid coupling a skill to unrelated conversation context unless required.

## Adding a New Skill

1. Create a new markdown file with a concise, descriptive name.
2. Add frontmatter (if your setup expects it).
3. Document usage criteria and boundaries.
4. Include command examples or workflow steps when relevant.
5. Keep wording short, direct, and action-oriented.

## Current Skills

- `opencode.md`: Delegates self-contained tasks to the OpenCode CLI.

This list will grow as new custom skills are added.

## Contribution Notes

- Prefer small, focused updates.
- Preserve existing style and conventions.
- Update this README when new skill categories are introduced.
