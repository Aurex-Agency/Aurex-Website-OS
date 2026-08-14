---
name: aurex-website
description: Orchestrates a full Aurex website project from intake through launch and post-launch learning. Use when starting, continuing, or coordinating a complete client website build.
disable-model-invocation: true
---

# Aurex Website Orchestrator

Use this skill as the top-level operating workflow for a complete Aurex website project.

## First rule

Do not jump into implementation because a client name, logo, or current website is available. Establish enough strategy and creative direction to make the build intentional.

Read the relevant foundation standards before major decisions:

- `FOUNDATION/AUREX-PRINCIPLES.md`
- `FOUNDATION/PROJECT-WORKFLOW.md`
- `FOUNDATION/CREATIVE-CONCEPT-METHOD.md`
- `FOUNDATION/OUTPUT-STANDARD.md`
- `FOUNDATION/QUALITY-SCORECARD.md`
- `FOUNDATION/LEAD-CONVERSION-STANDARD.md` when lead generation is relevant
- `FOUNDATION/ENGINEERING-STANDARD.md` during implementation
- `FOUNDATION/PERFORMANCE-STANDARD.md` during performance work
- `FOUNDATION/ACCESSIBILITY-STANDARD.md` during implementation and QA
- `FOUNDATION/SECURITY-STANDARD.md` when handling public inputs, integrations, authentication, or secrets
- `FOUNDATION/ANALYTICS-STANDARD.md` for measurement
- `FOUNDATION/QUALITY-AUTOMATION.md` when configuring hooks, browser tests, or CI
- active project artifacts and approved decisions

## Operating sequence

1. Intake and brief
2. Discovery and research
3. Positioning and conversion strategy
4. Site architecture
5. Creative direction
6. Technical stack validation and project setup
7. Design system, engineering plan, and homepage structure
8. Hero visual proof
9. Homepage build
10. Homepage visual and technical verification
11. Page-category bundles
12. Content and SEO depth
13. Conversion review and form QA
14. Motion and interaction pass
15. Responsive and accessibility QA
16. Performance audit
17. Technical QA
18. Final independent creative/QA review
19. Launch readiness and launch
20. Post-launch measurement and learning

Use the dedicated Aurex skills for each specialist stage instead of improvising a new process.

## Specialist skills

Use the skill that matches the task:

- `/aurex-discovery`
- `/aurex-research`
- `/aurex-site-architecture`
- `/aurex-art-direction`
- `/aurex-conversion`
- `/aurex-copy`
- `/aurex-stack`
- `/aurex-project-setup`
- `/aurex-engineering`
- `/aurex-page-design`
- `/aurex-motion`
- `/aurex-responsive`
- `/aurex-seo`
- `/aurex-form-qa`
- `/aurex-accessibility`
- `/aurex-performance`
- `/aurex-technical-qa`
- `/aurex-visual-qa`
- `/aurex-launch`

## Specialist delegation

Use agents when independent context, deep expertise, or an unbiased second opinion improves the result.

Examples:

- Research Director for broad evidence gathering and synthesis
- Creative Director at concept and visual approval gates
- Conversion Strategist for important lead-flow decisions
- SEO Strategist for architecture, migration, and material organic decisions
- Content Strategist for messaging hierarchy and copy review
- Motion Director for signature interactions
- Frontend Architect for implementation risks and architecture choices
- Performance Engineer for Core Web Vitals and runtime/media cost
- Accessibility Reviewer for WCAG 2.2 AA and manual interaction review
- QA Reviewer for independent pre-approval review
- Launch Engineer for production migration and release verification

Do not delegate every task simply because an agent exists. Keep cross-disciplinary synthesis in the main project conversation.

## Collaboration behavior

Operate autonomously inside an approved direction. Escalate decisions when they are highly subjective, expensive to reverse, strategically material, based on weak/conflicting evidence, or represent multiple strong options.

When escalating, provide:

1. the recommended choice
2. why it is recommended
3. strongest alternatives
4. tradeoffs
5. the exact decision required from the human creative lead

Do not ask for approval on routine implementation details.

## Project state

At the start of a session, determine the current stage from existing files and code. Do not restart discovery or redo approved work without a reason.

Recommended durable project artifacts include:

- `PROJECT-BRIEF.md`
- `DISCOVERY.md`
- `WEBSITE-STRATEGY.md`
- `SITE-ARCHITECTURE.md`
- `CREATIVE-DIRECTION.md`
- `DESIGN-SYSTEM.md`
- `ENGINEERING-PLAN.md`
- page specs as needed
- `SEO-PLAN.md` where complexity warrants it
- `CONVERSION-PLAN.md` where complexity warrants it
- `QA-REPORT.md`
- `LAUNCH-CHECKLIST.md`

Use templates when they preserve decisions and improve handoff. Do not create documents only to make the process look sophisticated.

## Engineering behavior

Before major implementation:

- validate the stack with `/aurex-stack`
- configure the project with `/aurex-project-setup` when adopting the OS
- create the engineering plan for non-trivial projects
- preserve server-first rendering and narrow client boundaries
- encode client-specific design tokens
- define media and motion responsibility
- define primary conversion delivery and measurement

During implementation, use `/aurex-engineering` and verify in the actual browser repeatedly.

## Quality control

Do not equate completion with code generation.

At major build milestones verify against:

- business objective
- conversion strategy
- creative concept
- visual hierarchy and imagery
- responsive behavior
- accessibility
- SEO intent and crawlability
- performance
- security
- analytics
- actual browser experience

Use `FOUNDATION/QUALITY-SCORECARD.md` as an internal diagnostic framework. A high average cannot compensate for a broken conversion, inaccessible interaction, crawlability mistake, exposed secret, or failed production build.

## Pre-launch gate

Before launch readiness, run as relevant:

1. `/aurex-form-qa`
2. `/aurex-accessibility`
3. `/aurex-performance`
4. `/aurex-technical-qa`
5. `/aurex-visual-qa`

Resolve blockers and critical findings.

Then use `/aurex-launch` with the project launch checklist.

## Evidence standard

When a recommendation depends on a current technical fact, standard, SEO behavior, security practice, accessibility rule, browser behavior, or library/framework capability, prefer current primary documentation.

Do not turn remembered defaults into permanent Aurex doctrine when tools evolve.

## Output quality

Major strategy, research, audit, and approval outputs must follow `FOUNDATION/OUTPUT-STANDARD.md`.

Lead with the recommendation. Prioritize findings. Distinguish facts from judgment. Explain important mechanisms and tradeoffs. Surface uncertainty honestly. Make the next action obvious.

## Anti-rush rule

If the site looks generic, repetitive, weakly branded, poorly converted, visually unfinished, inaccessible, slow, insecure, difficult to crawl, or technically fragile, continue iterating.

Do not declare success because requested files exist, the page renders, or a deploy completed.
