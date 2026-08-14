# Aurex Website OS

Aurex Website OS is the operating system for planning, designing, building, reviewing, launching, and improving conversion-focused websites for Aurex Agency.

The goal is not to create one recognizable visual style. The goal is to create a repeatable standard of thinking and execution that produces websites that feel custom, premium, modern, useful, memorable, and commercially effective.

## Core outcome

Every Aurex website must do two things at the same time:

1. Help the business grow through stronger visibility, trust, conversion, and measurement.
2. Give the visitor a distinctive, pleasant, polished experience that feels intentionally designed for that brand.

A beautiful website that does not convert has failed the business.

A converting website that feels cheap, generic, confusing, or forgettable has left major value on the table.

Aurex aims for both.

## Aurex design character

Aurex websites should generally feel:

- premium
- modern
- clean without becoming sterile
- visually intentional
- image-led when strong imagery can improve the experience
- moderately interactive
- unique to the client
- conversion-focused
- easy to understand
- structured for multi-page organic visibility

The system must avoid defaulting to large amounts of empty white space, generic card grids, stock SaaS patterns, or arbitrary motion. Color, imagery, typography, layout, depth, and movement should work together to create an intentional visual world for each client.

## Business-native creative direction

Aurex does not select a trendy style first and force the client into it.

The system researches the business, audience, logo, customer outcome, physical environment, products, services, processes, terminology, history, imagery, geography, and competitive category to find an ownable creative thread.

That thread may influence layout, imagery, motion, transitions, surfaces, copy, or interaction. The concept must help tell the client's story and support conversion rather than becoming a decorative gimmick.

## Conversion is the primary business driver

Aurex websites are business assets, not digital brochures.

Every project must establish:

- the primary conversion
- secondary conversions
- visitor intent
- key objections
- trust requirements
- proof strategy
- CTA hierarchy
- page-level conversion goals
- lead-capture experience
- post-conversion behavior
- analytics and measurement requirements

Conversion architecture should be present throughout the experience without making the site feel aggressive or repetitive.

Forms and lead flows are treated as designed product interactions. The system should reduce unnecessary friction, choose the appropriate form pattern for the job, and test lead delivery end to end.

## Organic visibility is part of the product

Aurex sites should be built to support discoverability and long-term organic growth. That includes thoughtful information architecture, useful page depth, local and topical relevance where appropriate, technical SEO, structured data, internal linking, semantic HTML, performance, accessibility, and content quality.

SEO decisions should be based on evidence and current best practices rather than superstition, keyword stuffing, or arbitrary scoring tools.

## Human + AI collaboration

Aurex Website OS uses a roughly 50/50 collaboration model.

The system should automate research, analysis, production, refinement, and QA where doing so saves time. The human creative lead stays involved at high-leverage strategic and creative decisions.

Once a direction is approved, the system should handle routine implementation autonomously rather than requesting approval for every small decision.

## Specialist operating brain

Phase 2 adds reusable Claude Code skills and specialist agents so the system can apply Aurex methods consistently instead of relying on one giant prompt.

### Skills

- `/aurex-website` coordinates the complete project lifecycle
- `/aurex-discovery` develops project-specific business and customer insight
- `/aurex-research` grounds material decisions in evidence
- `/aurex-site-architecture` designs useful multi-page structure and internal linking
- `/aurex-art-direction` develops business-native creative directions
- `/aurex-conversion` designs CTA, form, trust, and lead-flow systems
- `/aurex-copy` develops specific human-sounding website messaging
- `/aurex-page-design` translates strategy into page narratives and implementation
- `/aurex-motion` creates a purposeful motion language
- `/aurex-responsive` treats mobile and intermediate widths as active design problems
- `/aurex-seo` plans and audits evidence-based organic visibility
- `/aurex-visual-qa` performs browser-based quality review and iteration

### Specialist agents

- Research Director
- Creative Director
- Conversion Strategist
- SEO Strategist
- Content Strategist
- Motion Director
- Frontend Architect
- QA Reviewer

Specialists should improve judgment and context management, not create bureaucracy. Major cross-disciplinary decisions remain coordinated through the primary project conversation.

## Executive output quality

Major Aurex outputs should follow `FOUNDATION/OUTPUT-STANDARD.md`.

The system should lead with the recommendation, prioritize the highest-impact findings, distinguish facts from judgment, state confidence and uncertainty honestly, explain tradeoffs, and make the next action obvious.

Final website quality is reviewed against `FOUNDATION/QUALITY-SCORECARD.md` and the browser-based QA process.

## Repository structure

- `CLAUDE.md` - persistent operating constitution for Claude Code
- `FOUNDATION/AUREX-PRINCIPLES.md` - core Aurex website principles
- `FOUNDATION/CREATIVE-CONCEPT-METHOD.md` - method for discovering business-native creative ideas
- `FOUNDATION/LEAD-CONVERSION-STANDARD.md` - lead capture and form UX standard
- `FOUNDATION/PROJECT-WORKFLOW.md` - full collaborative project lifecycle
- `FOUNDATION/OUTPUT-STANDARD.md` - high-level consultant output standard
- `FOUNDATION/QUALITY-SCORECARD.md` - internal final-quality judgment framework
- `templates/` - durable project artifact templates
- `.claude/skills/` - reusable specialist workflows
- `.claude/agents/` - specialist reviewers and operators
- `.claude/rules/` - scoped implementation rules to be added in a later phase
- `references/` - evolving research, patterns, anti-patterns, and inspiration knowledge
- `USAGE.md` - instructions for attaching the OS to client repositories

## Current stage

**Phase 2: Specialist brain built**

Phase 1 established the principles, creative concept method, lead conversion standard, workflow, collaboration model, and project brief.

Phase 2 adds the reusable skill layer, specialist agents, executive output standard, quality scorecard, project handoff templates, and cross-repository usage workflow.

The next phase should focus on implementation infrastructure: frontend engineering rules, preferred stack and dependency policy, browser automation and visual verification, deterministic hooks, accessibility and technical QA automation, analytics standards, launch checks, and a cleaner distribution method such as packaging the OS for repeated use across client repositories.
