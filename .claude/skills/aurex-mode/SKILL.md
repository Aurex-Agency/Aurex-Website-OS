---
name: aurex-mode
description: Selects QUICK, STANDARD, or DEEP operating mode for an Aurex task so reasoning, specialist use, context loading, and verification stay proportional to the work.
---

# Aurex Mode Selector

Use this skill at the beginning of a meaningful task when the correct level of Aurex process is not already obvious.

Read `FOUNDATION/EFFICIENCY-STANDARD.md`.

## Goal

Choose the smallest operating mode that can reliably produce an excellent result.

Do not equate deeper process with higher quality.

## Step 1: summarize the task in one sentence

State the actual work unit, not the entire project.

Example:

Bad: "Improve the client website."

Better: "Replace the approved homepage hero with the new video-led composition and preserve the existing conversion hierarchy."

## Step 2: score the task qualitatively

Consider:

- strategic impact
- creative impact
- reversibility
- conversion impact
- SEO impact
- accessibility risk
- security/analytics risk
- implementation complexity
- uncertainty
- whether the pattern will be reused widely

## Step 3: choose the mode

### QUICK

Choose when the work is bounded, low-risk, and inside an approved strategy/design language.

Expected operating plan:

- primary session only
- directly relevant files only
- no broad research
- no specialist by default
- targeted verification

### STANDARD

Choose for meaningful page, feature, conversion, content, or design work that needs focused reasoning and browser verification.

Expected operating plan:

- primary session
- relevant Aurex skills
- zero to two focused specialists when useful
- existing strategy artifacts as context
- browser verification for user-facing work
- update durable project memory if a reusable decision changes

### DEEP

Choose for a new website, major redesign, architecture/migration decision, major conversion system, or final high-stakes audit.

Expected operating plan:

- broader research as justified
- multiple specialists only when each has a distinct question
- major human approval gates
- comprehensive verification appropriate to the work

## Step 4: state the plan concisely

Return:

```text
MODE: QUICK | STANDARD | DEEP

WHY:
<1-3 sentences>

CONTEXT TO LOAD:
- ...

SKILLS NEEDED:
- ...

SPECIALISTS:
- none | named specialists with exact question

VERIFICATION:
- ...

HUMAN DECISION REQUIRED:
- none | exact decision
```

## Escalation

If implementation reveals materially greater uncertainty or risk, explicitly recommend an escalation.

Example:

"This started as QUICK, but the requested CTA change affects the shared lead-routing architecture and analytics events. Escalating to STANDARD."

Do not silently expand into a full project audit.

## Cost awareness

Do not estimate model tokens unless the environment provides reliable usage data.

Instead reason about relative cost:

- low
- moderate
- high

Do not sacrifice required verification solely to stay in a cheaper mode.
