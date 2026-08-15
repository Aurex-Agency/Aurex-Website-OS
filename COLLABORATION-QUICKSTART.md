# Aurex Collaboration Quickstart

This is the simple operating guide for using ChatGPT and Claude Code together without wasting model usage or manually moving large amounts of context.

You do not need to understand every Aurex skill, agent, rule, or foundation document.

## The roles

### ChatGPT

Use ChatGPT for:

- strategy
- research
- creative concepts
- conversion thinking
- sitemap and content reasoning
- reviewing Claude's GitHub work
- deciding what matters next

### Claude Code

Use Claude for:

- local codebase work
- implementation
- browser inspection
- debugging
- responsive refinement
- tests and build work
- technical execution

### GitHub

Use GitHub as the shared state between both systems.

Important decisions and status should live in files, branches, commits, and pull requests instead of only inside chat transcripts.

## The three modes

### QUICK

Use for small changes such as copy, images, spacing, a known mobile issue, or a simple page from an approved pattern.

Default model class: FAST when practically available.

Do not invoke the full Aurex process.

### STANDARD

Use for most meaningful daily work such as new page patterns, sections, forms, approved homepage implementation, motion, and normal engineering.

Default model class: STANDARD, normally Sonnet-class in Claude Code.

This is the normal working mode.

### DEEP

Use for major decisions such as a new website, major redesign, architecture, homepage creative direction, SEO migration, major conversion systems, or final pre-launch review.

DEEP is mixed-model. Research and implementation can remain STANDARD while high-leverage synthesis or high-risk decisions may use PREMIUM, normally Opus-class in Claude Code.

DEEP should not be used for ordinary edits.

## Model routing in plain English

You generally should not have to choose the model manually for every task.

Aurex should ask:

1. How hard is the reasoning?
2. How bad would it be if this decision were wrong?

Then it chooses:

```text
FAST
for simple, low-risk work

STANDARD
for most production work

PREMIUM
for difficult or high-risk judgment
```

Important: DEEP does not mean everything uses PREMIUM.

A new website may use STANDARD for research gathering and coding, then PREMIUM only for creative synthesis or another high-leverage decision.

Use `/aurex-route` when you want Claude to explicitly recommend mode, model class, context, specialists, and escalation criteria before work begins.

## Starting Claude with a model

Claude Code supports setting the primary session model with `--model`.

Examples:

```bash
claude --model sonnet
```

or:

```bash
claude --model opus
```

When using the Aurex launcher, extra Claude arguments pass through, so you can use:

```bash
aurex --model sonnet
```

or, for a deliberate premium reasoning session:

```bash
aurex --model opus
```

Do not hard-code a specific FAST model name into your normal workflow. Availability can depend on the Claude environment/provider. Aurex uses the FAST class and should adapt to what is actually available.

## Escalation instead of waste

Do not start every uncertain task with PREMIUM.

For a difficult technical problem:

```text
STANDARD attempt
  -> gather evidence
  -> second meaningfully different hypothesis if warranted
  -> still blocked?
  -> create compressed escalation brief
  -> PREMIUM solves the specific unresolved question
```

The stronger model should receive the problem, evidence, relevant files, attempts, errors, constraints, and exact question. It should not receive the entire project transcript.

## The normal collaboration loop

### Step 1: start with ChatGPT when strategy or review is needed

Example:

```text
New Aurex project for ABC Roofing. Help me determine the website strategy and creative direction.
```

ChatGPT researches and reasons with you.

### Step 2: create a focused build brief

Once you approve the direction, ChatGPT or the human creates `AUREX-BRIEF.md` in the client repo.

The brief contains only what Claude needs to execute the current assignment. It does not contain the whole ChatGPT conversation.

### Step 3: Claude implements

Open Claude Code in the client repository with Aurex OS attached.

Tell Claude:

```text
Read AUREX-BRIEF.md and AUREX-STATUS.md. Use /aurex-route if routing is not obvious. Execute the approved assignment with the smallest appropriate mode and model class. Do not repeat approved strategy work.
```

Claude builds, runs relevant checks, and inspects the browser when appropriate.

### Step 4: Claude updates status and pushes

Claude updates `AUREX-STATUS.md` and pushes the focused branch or pull request.

The status should say what changed, what was verified, what remains uncertain, and what review is requested.

### Step 5: return to ChatGPT

Tell ChatGPT something like:

```text
@GitHub Review the homepage-v1 PR. Read AUREX-STATUS.md and the approved creative direction. Review only creative fidelity, conversion clarity, and mobile UX.
```

ChatGPT can inspect the GitHub implementation directly.

### Step 6: targeted revision

ChatGPT produces a focused `AUREX-REVIEW.md` style response with blockers, important revisions, polish, what should not change, and acceptance criteria.

Claude applies only those revisions and verifies them.

Repeat only if necessary.

## What you should NOT do

Do not:

- paste entire ChatGPT conversations into Claude
- paste entire Claude transcripts into ChatGPT
- ask Claude to research the whole market again when approved findings already exist
- invoke every Aurex specialist for every task
- use PREMIUM merely because it is available
- run a full-site audit after every small edit
- keep one Claude session alive forever just to preserve memory

## When to start a fresh Claude session

A fresh session is healthy when the current work unit is complete, the session has become large/noisy, or you are moving to a different page category or project stage.

Before starting fresh, update `AUREX-STATUS.md` and durable project artifacts.

Then the new session reads current state instead of depending on chat history.

## What you need to remember

Most of the time:

```text
ChatGPT
  -> decide/research/review
  -> AUREX-BRIEF.md

Claude
  -> route task
  -> build/test
  -> AUREX-STATUS.md + GitHub branch/PR

ChatGPT
  -> review GitHub
  -> targeted revision

Claude
  -> fix/verify
```

And use:

- QUICK + FAST for small low-risk work
- STANDARD + STANDARD model for normal production
- DEEP + mixed models for major/high-risk work
- PREMIUM only where premium reasoning adds real value

## Recommended first real test

Choose an existing website you know well rather than a brand-new paying client's full build.

1. Run a STANDARD or DEEP benchmark review.
2. Compare Aurex findings to your judgment.
3. Choose one meaningful area to improve.
4. Create a focused build brief.
5. Route the implementation with `/aurex-route`.
6. Let Claude implement it.
7. Review the GitHub result with ChatGPT.
8. Record any routing, quality, or workflow weaknesses in the OS.

This feedback loop improves quality and helps Aurex learn where stronger models are actually worth their cost.
