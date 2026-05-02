# Codex Writing Skills

Creative writing skills for Codex: brainstorming, prose drafting, critique, story structure, wiki documentation, continuity tracking, and Codex role skills that mirror a writing team.

## Install

Copy the skill directories you want into your Codex skills directory, then restart Codex:

```bash
cp -a skills/* ~/.codex/skills/
```

For a smaller install, start with:

```bash
cp -a skills/cw-router \
  skills/cw-command-bs \
  skills/cw-command-write \
  skills/cw-command-wiki \
  skills/cw-command-critique \
  skills/prose-writing \
  skills/brainstorming \
  skills/prose-critique \
  skills/wiki-docs \
  ~/.codex/skills/
```

## Quick Start

Use natural language or the command-entry skills:

```text
/bs Explore five core premises for a cultivation web novel.
/write action-heavy Draft the scene where the protagonist escapes the sect patrol.
/wiki Create a finalized page for the Qi Condensation realm.
/critique Review this chapter for pacing, protagonist motivation, and hook strength.
```

If your Codex client treats slash-prefixed text specially, invoke the skills explicitly:

```text
Use cw-command-bs to brainstorm a magic system.
Use cw-agent-writer to draft chapter one in a fast web-novel style.
Use cw-agent-critic to critique this scene for voice and continuity.
```

## Skill Groups

| Group | Skills |
|---|---|
| Router and commands | `cw-router`, `cw-command-bs`, `cw-command-write`, `cw-command-wiki`, `cw-command-critique` |
| Writing roles | `cw-agent-story-orchestrator`, `cw-agent-draft-orchestrator`, `cw-agent-writer`, `cw-agent-critic`, `cw-agent-reader-sim` |
| Planning roles | `cw-agent-brainstormer`, `cw-agent-outliner`, `cw-agent-character-sim`, `cw-agent-researcher`, `cw-agent-style-creator` |
| Knowledge roles | `cw-agent-knowledge-orchestrator`, `cw-agent-wiki-editor`, `cw-agent-continuity-checker`, `cw-agent-chronicler`, `cw-agent-session-miner`, `cw-agent-graph-maintainer`, `cw-agent-explorer` |
| Core writing knowledge | `brainstorming`, `prose-writing`, `prose-critique`, `story-architecture`, `story-context`, `story-decisions`, `wiki-docs`, `writing-artifacts`, `writing-issues`, `writing-principles`, `writing-staffing`, `orchestrate` |

## Suggested Project Layout

These skills work with plain files. A writing project can use this layout:

```text
my-story/
├── story/                 # Chapters, scenes, manuscript drafts
├── wiki/                  # Reader-facing reference pages
├── kb/                    # Author-facing canon and working knowledge
│   ├── styles/
│   ├── characters/
│   ├── world/
│   ├── timeline/
│   ├── canon/
│   └── issues/
└── work/                  # Temporary outlines, brainstorms, critiques, revisions
```

The layout is a convention, not a runtime dependency. If your project already uses different folders, tell Codex which files or directories contain canon, drafts, and style references.

## Validate

Validate installed or repo-local skills with Codex's skill validator:

```bash
for d in skills/*; do
  python3 ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py "$d"
done
```

## Notes

This repository is Codex-only. It does not provide a separate plugin runtime, package manager integration, or automatic multi-agent execution. The `cw-agent-*` directories are Codex role skills: they guide the current Codex assistant into a specialist writing role, and Codex subagents are used only when the user explicitly asks for delegated or parallel agent work.
