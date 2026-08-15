---
name: aurex-project-setup
description: Installs or updates the Aurex engineering and automation layer inside a client website repository, including project instructions, quality commands, hooks, browser testing, and CI without overwriting existing project configuration blindly. Use once near the beginning of a project and when adopting Aurex OS in an existing repo.
disable-model-invocation: true
---

# Aurex Project Setup

This skill adapts Aurex Website OS to the active client repository.

Do not blindly copy a starter over an existing project.

## 1. Inspect first

Determine:

- framework and version
- package manager and lockfile
- package scripts
- TypeScript/lint configuration
- existing `.claude` files
- existing hooks/settings
- existing CI
- existing test framework
- hosting/deployment platform
- environment variable conventions
- current git status

Do not overwrite unrelated existing configuration.

## 2. Confirm technical direction

Use `/aurex-stack` if the stack has not been approved.

For an established project, preserve sound architecture and add only the missing Aurex quality layer.

## 3. Project instructions

Create or update project instructions so the client repo records:

- approved framework/package manager
- real build/lint/type/test commands
- project structure
- CMS/integration notes
- deployment target
- any client-specific technical constraints

Keep shared Aurex methodology in Aurex Website OS rather than duplicating it into every client repo.

## 4. Quality scripts

Ensure the project has clear commands for the checks it actually supports, such as:

- typecheck
- lint
- test
- build
- e2e
- accessibility

Do not invent a script that points to a tool that is not installed.

## 5. Claude hooks

Install Aurex hooks only after inspecting existing `.claude/settings.json`.

Merge instead of replacing.

Recommended hooks:

- PostToolUse formatter for edited source files when a local formatter exists
- PreToolUse quality gate before `git push`

Use the starter hook scripts from `starter/.aurex/hooks/` as a base and adapt paths/package-manager behavior to the project.

Run `/hooks` after installation to verify Claude Code recognizes the configuration.

## 6. Browser QA

If the project does not already have browser testing and scope supports it, recommend Playwright.

For accessibility automation, add `@axe-core/playwright` when appropriate.

Create representative smoke tests for:

- homepage render
- navigation
- primary conversion flow
- accessibility scan of representative pages

Do not claim automated browser coverage before real tests exist.

## 7. CI

If the project uses GitHub, create or update a quality workflow matching the actual package manager and scripts.

Recommended CI layers when available:

1. install with lockfile
2. typecheck
3. lint
4. unit/integration tests
5. production build
6. browser tests where practical
7. automated accessibility scan where practical

Do not download browsers or run heavy e2e jobs when the project does not use them.

## 8. Environment safety

Ensure secret env files are ignored and example env documentation contains only fake values/placeholders.

Never migrate secrets into source control while setting up automation.

## 9. Verify setup

Run every new command or hook path you add.

A configuration file that parses is not enough. Confirm the commands actually work in this repository.

## Output

### Installed
Exact files/configuration added or changed.

### Existing configuration preserved
Important project settings that were intentionally not replaced.

### Quality commands
The actual commands now available.

### Automation
Hooks and CI behavior.

### Verification
What was run successfully.

### Remaining optional upgrades
Tools such as Playwright, axe, Lighthouse CI, or bundle analysis that were not installed and why.