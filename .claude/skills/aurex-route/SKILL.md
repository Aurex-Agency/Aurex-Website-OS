---
name: aurex-route
description: Selects the smallest appropriate Aurex operating mode, model class, specialist scope, and escalation path for a task. Use before substantial work when cost, context, or model choice matters.
disable-model-invocation: true
---

# Aurex Model and Effort Router

Use `FOUNDATION/EFFICIENCY-STANDARD.md` and `FOUNDATION/MODEL-ROUTING-STANDARD.md`.

## Objective

Spend reasoning, context, agents, and model capability in proportion to the task.

Do not maximize intelligence usage. Maximize quality per unit of effort.

## Step 1: classify scope

Choose QUICK, STANDARD, or DEEP.

Prefer the smallest mode that can reliably produce an excellent result.

## Step 2: score reasoning difficulty

Classify as:

- Low: mechanical or well-understood execution
- Medium: meaningful implementation with some judgment
- High: ambiguous, multi-variable, novel, or difficult reasoning

## Step 3: score consequence of error

Classify as:

- Low: easy to detect and reverse, little business impact
- Medium: affects meaningful UX, conversion, SEO, or engineering behavior
- High: production, migration, security, attribution, major creative, architecture, DNS, or other expensive-to-reverse consequence

## Step 4: choose model class

Default mapping:

- Low difficulty + Low risk -> FAST
- Medium difficulty + Low/Medium risk -> STANDARD
- High difficulty + Medium risk -> STANDARD first, escalate if blocked
- Medium difficulty + High risk -> PREMIUM or premium review
- High difficulty + High risk -> PREMIUM

Do not choose PREMIUM because it sounds safer. State the reason.

## Step 5: choose specialists

Use zero specialists by default.

Add one when it supplies expertise or independent judgment the primary session materially lacks.

Add multiple specialists only in DEEP work where each has a distinct question and deliverable.

Avoid overlapping reviews.

## Step 6: define escalation trigger

Before starting, define what would justify a stronger model.

Examples:

- two focused debugging hypotheses fail
- implementation requires changing approved architecture
- evidence is conflicting
- production risk is discovered
- creative decision becomes strategically material
- SEO implications are broader than expected

Do not escalate simply because the first attempt was imperfect.

## Step 7: protect context

Read only the files necessary for the current assignment plus durable project artifacts that contain approved decisions.

Do not reread the entire repo or rerun discovery unless the task requires it.

If escalating, create a compressed escalation brief instead of passing the whole conversation.

## Routing response

For non-trivial routing, return:

```text
MODE:
MODEL CLASS:
REASONING DIFFICULTY:
RISK:
RELEVANT SKILLS:
SPECIALISTS:
FILES/CONTEXT NEEDED:
ESCALATION TRIGGER:
WHY THIS IS SUFFICIENT:
```

Keep this compact.

## Examples

### Copy update

```text
MODE: QUICK
MODEL CLASS: FAST
REASONING DIFFICULTY: Low
RISK: Low
SPECIALISTS: None
ESCALATION: Only if copy change alters approved positioning or conversion promise.
```

### Approved homepage implementation

```text
MODE: STANDARD
MODEL CLASS: STANDARD
REASONING DIFFICULTY: Medium
RISK: Medium
SPECIALISTS: None initially
ESCALATION: Creative Director only if implementation exposes a material unresolved art-direction decision.
```

### New homepage creative direction

```text
MODE: DEEP
MODEL CLASS: PREMIUM for synthesis, STANDARD for research gathering
REASONING DIFFICULTY: High
RISK: High
SPECIALISTS: Creative Director; Research Director only if evidence gathering is substantial
ESCALATION: Human approval required before implementation.
```

### DNS cutover

```text
MODE: DEEP
MODEL CLASS: PREMIUM review
REASONING DIFFICULTY: Medium
RISK: High
SPECIALISTS: Launch Engineer
ESCALATION: Human approval before production change.
```

## Rule

If a cheaper model repeatedly requires rework that costs more than using the stronger model once, the routing decision is bad. Optimize total effort, not just per-call cost.
