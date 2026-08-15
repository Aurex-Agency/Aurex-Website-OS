# Aurex Quality Automation

Automation exists to catch regressions early and make repeatable checks deterministic. It does not replace creative review, browser inspection, or human judgment.

## Quality layers

A mature Aurex client repo should use the layers that fit its scope.

### Layer 1: edit-time hygiene

Examples:

- local formatter after edits
- fast lint/type feedback

Purpose: prevent formatting and obvious code issues from accumulating.

### Layer 2: pre-push gate

Recommended checks when configured:

1. typecheck
2. lint
3. test
4. production build

Purpose: prevent obviously broken work from leaving the local branch.

The starter PreToolUse hook blocks Claude-driven `git push` when one of these configured scripts fails.

### Layer 3: CI

GitHub Actions or the client's CI should repeat deterministic repository checks independently of Claude's local session.

Recommended jobs:

- lockfile install
- typecheck
- lint
- unit/integration tests
- production build
- browser smoke tests when available
- automated accessibility tests when available

CI must use the project's actual package manager and lockfile.

### Layer 4: browser automation

Use Playwright or an equivalent browser framework for high-value flows.

Prioritize:

- homepage loads
- navigation works
- critical pages render
- primary form/booking flow
- mobile viewport smoke test
- console errors
- automated accessibility scan

Do not create hundreds of brittle visual selectors when a few role-based business-critical tests provide stronger value.

### Layer 5: visual QA

Automation cannot decide whether a website feels premium, client-specific, visually balanced, or creatively successful.

Use `/aurex-visual-qa` in the actual browser.

### Layer 6: performance diagnostics

Use Lighthouse or equivalent tooling on production-like pages to find issues.

Use Core Web Vitals field data after launch when enough traffic exists.

Do not make a Lighthouse score the sole release criterion.

## Recommended browser testing stack

When browser automation is justified:

- `@playwright/test`
- `@axe-core/playwright` for automated accessibility detection

Automated axe tests can catch common issues but must be paired with manual accessibility review.

## CI philosophy

Aurex CI should fail on deterministic correctness problems such as:

- build failure
- type failure
- lint errors under the project's configured standard
- failing tests
- broken critical smoke tests
- intentionally enforced accessibility violations

Be careful with hard failure thresholds for noisy lab metrics such as Lighthouse performance score. Treat them as diagnostic or regression signals unless the project has proven stable thresholds.

## Visual regression

Screenshot regression can be useful for mature component systems or stable templates.

Do not add visual snapshots so early that every intentional design iteration becomes a test-maintenance chore.

When used, review diffs rather than automatically accepting broad updates.

## Forms and integrations

Automated tests should avoid sending uncontrolled production leads.

Use:

- test/sandbox endpoints when available
- safe test identifiers
- cleanup steps when needed
- explicit production-safe smoke tests only during launch verification

## Hook safety

Claude Code hooks run automatically.

Aurex hook scripts must:

- avoid unexpected package installation
- avoid exposing secrets
- avoid destructive side effects
- return clear failure reasons
- be fast when the relevant condition does not apply

The starter formatter never invokes `npx` to download Prettier. It formats only when local Prettier already exists.

The starter quality gate does nothing unless Claude is attempting `git push`, then runs only scripts that already exist in `package.json`.

## Installation rule

Never copy `starter/.claude/settings.json` over a client's existing settings file.

Use `/aurex-project-setup` to inspect and merge hooks safely.

## Definition of useful automation

Keep a check when it catches a meaningful class of failure more reliably than the maintenance burden it creates.

Remove or redesign automation that is noisy enough to teach developers to ignore it.