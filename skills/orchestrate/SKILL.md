---
name: orchestrate
description: Use when coordinating multi-step creative writing work across brainstorming, outlining, drafting, critique, revision, documentation, or knowledge maintenance.
---

# Orchestrate

Coordinate the workflow without losing the author's intent. Your value is choosing the right next step, preserving context, synthesizing results, and keeping exploratory material separate from confirmed canon.

## Core Pattern

1. Clarify the goal, scope, constraints, and target reader experience.
2. Gather only the context needed for the current step from `story/`, `wiki/`, `kb/`, `work/`, or user-provided text.
3. Choose the narrowest role or core skill that fits the next action.
4. Produce or synthesize the artifact requested by the user.
5. Record decisions and unresolved questions when they affect future writing.

## Coordination Rules

- Do the bounded work locally unless the user explicitly asks for delegated or parallel agent work.
- If delegation is requested, split work into independent roles such as brainstormer, writer, critic, reader-sim, or researcher.
- Match context to role: writers need briefs and style; critics need drafts and focus; wiki work needs confirmed sources; continuity checks need canon.
- Do not turn uncertain brainstorm material into canon without user confirmation.
- Keep a short synthesis after multi-step work: what changed, what still risks contradiction, and what should happen next.

## Common Flows

- Brainstorm -> choose direction -> outline -> draft -> critique -> revise -> record decisions.
- Draft -> reader response -> critique synthesis -> targeted revision.
- New canon -> wiki update -> knowledge-base update -> continuity check.
