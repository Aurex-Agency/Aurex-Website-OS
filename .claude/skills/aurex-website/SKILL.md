---
name: aurex-website
description: Orchestrates a complete Aurex website project while matching process depth to the task. Use when starting, continuing, or coordinating client website work.
disable-model-invocation: true
---

# Aurex Website Orchestrator

Use this skill as the top-level operating workflow for Aurex website work.

## First decision: choose the operating mode

Before expanding context or invoking specialists, read `FOUNDATION/EFFICIENCY-STANDARD.md` and choose the smallest mode that can reliably produce an excellent result.

Use `/aurex-mode` when the correct mode is not obvious.

### QUICK

For bounded, low-risk changes inside approved strategy and design language.

Default: primary session, directly relevant files, no broad research, no specialist by default, targeted verification.

### STANDARD

For meaningful page, feature, conversion, design, or content work.

Default: primary session, relevant skills, zero to two focused specialists when useful, browser verification, durable artifact updates when decisions change.

STANDARD is the normal default for day-to-day production work.

### DEEP

For new websites, major redesigns, architecture or migration decisions, major conversion systems, or final high-stakes reviews.

Use multiple specialists only when each has a distinct question and deliverable.

Do not use DEEP merely because the project is important while the current task is small.

## Shared foundation

Read only the standards relevant to the current work. Do not load every foundation document automatically.

Common references include:

- `FOUNDATION/AUREX-PRINCIPLES.md`
- `FOUNDATION/PROJECT-WORKFLOW.md`
- `FOUNDATION/CREATIVE-CONCEPT-METHOD.md`
- `FOUNDATION/EFFICIENCY-STANDARD.md`
- `FOUNDATION/COLLABORATION-PROTOCOL.md`
- `FOUNDATION/OUTPUT-STANDARD.md`
- `FOUNDATION/QUALITY-SCORECARD.md`
- `FOUNDATION/LEAD-CONVERSION-STANDARD.md` when lead generation is relevant
- `FOUNDATION/ENGINEERING-STANDARD.md` during implementation
- `FOUNDATION/PERFORMANCE-STANDARD.md` during performance work
- `FOUNDATION/ACCESSIBILITY-STANDARD.md` during implementation and QA
- `FOUNDATION/SECURITY-STANDARD.md` when handling public inputs, integrations, authentication, or secrets
- `FOUNDATION/ANALYTICS-STANDARD.md` for measurement
- `FOUNDATION/QUALITY-AUTOMATION.md` for hooks, browser tests, or CI
- active project artifacts and approved decisions

## Full project sequence

DEEP new-site work normally moves through:

1. Intake and brief
2. Discovery and research
3. Positioning and conversion strategy
4. Site architecture
5. Creative direction
6. Technical stack validation and project setup
7. Design system, engineering plan, and homepage structure
8. Hero visual proof
9. Homepage build and verification
10. Page-category bundles
11. Content and SEO depth
12. Conversion review and form QA
13. Motion and interaction pass
14. Responsive and accessibility QA
15. Performance audit
16. Technical QA
17. Final independent creative/QA review
18. Launch readiness and launch
19. Post-launch measurement and learning

QUICK and STANDARD tasks should not replay this full sequence. Enter at the relevant stage and perform only the process required for the current work unit.

## Specialist skills

Use only the skills relevant to the task:

- `/aurex-mode`
- `/aurex-handoff`
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

Before invoking an agent, define the exact question and expected output.

Useful specialists include:

- Research Director for broad evidence gathering
- Creative Director for major concept and visual judgment
- Conversion Strategist for material lead-flow decisions
- SEO Strategist for architecture, migration, and material organic decisions
- Content Strategist for messaging hierarchy and copy review
- Motion Director for signature interactions
- Frontend Architect for implementation risks and architecture choices
- Performance Engineer for Core Web Vitals and runtime/media cost
- Accessibility Reviewer for WCAG 2.2 AA and manual interaction review
- QA Reviewer for independent pre-approval review
- Launch Engineer for production migration and release verification

Do not delegate every task because agents exist. Prefer one focused specialist over overlapping specialists. Do not use agent teams by default.

## ChatGPT and Claude collaboration

Follow `FOUNDATION/COLLABORATION-PROTOCOL.md` when work is moving between ChatGPT strategy/review and Claude implementation.

Use:

- `AUREX-BRIEF.md` for focused implementation assignments
- `AUREX-STATUS.md` for current project state and handoff
- `AUREX-REVIEW.md` for focused review findings

Do not copy whole chat transcripts into project context.

Claude should implement from approved durable decisions. After meaningful work, update status and push the focused branch or PR. ChatGPT can review the GitHub implementation and return prioritized revision requirements.

## Collaboration behavior

Operate autonomously inside approved direction. Escalate decisions when they are highly subjective, expensive to reverse, strategically material, based on weak or conflicting evidence, or represent multiple strong options.

When escalating, provide:

1. recommendation
2. reasoning
3. strongest alternatives
4. tradeoffs
5. exact decision required from the human creative lead

Do not ask for approval on routine implementation details.

## Project state and context discipline

At the start of a session:

1. read `AUREX-STATUS.md` when present
2. read only the approved artifacts relevant to the current task
3. inspect only the source files necessary to understand the work
4. do not restart discovery or repeat settled research without a reason

Recommended durable artifacts include:

- `PROJECT-BRIEF.md`
- `DISCOVERY.md`
- `WEBSITE-STRATEGY.md`
- `SITE-ARCHITECTURE.md`
- `CREATIVE-DIRECTION.md`
- `DESIGN-SYSTEM.md`
- `ENGINEERING-PLAN.md`
- `AUREX-BRIEF.md`
- `AUREX-STATUS.md`
- page specs as needed
- `SEO-PLAN.md` where complexity warrants it
- `CONVERSION-PLAN.md` where complexity warrants it
- `QA-REPORT.md`
- `LAUNCH-CHECKLIST.md`

Before clearing or ending a long session, preserve durable decisions and update `AUREX-STATUS.md` so the next session does not require the old transcript.

## Engineering behavior

Before major implementation, validate the stack and project quality setup when relevant. During implementation, preserve the approved creative language, server-first rendering, accessibility, media responsibility, conversion delivery, and measurement.

Use browser inspection repeatedly for user-facing work.

## Verification depth

Match verification to the operating mode and risk.

QUICK: targeted checks for the changed behavior.

STANDARD: browser inspection, relevant tests, responsive review, and affected conversion/accessibility checks.

DEEP: comprehensive checks appropriate to the project gate, including build, representative routes, accessibility, performance, conversion, analytics, SEO, and launch safety where relevant.

Efficiency never means claiming something passed when it was not verified.

## Quality control

Do not equate completion with code generation.

At major milestones verify against the relevant business objective, conversion strategy, creative concept, responsive behavior, accessibility, SEO intent, performance, security, analytics, and actual browser experience.

Use `FOUNDATION/QUALITY-SCORECARD.md` for major final reviews. A high average cannot compensate for a broken conversion, inaccessible interaction, crawlability mistake, exposed secret, or failed production build.

## Output quality

Major strategy, research, audit, and approval outputs should follow `FOUNDATION/OUTPUT-STANDARD.md`.

Lead with the recommendation. Prioritize. Distinguish facts from judgment. Explain meaningful tradeoffs. Make the next action obvious.

## Anti-rush and anti-waste rule

If the site is generic, weakly branded, poorly converted, inaccessible, slow, insecure, difficult to crawl, or technically fragile, continue iterating.

At the same time, do not spend DEEP-mode effort on a bounded task that is already understood.

Excellent work is both high quality and proportionate.
