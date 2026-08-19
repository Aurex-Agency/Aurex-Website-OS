# Aurex Website OS

Aurex Website OS is the operating system for planning, designing, building, reviewing, launching, and improving conversion-focused websites for Aurex Agency.

The goal is not one recognizable Aurex visual style. The goal is a repeatable standard of thinking and execution that produces websites that feel custom, premium, modern, useful, memorable, technically strong, and commercially effective.

## Core outcome

Every Aurex website should:

1. Help the business grow through stronger visibility, trust, conversion, and measurement.
2. Give the visitor a distinctive, polished experience intentionally designed for that business.

A beautiful website that does not convert has failed the business.

A converting website that feels generic, confusing, slow, inaccessible, or fragile has also left value on the table.

Aurex aims for both.

## Creative philosophy

Aurex does not choose a trendy style and force the client into it.

The system looks for an ownable creative thread in the business itself: customer outcome, identity, products, services, materials, physical environment, process, language, history, geography, culture, and imagery.

That thread can influence layout, imagery, motion, transitions, surfaces, typography, and copy, but it must strengthen the business story and conversion path rather than become a gimmick.

## Conversion and organic visibility

Conversion is the primary commercial driver. Aurex designs CTA hierarchy, proof, trust, lead capture, post-conversion behavior, and measurement as part of the product experience.

Organic visibility is designed into site architecture, content depth, semantic rendering, internal linking, local relevance where appropriate, performance, accessibility, and technical SEO.

Material SEO and CRO recommendations should be based on evidence rather than folklore.

## Proportional operating modes

Aurex now uses three operating modes so quality does not require maximum model usage on every task.

### QUICK

Small, bounded, low-risk changes inside an approved strategy or design system.

Default: one Claude session, directly relevant files, no broad research, no specialist by default, targeted verification.

### STANDARD

The normal mode for meaningful production work such as a new page pattern, section redesign, lead flow, approved homepage implementation, or focused audit.

Default: primary session, relevant skills, zero specialists by default and one routinely when useful, browser verification. A second requires a distinct unresolved question.

### DEEP

For new websites, major redesigns, site architecture, migrations, major conversion systems, or high-stakes final audits.

DEEP can use broader research and multiple specialists, but only when each has a defined question and deliverable; routine use is capped at three per phase.

DEEP is not the default.

See `FOUNDATION/EFFICIENCY-STANDARD.md` and `/aurex-mode`.

## ChatGPT + Claude collaboration

Aurex is designed around complementary roles:

```text
Human creative lead
        ↓
ChatGPT
strategy + research + creative review + prioritization
        ↓
GitHub
AUREX-BRIEF.md + approved project artifacts
        ↓
Claude Code
local implementation + browser + tests
        ↓
GitHub
AUREX-STATUS.md + branch/PR
        ↓
ChatGPT
focused GitHub review
        ↓
Claude Code
targeted revision + verification
```

GitHub is shared state. Long chat transcripts are not.

Use:

- `templates/AUREX-BRIEF.md` for focused implementation handoffs
- `templates/AUREX-STATUS.md` for current project state
- `templates/AUREX-REVIEW.md` for prioritized review findings
- `FOUNDATION/COLLABORATION-PROTOCOL.md` for the full handoff model
- `COLLABORATION-QUICKSTART.md` for the simple human workflow

## Human + AI relationship

Aurex uses a roughly 50/50 collaboration model.

The system automates research, implementation, refinement, technical work, and QA where useful. The human creative lead remains involved at high-leverage strategic and creative decisions.

Routine execution inside an approved direction should continue autonomously until another material decision is reached.

## Specialist skills

### Coordination and efficiency

- `/aurex-website`
- `/aurex-mode`
- `/aurex-handoff`

### Strategy and creative

