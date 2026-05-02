# AGENTS.md

Guidance for Codex agents working in this repository.

## Repository Overview

This is a Codex-native creative writing skills repository. Every installable skill lives under `skills/<skill-name>/` and must contain a valid `SKILL.md`.

## Skill Types

- `cw-command-*`: command-entry skills for explicit writing workflows such as `/bs`, `/write`, `/wiki`, and `/critique`.
- `cw-agent-*`: role skills that make Codex behave like a focused writing specialist such as writer, critic, outliner, or wiki editor.
- Core skills: reusable writing knowledge such as `prose-writing`, `prose-critique`, `story-context`, and `writing-principles`.

## Development Rules

- Keep the repo Codex-only. Do not add alternate runtime package files, plugin metadata, or non-Codex install instructions.
- Keep skill bodies concise. Move large reference material into `resources/` only when it is genuinely useful and discoverable from `SKILL.md`.
- Role skills must describe Codex behavior directly. Do not describe them as external processes.
- Use plain project folders in examples: `story/`, `wiki/`, `kb/`, and `work/`.
- Preserve the rule that Codex subagents are used only when the user explicitly asks for delegated or parallel agent work.

## Validation

Run the Codex skill validator for every skill:

```bash
for d in skills/*; do
  python3 ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py "$d"
done
```

Before committing, also audit for legacy runtime references using the same check defined in CI.
