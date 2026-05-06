# OKR-First Convention

This convention applies to any AI agent working on a project with OKRs.

## Before Starting Any Task

1. Check if `.okr.md` exists (or query okr.io via MCP if connected)
2. Read the current Objective and Key Results
3. Ask: **Does this task move a KR?**

If yes: proceed, and note which KR it serves.
If no: pause. Either the task shouldn't be done, or the OKRs are missing something.

## The Question That Matters

Before writing code, drafting content, or doing research, ask:

> "Which Key Result does this move? By how much?"

If you can't answer, the task is probably not important.

## During Execution

Reference the OKRs in your work:
- "This implements the onboarding flow for KR1 (Get 80% completion rate)"
- "This research supports KR2 (Close 3 paid pilots) by identifying procurement blockers"

This keeps work connected to outcomes, not just activity.

## After Completion

Report progress:
- Update `.okr.md` with new current values
- Or call the MCP `update_progress` tool if using okr.io
- Note any blockers that emerged

## When Blocked

Update KR status to `at_risk` with a clear blocker description.

Don't hide problems. Surface them early so they can be addressed.

## Anti-Patterns

**Working without checking OKRs**: Every session should start with OKR context.

**Tasks that don't connect to KRs**: If a task doesn't move any KR, question whether it should exist.

**Finishing without reporting**: Progress not recorded is progress lost across sessions.

**Hiding blockers**: At-risk is not failure. It's visibility.

## Integration

### Standalone
Keep `.okr.md` at repo root. Read it at session start. Update it when progress happens.

### With okr.io MCP
Query `/context` for current OKRs at session start. Call `update_progress` or `check_in` tools to report status.

## Why This Matters

AI agents are powerful but stateless. Without OKR context, they optimize for local tasks, not strategic outcomes.

OKR-first means every action is connected to what actually matters.
