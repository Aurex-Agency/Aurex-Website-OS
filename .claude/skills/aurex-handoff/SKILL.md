---
name: aurex-handoff
description: Creates a concise durable handoff between ChatGPT, Claude Code, and the human creative lead without transferring entire chat histories.
---

# Aurex Handoff

Use this skill when work is moving between strategy/review and implementation, or when a Claude session is ending and another session or ChatGPT needs the current state.

Read `FOUNDATION/COLLABORATION-PROTOCOL.md`.

## Determine handoff direction

Choose one:

- ChatGPT or human strategy -> Claude implementation
- Claude implementation -> ChatGPT review
- Claude session -> fresh Claude session
- review -> revision implementation

## Strategy to implementation

Create or update `AUREX-BRIEF.md`.

Include only information needed to execute the current work:

1. objective
2. business reason
3. operating mode
4. approved context
5. exact scope
6. required content/assets
7. creative constraints
8. conversion requirements
9. technical constraints
10. acceptance criteria
11. what must not change
12. unresolved decisions
13. required verification
14. human approval gate

Reference existing artifacts instead of copying them wholesale.

## Implementation to review

Update `AUREX-STATUS.md`.

Include:

1. current branch or PR
2. task completed
3. files/areas materially changed
4. implementation decisions worth preserving
5. verification performed
6. known limitations or unverified areas
7. exact review requested from ChatGPT or the human
8. recommended next action

Do not write a chronological diary of everything Claude did.

## Session to fresh session

Before ending or clearing a long session:

- ensure approved decisions are in durable project artifacts
- update `AUREX-STATUS.md`
- list unresolved blockers
- list the next action
- remove stale status information when it is no longer relevant

The next session should not require the previous transcript.

## Review to revision

When translating review findings into implementation work, create a focused revision brief.

Order feedback:

1. blockers
2. important revisions
3. polish
4. optional experiments

For each required revision state:

- issue
- why it matters
- intended outcome
- acceptance criteria

Do not over-prescribe code unless the implementation method itself matters.

## Output rule

The handoff should be concise enough that a new session can read it quickly but complete enough that it does not need the old transcript.

If the handoff is becoming long, move stable information into its proper project artifact and reference it.
