# Aurex Website OS

Aurex Website OS is the operating system for planning, designing, building, reviewing, launching, and improving conversion-focused websites for Aurex Agency.

The goal is not one recognizable Aurex visual style. The goal is a repeatable standard of thinking and execution that produces websites that feel custom, premium, modern, useful, memorable, technically strong, and commercially effective.

## Core outcome

Every Aurex website must do two things at the same time:

1. Help the business grow through stronger visibility, trust, conversion, and measurement.
2. Give the visitor a distinctive, polished experience that feels intentionally designed for that business.

A beautiful website that does not convert has failed the business.

A converting website that feels cheap, generic, confusing, slow, inaccessible, or fragile has also left major value on the table.

Aurex aims for both.

## Aurex design character

Aurex websites should generally feel:

- premium
- modern
- clean without becoming sterile
- visually intentional
- image-led when strong imagery improves the story
- moderately interactive
- unique to the client
- conversion-focused
- easy to understand
- structured for multi-page organic visibility

The system must avoid defaulting to empty white sections, generic cards, stock SaaS layouts, arbitrary gradients, library-default styling, or random motion.

Color, imagery, typography, layout, depth, movement, content, and conversion should work together to create a client-specific visual world.

## Business-native creative direction

Aurex does not select a trendy style first and force the client into it.

The system researches the business, audience, logo, customer outcome, physical environment, products, services, processes, terminology, history, imagery, geography, and competitive category to find an ownable creative thread.

That thread may influence layout, imagery, motion, transitions, surfaces, copy, or interaction. The concept must help tell the business story and support conversion rather than becoming a gimmick.

## Conversion is the primary business driver

Aurex websites are business assets, not digital brochures.

Every project should establish:

- primary conversion
- secondary conversions
- visitor intent
- objections
- proof requirements
- CTA hierarchy
- lead-capture experience
- post-conversion behavior
- analytics and measurement

Forms and lead flows are treated as designed product interactions and are tested through real delivery, error, mobile, accessibility, and tracking paths.

## Organic visibility is part of the product

Aurex sites should support discoverability and long-term organic growth through useful information architecture, page depth, technical SEO, local relevance where appropriate, semantic rendering, internal linking, performance, accessibility, and content quality.

Material SEO decisions should be based on evidence and current guidance rather than folklore, keyword stuffing, or arbitrary tool scores.

## Human + AI collaboration

Aurex Website OS uses a roughly 50/50 collaboration model.

The system should automate research, production, refinement, technical work, and QA where doing so saves time. The human creative lead remains involved at high-leverage strategic and creative decisions.

Once a direction is approved, routine execution should continue autonomously until another material decision is reached.

## Specialist operating brain

### Strategy and creative skills

- `/aurex-website`
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

### Engineering and production skills

- `/aurex-stack`
- `/aurex-project-setup`
- `/aurex-engineering`
- `/aurex-form-qa`
- `/aurex-accessibility`
- `/aurex-performance`
- `/aurex-technical-qa`
- `/aurex-launch`

### Specialist agents

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

Specialists improve judgment and context management. They should not create bureaucracy or fragment the overall website strategy.

## Engineering default

For a new Aurex SMB marketing site without unusual constraints, the default starting point is:

- Next.js App Router
- TypeScript
- Tailwind CSS with client-specific design tokens
- React Server Components by default
- Motion for most animation
- GSAP/ScrollTrigger only for advanced choreography
- Radix/shadcn primitives only when useful, with custom visual styling
- Vercel by default unless the client requires another platform

This is a default, not a mandatory answer. Existing sound stacks should normally be preserved.

## Quality automation

Phase 3 adds a reusable engineering automation layer:

- path-scoped Claude rules for frontend architecture, design implementation, media, motion, SEO rendering, accessibility, forms, analytics, security, and verification
- project setup workflow that adapts the OS to the actual client repo
- optional format-on-edit hook when local Prettier exists
- pre-push quality hook that blocks Claude-driven `git push` when configured typecheck, lint, test, or build scripts fail
- Playwright smoke-test starter
- Playwright + axe accessibility-test starter
- GitHub Actions quality starter that must be adapted to the actual package manager and scripts
- durable engineering and launch templates

Automation catches repeatable failures. It does not replace browser review, creative judgment, or manual accessibility testing.

## Production quality principles

Aurex expects:

- server-first rendering and narrow client boundaries
- optimized media and fonts
- evidence-based Core Web Vitals work
- WCAG 2.2 AA as the normal accessibility target
- secure handling of public inputs and secrets
- real form delivery verification
- meaningful analytics events
- production build verification
- responsive browser QA
- independent visual QA
- controlled launch and post-launch checks

Current Core Web Vitals good targets are LCP <= 2.5s, INP <= 200ms, and CLS <= 0.1 at the 75th percentile. Field data is preferred when available.

## Repository structure

- `CLAUDE.md` - persistent operating constitution
- `FOUNDATION/` - principles and quality standards
- `.claude/skills/` - reusable operating workflows
- `.claude/agents/` - specialist reviewers and operators
- `.claude/rules/` - scoped implementation rules
- `templates/` - durable project artifacts
- `starter/` - automation and test starters copied/adapted into client repos
- `references/` - evolving research and patterns
- `USAGE.md` - instructions for using the OS across client repositories

## Current stage

**Phase 3: Engineering and automation layer built**

Phase 1 established the Aurex philosophy and workflow.

Phase 2 created the specialist strategy and creative brain.

Phase 3 connects that brain to a production engineering system with stack selection, implementation standards, deterministic quality gates, browser testing, accessibility, performance, security, analytics, technical QA, and controlled launch procedures.

The next major evolution should focus on packaging, one-command project bootstrap, deeper visual regression/browser automation, reusable integration adapters, and learning from real Aurex client projects without allowing the system to converge on one visual aesthetic.
