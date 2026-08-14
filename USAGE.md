# Using Aurex Website OS on Client Projects

Aurex Website OS is a shared operating brain that supports separate client repositories while preserving client-specific code, content, creative direction, and project memory.

## Recommended local layout

Keep the OS cloned somewhere stable:

```text
~/Aurex/
  Aurex-Website-OS/
  clients/
    client-one/
    client-two/
```

## Recommended one-command launcher

The repo includes:

```text
bin/aurex
```

On macOS/Linux, make it executable once:

```bash
chmod +x ~/Aurex/Aurex-Website-OS/bin/aurex
```

Then either call it directly or add a symlink somewhere on your PATH, for example:

```bash
mkdir -p ~/.local/bin
ln -s ~/Aurex/Aurex-Website-OS/bin/aurex ~/.local/bin/aurex
```

Make sure `~/.local/bin` is on your PATH.

After that, from any client repository you can start Claude Code with Aurex OS attached using:

```bash
aurex
```

The launcher resolves the real OS directory even when invoked through a symlink and enables additional-directory Claude memory automatically.

Any extra Claude CLI arguments are passed through:

```bash
aurex --chrome
```

## Start Claude Code manually

If you do not use the launcher, from inside a client repository run:

```bash
CLAUDE_CODE_ADDITIONAL_DIRECTORIES_CLAUDE_MD=1 claude --add-dir ../../Aurex-Website-OS
```

Adjust the path to the OS on your machine.

The environment variable tells Claude Code to load shared `CLAUDE.md` and `.claude/rules/` from the additional directory. The added directory also makes the OS skills and agents available.

## First-time setup inside a client repo

After attaching the OS, run:

```text
/aurex-project-setup
```

This should inspect the active client repository before making changes.

It may configure or recommend:

- project-specific Claude instructions
- actual typecheck/lint/test/build scripts
- Aurex Claude hooks
- Playwright browser testing
- axe accessibility automation
- GitHub Actions quality checks
- environment safety

It must merge existing configuration instead of overwriting it blindly.

## Start or continue the project

Use:

```text
/aurex-website
```

For a new project, provide the client context and build the project brief.

For an existing project, ask the orchestrator to determine the current stage from existing project artifacts and code.

Do not redo approved work without a reason.

## Core project artifacts

Recommended durable project memory:

```text
PROJECT-BRIEF.md
DISCOVERY.md
WEBSITE-STRATEGY.md
SITE-ARCHITECTURE.md
CREATIVE-DIRECTION.md
DESIGN-SYSTEM.md
ENGINEERING-PLAN.md
SEO-PLAN.md
CONVERSION-PLAN.md
QA-REPORT.md
LAUNCH-CHECKLIST.md
```

Not every project requires every file. Create documents when they preserve decisions that future sessions need.

## Skill map

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

The master `/aurex-website` workflow should coordinate these instead of invoking all of them unnecessarily.

## Specialist agents

The OS includes specialists for:

- research
- creative direction
- conversion
- SEO
- content
- motion
- frontend architecture
- performance
- accessibility
- independent QA
- launch engineering

Use agents when isolated deep work or an independent review improves the result. Keep cross-disciplinary synthesis in the main conversation.

## Claude hooks

Aurex includes starter hook files under:

```text
starter/.claude/settings.json
starter/.aurex/hooks/
```

### Format-on-edit

After Claude edits supported source files, the hook runs local Prettier only when Prettier already exists in the project's `node_modules`.

It never calls `npx` to download a formatter unexpectedly.

### Pre-push quality gate

When Claude attempts `git push`, the hook inspects the client repo and runs configured scripts in this order when they exist:

1. typecheck
2. lint
3. test
4. build

If a check fails, the hook denies the push and returns the failure to Claude.

Do not copy the starter settings over existing `.claude/settings.json`. Use `/aurex-project-setup` to merge it safely.

After hook setup, use Claude Code `/hooks` to confirm the hooks are loaded.

## Browser testing starter

Reusable Playwright examples live in:

```text
starter/quality/playwright/
```

They include:

- representative route smoke testing
- desktop and mobile Chromium projects
- console/page-error detection
- axe accessibility scanning

Set representative routes with:

```bash
AUREX_TEST_ROUTES="/,/services,/about,/contact"
```

Configure `PLAYWRIGHT_BASE_URL` for an already-running site or `AUREX_START_COMMAND` when the adapted Playwright config should start the app.

The starter must be copied and adapted into the client repo before use.

## CI starter

The npm GitHub Actions starter lives at:

```text
starter/.github/workflows/aurex-quality.yml
```

It is intentionally not universal.

`/aurex-project-setup` should adapt:

- package manager
- Node version
- install command
- actual scripts
- browser-test setup
- environment requirements

Never commit a CI workflow that has not been run or reviewed against the real client repository.

## Human collaboration

The default Aurex mode is approximately 50/50 collaboration.

Expect human review at high-leverage gates such as:

1. discovery and strategy
2. site architecture
3. creative direction
4. homepage structure and hero
5. homepage approval
6. strategically new page-category patterns
7. final creative review
8. launch

Do not require approval for routine engineering choices inside an approved strategy unless the decision is expensive to reverse or changes the project materially.

## Build workflow after creative approval

A typical engineering sequence is:

```text
/aurex-stack
/aurex-project-setup
create ENGINEERING-PLAN.md
/aurex-engineering
browser inspection
/aurex-responsive
/aurex-motion
/aurex-form-qa
/aurex-accessibility
/aurex-performance
/aurex-technical-qa
/aurex-visual-qa
/aurex-launch
```

The orchestrator decides which steps are needed and when.

## Quality rule

A production build is not equivalent to an approved website.

Before launch, Aurex should have evidence for:

- real browser behavior
- responsive quality
- primary conversion delivery
- accessibility
- crawlability and SEO controls
- performance
- analytics
- security baseline
- visual quality

If something cannot be verified, record it as unverified instead of assuming it works.

## OS improvement loop

When a client project reveals a reusable lesson, propose a specific change back to Aurex Website OS.

Useful lessons include:

- repeated design anti-patterns
- form failures
- better source hierarchies
- animation implementation problems
- responsive edge cases
- SEO migration mistakes
- performance regressions
- accessibility failures
- stronger automation checks

The system should become smarter from real projects without converging on one visual style.
