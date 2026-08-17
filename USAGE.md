# Using Aurex Website OS on Client Projects

Aurex Website OS is a shared operating brain for separate client repositories. It should increase quality without forcing every task through the full agency process.

If you are new to the system, read `COLLABORATION-QUICKSTART.md` first.

## The simple mental model

```text
ChatGPT
strategy + research + review
        ↓
GitHub durable brief
        ↓
Claude Code
implementation + browser + tests
        ↓
GitHub status + branch/PR
        ↓
ChatGPT
focused review
        ↓
Claude Code
revision + verification
```

Do not make both systems redo the same work.

## Operating modes

Use `/aurex-mode` when the correct depth is unclear.

### QUICK

Small, bounded, low-risk changes inside an approved strategy.

Default: no specialists, no broad research, targeted verification.

### STANDARD

Meaningful daily production work such as a page, section, feature, lead flow, or approved homepage implementation.

Default: primary session, relevant skills, zero to two focused specialists when useful, browser verification.

### DEEP

New websites, major redesigns, architecture/migration decisions, major conversion systems, or high-stakes final audits.

DEEP is not the default.

See `FOUNDATION/EFFICIENCY-STANDARD.md`.

## Recommended local layout

```text
~/Aurex/
  Aurex-Website-OS/
  clients/
    client-one/
    client-two/
```

## Recommended one-command launcher

The repo includes `bin/aurex`.

On macOS/Linux:

```bash
chmod +x ~/Aurex/Aurex-Website-OS/bin/aurex
mkdir -p ~/.local/bin
ln -s ~/Aurex/Aurex-Website-OS/bin/aurex ~/.local/bin/aurex
```

Make sure `~/.local/bin` is on your PATH.

From a client repository:

```bash
aurex
```

Extra Claude CLI arguments pass through:

```bash
aurex --chrome
```

## Manual launch

From inside a client repository:

```bash
CLAUDE_CODE_ADDITIONAL_DIRECTORIES_CLAUDE_MD=1 claude --add-dir ../../Aurex-Website-OS
```

Adjust the path for your machine.

## First-time setup in a client repo

Run:

```text
/aurex-project-setup
```

The setup skill inspects the real repository before proposing changes. It may configure or recommend:

- project-specific Claude instructions
- actual typecheck/lint/test/build scripts
- Aurex Claude hooks
- Playwright browser testing
- axe accessibility automation
- GitHub Actions quality checks
- environment safety

It must merge existing configuration instead of overwriting it blindly.

## Start or continue work

Use:

```text
/aurex-website
```

The orchestrator should first determine the operating mode and current project state.

For a bounded task you may invoke the relevant skill directly instead of running the full website process.

## Collaboration files

### `AUREX-BRIEF.md`

Focused assignment handed into implementation.

Use `templates/AUREX-BRIEF.md`.

It stores:

- objective
- approved context
- exact scope
- creative and conversion intent
- constraints
- acceptance criteria
- verification requirements

It should not contain entire strategy conversations.

### `AUREX-STATUS.md`

Concise current project checkpoint.

Use `templates/AUREX-STATUS.md`.

Update it after meaningful work and before clearing a long session.

It stores:

- current branch/PR
- approved state
- recent work
- verification
- known issues
- requested review
- next action

### `AUREX-REVIEW.md`

Focused review format for ChatGPT, the human creative lead, or another reviewer.

Use `templates/AUREX-REVIEW.md`.

It separates:

- blockers
- important revisions
- polish
- optional experiments
- elements that must be preserved

## Recommended ChatGPT to Claude workflow

### Strategy or direction

Use ChatGPT for broad research, strategy, creative direction, conversion reasoning, and prioritization when those tasks benefit from external research or a second strategic brain.

After approval, compress the decision into `AUREX-BRIEF.md`.

### Implementation

Claude Code reads the brief, status, and only the project files relevant to the current assignment.

It implements, verifies, updates `AUREX-STATUS.md`, and pushes a focused branch or PR.

### Review

Ask ChatGPT to inspect the GitHub branch or PR and specify the review scope.

Example:

```text
@GitHub Review the homepage-v1 PR. Read AUREX-STATUS.md and CREATIVE-DIRECTION.md. Review only creative fidelity, conversion clarity, and mobile UX.
```

Do not ask for a full-site audit after every small change.

### Revision

Translate review findings into a focused revision brief. Claude fixes only what is required, verifies it, and updates status.

