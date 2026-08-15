---
name: aurex-engineering
description: Implements an approved Aurex design and strategy as production-quality frontend code while preserving creative specificity, conversion, SEO, accessibility, responsiveness, and performance. Use during page and component implementation.
---

# Aurex Engineering

Read the approved project artifacts before coding:

- PROJECT-BRIEF.md
- WEBSITE-STRATEGY.md
- CREATIVE-DIRECTION.md
- DESIGN-SYSTEM.md
- relevant PAGE-SPEC.md

Also follow `FOUNDATION/ENGINEERING-STANDARD.md` and the active `.claude/rules/`.

## Step 1: Understand before editing

Identify:

- page objective
- primary conversion
- approved creative concept
- required media
- page-specific interaction
- shared primitives
- SEO intent
- accessibility risks
- responsive behavior

Do not invent a new visual direction during implementation.

## Step 2: Inspect the codebase

Understand:

- framework/version
- app structure
- existing tokens
- existing primitives
- routing
- data/content patterns
- analytics
- form architecture
- animation libraries
- build/test commands

Reuse good infrastructure. Do not preserve bad visual patterns merely because they already exist.

## Step 3: Plan boundaries

Decide:

- server versus client component boundaries
- shared primitives versus page-specific sections
- media loading strategy
- animation responsibility
- data/content model
- form submission path
- analytics events

Keep client boundaries narrow.

## Step 4: Implement the design system

Before repeating visual values, ensure project tokens represent the approved system.

Do not let library defaults substitute for design decisions.

## Step 5: Implement composition

Build the page according to content meaning, not a generic section template.

Preserve:

- hierarchy
- rhythm
- imagery
- transition logic
- CTA visibility
- signature creative moments

Do not over-componentize one-off creative sections until abstraction has a clear benefit.

## Step 6: Implement interaction

Use the lightest appropriate technique:

1. CSS for simple states
2. Motion for ordinary React interaction and animation
3. GSAP/ScrollTrigger for advanced timeline or scroll choreography

Implement reduced-motion behavior with the interaction, not later as a patch.

## Step 7: Implement conversion

For lead flows:

- semantic fields
- server validation
- states for loading/error/success
- abuse protection
- real delivery integration
- analytics
- mobile behavior

## Step 8: Verify during implementation

After meaningful visual changes:

- render in browser
- inspect desktop
- inspect mobile
- check console
- test primary interaction

Do not wait until the entire website is complete to discover the visual system is wrong.

## Step 9: Technical review

Before handing the page back:

- run relevant type/lint/build checks
- confirm no accidental client-boundary expansion
- confirm media strategy
- confirm metadata/page semantics where relevant
- test reduced motion
- test keyboard behavior for new controls
- test primary CTA/form behavior

## Output

Report:

### Implemented
What changed.

### Visual fidelity
How implementation matches the approved concept.

### Technical decisions
Only material decisions and why.

### Verification
What was actually tested.

### Remaining risks
Anything not yet verified or requiring assets/integrations.

### Human review point
The exact visual/strategic decision needing approval, if any.