# Codex Writing Skills Architecture

## Layers

```mermaid
flowchart TB
    User[User request] --> Router[cw-router]
    User --> Workflows[cw-brainstorm / cw-write / cw-wiki / cw-critique]

    Router --> Roles[cw-agent-* role skills]
    Workflows --> Roles
    Workflows --> Core[Core writing skills]
    Roles --> Core

    Core --> Project[story / wiki / kb / work files]
```

## Workflow Skills

Workflow skills provide short, explicit Codex entrypoints:

| Skill | Use |
|---|---|
| `cw-brainstorm` | Explore story ideas without committing to canon |
| `cw-write` | Draft or revise prose |
| `cw-wiki` | Document finalized canon |
| `cw-critique` | Critique existing prose |

These are Codex skills, not client commands. Invoke them by name in natural language.

## Role Skills

Role skills guide the current Codex assistant into specialist writing behavior:

| Area | Role skills |
|---|---|
| Orchestration | `cw-agent-story-orchestrator`, `cw-agent-draft-orchestrator`, `cw-agent-knowledge-orchestrator` |
| Creation | `cw-agent-writer`, `cw-agent-brainstormer`, `cw-agent-outliner`, `cw-agent-character-sim`, `cw-agent-style-creator` |
| Review | `cw-agent-critic`, `cw-agent-reader-sim`, `cw-agent-continuity-checker` |
| Knowledge | `cw-agent-wiki-editor`, `cw-agent-chronicler`, `cw-agent-session-miner`, `cw-agent-graph-maintainer`, `cw-agent-explorer`, `cw-agent-researcher` |

Role skills may coordinate a workflow, but they do not imply automatic parallel execution. Codex subagents are used only when the user explicitly asks for delegated or parallel agent work.

## Project Files

The skills assume ordinary files and directories:

- `story/`: chapters, scenes, manuscript drafts
- `wiki/`: reader-facing reference pages
- `kb/`: author-facing canon, character state, timeline, style, issues
- `work/`: temporary brainstorms, outlines, critique notes, and revision artifacts

Projects can use different names if the user points Codex to the relevant files.