See `FOUNDATION/COLLABORATION-PROTOCOL.md`.

## Core project memory

Use durable files so fresh sessions do not need old transcripts.

Common artifacts:

```text
PROJECT-BRIEF.md
DISCOVERY.md
WEBSITE-STRATEGY.md
SITE-ARCHITECTURE.md
CREATIVE-DIRECTION.md
DESIGN-SYSTEM.md
ENGINEERING-PLAN.md
AUREX-BRIEF.md
AUREX-STATUS.md
SEO-PLAN.md
CONVERSION-PLAN.md
QA-REPORT.md
LAUNCH-CHECKLIST.md
```

Not every project needs every file.

## Skill map

### Efficiency and coordination

- `/aurex-mode`
- `/aurex-handoff`
- `/aurex-website`

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

### Engineering and production

- `/aurex-stack`
- `/aurex-project-setup`
- `/aurex-engineering`
- `/aurex-form-qa`
- `/aurex-accessibility`
- `/aurex-performance`
- `/aurex-technical-qa`
- `/aurex-launch`

The orchestrator should call only the skills needed for the current work.

## Specialist policy

Specialists exist for research, creative direction, conversion, SEO, content, motion, frontend architecture, performance, accessibility, independent QA, and launch engineering.

Before invoking one, define the exact question.

Prefer one focused specialist over overlapping specialists.

Do not use agent teams by default.

## Claude hooks

Starter hook files live under:

```text
starter/.claude/settings.json
starter/.aurex/hooks/
```

### Format-on-edit

Runs local Prettier only when it already exists in the project. It never uses `npx` to download a formatter unexpectedly.

### Pre-push quality gate

When Claude attempts `git push`, the hook runs configured scripts when they exist:

1. typecheck
2. lint
3. test
4. build

A failure denies the push and returns the reason to Claude.

Use `/aurex-project-setup` to merge hooks safely with existing client configuration.

## Browser testing starter

Reusable Playwright examples live in:

```text
starter/quality/playwright/
```

They include desktop/mobile route smoke testing, console/page-error detection, and axe accessibility scanning.

Representative routes can be configured with:

```bash
AUREX_TEST_ROUTES="/,/services,/about,/contact"
```

Adapt the starter to the real client repo before relying on it.

## CI starter

The npm GitHub Actions starter lives at:

```text
starter/.github/workflows/aurex-quality.yml
```

It is intentionally not universal. `/aurex-project-setup` should adapt package manager, Node version, install command, scripts, browser setup, and environment requirements.

## Human collaboration

The default relationship is roughly 50/50.

Human review belongs at high-leverage gates such as:

- discovery/strategy
- site architecture
- creative direction
- homepage structure and hero
- homepage approval
- strategically new page-category patterns
- dedicated mobile art-direction pass
- mobile visual approval
- final creative review
- launch

Routine implementation inside an approved direction should not require constant approval.

## Desktop to mobile approval gate

Desktop visual approval and mobile visual approval are separate gates. Technically responsive does not mean creatively approved on mobile.

The canonical sequence for any meaningfully visual page or section:

```text
Desktop visual implementation/review
        ↓
Desktop visual approval
        ↓
Dedicated mobile art-direction pass
        ↓
Human + ChatGPT mobile visual approval
        ↓
Launch readiness
```

A dedicated mobile art-direction pass reviews mobile hierarchy, layout, crops, motion, and interaction on its own terms rather than assuming desktop intent survived the breakpoint. Do not treat a passing responsive breakpoint as mobile creative sign-off, and do not begin launch-readiness work before mobile visual approval is recorded in `AUREX-STATUS.md`.

## Session reset discipline

Do not keep a huge Claude conversation alive only to preserve memory.

Before starting fresh:

1. update durable approved artifacts
2. update `AUREX-STATUS.md`
3. record blockers and unverified areas
4. state the next action

Then a fresh session can continue from project state instead of chat history.

## Quality rule

Efficiency does not mean skipping quality.

A production build is not equivalent to an approved website.

Before launch, have appropriate evidence for real browser behavior, responsive quality, conversion delivery, accessibility, crawlability, performance, analytics, security, and visual quality.

If something cannot be verified, label it unverified.

## OS improvement loop

When a client project reveals a reusable lesson, propose a specific improvement back to Aurex Website OS.

The system should become smarter from real projects while each client remains visually distinct.