- `/aurex-discovery`
- `/aurex-research`
- `/aurex-site-architecture`
- `/aurex-art-direction`
- `/aurex-conversion`
- `/aurex-copy`
- `/aurex-page-design`
- `/aurex-motion`
- `/aurex-responsive`
- `/aurex-seo`
- `/aurex-visual-qa`
- `/aurex-polish` - browser-first, macro-before-micro refinement capped at two passes

### Engineering and production

- `/aurex-stack`
- `/aurex-project-setup`
- `/aurex-engineering`
- `/aurex-form-qa`
- `/aurex-accessibility`
- `/aurex-performance`
- `/aurex-technical-qa`
- `/aurex-launch`

## Specialist agents

- Research Director
- Creative Director
- Conversion Strategist
- SEO Strategist
- Content Strategist
- Motion Director
- Frontend Architect
- Performance Engineer
- Accessibility Reviewer
- QA Reviewer
- Launch Engineer

Specialists improve judgment and context management. They should not create bureaucracy. Prefer one focused specialist over overlapping agents. Agent teams are not the default.

## Engineering default

For a new Aurex SMB marketing site without unusual constraints, the starting point is generally:

- Next.js App Router
- TypeScript
- Tailwind CSS with client-specific design tokens
- React Server Components by default
- Motion as the default premium layer for most React animation
- native CSS for simple transitions and hover/focus states
- GSAP/ScrollTrigger, Rive, and Three.js/React Three Fiber only when an approved concept requires their specialized capabilities
- Radix/shadcn primitives only when useful, with custom styling
- Vercel unless the project requires another platform

This is a default, not doctrine. Sound existing stacks should normally be preserved.

## Quality automation

The production layer includes:

- path-scoped Claude rules
- project setup workflow
- format-on-edit starter using local Prettier only
- pre-push quality gate for typecheck, lint, test, and build scripts
- Playwright desktop/mobile smoke tests
- Playwright + axe accessibility starter
- adaptable GitHub Actions starter
- engineering and launch templates

Automation catches repeatable failures. It does not replace browser review, creative judgment, or manual accessibility testing.

Motion AI Kit is configured once in the Claude Code development environment, not installed into every client site. It supplies current Motion documentation and implementation tooling while Aurex retains creative direction. Client repositories receive only the runtime dependencies their approved concepts use. See `references/MOTION-AI-TOOLING.md`.

## Production quality principles

Aurex expects server-first rendering, optimized media/fonts, accessibility, secure public inputs, real form delivery verification, meaningful analytics, production build verification, responsive browser QA, performance review, controlled launch, and independent visual QA.

## Repository structure

- `CLAUDE.md` - concise persistent constitution
- `FOUNDATION/` - strategy, quality, efficiency, and collaboration standards
- `.claude/skills/` - reusable workflows
- `.claude/agents/` - specialist reviewers/operators
- `.claude/rules/` - scoped implementation and efficiency rules
- `templates/` - durable project and handoff artifacts
- `starter/` - automation and test starters for client repos
- `references/` - evolving research and patterns
- `references/visual/INDEX.md` - curated visual principles with provenance and anti-copy notes
- `COLLABORATION-QUICKSTART.md` - simple ChatGPT/Claude workflow
- `USAGE.md` - full operating instructions

## Current stage

**Phase 3.6: Visual production loop tightened**

Phase 1 established the Aurex philosophy and workflow.

Phase 2 created the specialist strategy and creative brain.

Phase 3 connected that brain to a production engineering, QA, automation, and launch system.

Phase 3.5 adds proportional QUICK/STANDARD/DEEP operating modes, specialist cost discipline, session/context rules, durable ChatGPT-to-Claude handoffs, project status checkpoints, and a GitHub-centered review loop.

Phase 3.6 adds bounded browser-first polish, macro-before-micro review, explicit Visual Acceptance separate from Technical QA, 1-3 signature moments, and a structured visual reference library without changing the operating modes or mobile approval gate.

The next priority is real-world battle testing on an existing Aurex website so the system can learn from actual implementation behavior rather than continuing to grow only in theory.
