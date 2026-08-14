# Using Aurex Website OS on Client Projects

Aurex Website OS is intended to be a shared operating brain that can support many separate client repositories.

## Recommended local layout

Keep the OS cloned somewhere stable on your machine, for example:

```text
~/Aurex/
  Aurex-Website-OS/
  clients/
    client-one/
    client-two/
```

## Start Claude Code with the OS attached

From inside a client repository, add the OS directory when starting Claude Code.

Example:

```bash
CLAUDE_CODE_ADDITIONAL_DIRECTORIES_CLAUDE_MD=1 claude --add-dir ../../Aurex-Website-OS
```

Adjust the path to wherever the OS lives on your machine.

This setup is intended to make the OS skills, agents, and shared Claude instructions available while the client repository remains the primary working directory.

## Start a project

Use the master workflow explicitly:

```text
/aurex-website
```

Then provide the client context or ask the system to determine the current project stage from the repository.

For a new project, the first durable artifact should normally be a project brief based on `templates/PROJECT-BRIEF.md`.

## Specialist skills

The OS includes:

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

The master `/aurex-website` workflow should coordinate these instead of invoking every skill unnecessarily.

## Specialist agents

The OS includes project specialists for:

- research direction
- creative direction
- conversion strategy
- SEO strategy
- content strategy
- motion direction
- frontend architecture
- independent QA review

Use specialist agents when isolated deep work or an independent review would improve the main session. Keep major cross-disciplinary decisions in the main conversation so the full project context remains available.

## Working artifacts in a client repository

Recommended durable project files include:

```text
PROJECT-BRIEF.md
DISCOVERY.md
WEBSITE-STRATEGY.md
SITE-ARCHITECTURE.md
CREATIVE-DIRECTION.md
DESIGN-SYSTEM.md
SEO-PLAN.md
CONVERSION-PLAN.md
QA-REPORT.md
LAUNCH-CHECKLIST.md
```

Not every project needs every file. Create artifacts when they preserve decisions or context that future sessions need.

## Human collaboration

The default Aurex mode is approximately 50/50 collaboration.

Expect human review at high-leverage gates such as:

1. discovery and strategic understanding
2. site architecture
3. creative direction
4. homepage structure and hero
5. homepage approval
6. new page-category patterns
7. final creative review
8. launch

Do not require approval for routine implementation choices inside an approved direction.

## High-quality output rule

For major strategy, research, audits, or decisions, use `FOUNDATION/OUTPUT-STANDARD.md`.

The system should lead with the recommendation, prioritize findings, distinguish evidence from judgment, explain tradeoffs, and make the next action obvious.

## Quality control

Before final approval, use:

- `FOUNDATION/QUALITY-SCORECARD.md`
- `/aurex-visual-qa`
- the independent QA reviewer agent

A production build is not equivalent to an approved website.

## OS improvement loop

When a client project reveals a reusable lesson, propose a specific change back to Aurex Website OS.

Examples:

- a recurring design anti-pattern
- a form failure
- a better research source hierarchy
- a useful motion pattern
- a responsive edge case
- a new SEO migration rule
- a stronger QA check

The goal is for real client experience to improve the system over time.
