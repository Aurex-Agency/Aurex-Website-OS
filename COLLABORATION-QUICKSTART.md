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

Use for small changes.

Examples:

- change copy
- swap an image
- fix spacing
- fix one mobile issue
- add a simple page from an approved template

Claude should not invoke the full Aurex process.

### STANDARD

Use for most meaningful daily work.

Examples:

- build a new page pattern
- redesign a section
- add a lead form
- implement an approved homepage
- add meaningful motion

This is the normal working mode.

### DEEP

Use for major decisions.

Examples:

- new website
- major redesign
- site architecture
- homepage creative direction
- SEO migration
- major conversion system
- final pre-launch audit

DEEP should not be used for ordinary edits.

## The normal collaboration loop

### Step 1: start with ChatGPT when strategy or review is needed

Example:

```text
New Aurex project for ABC Roofing. Help me determine the website strategy and creative direction.
```

ChatGPT researches and reasons with you.

### Step 2: create a focused build brief

Once you approve the direction, ChatGPT or the human creates `AUREX-BRIEF.md` in the client repo.

The brief contains only what Claude needs to execute the current assignment.

It does not contain the whole ChatGPT conversation.

### Step 3: Claude implements

Open Claude Code in the client repository with Aurex OS attached.

Tell Claude:

```text
Read AUREX-BRIEF.md and AUREX-STATUS.md. Execute the current approved assignment using the smallest appropriate Aurex mode. Do not repeat approved strategy work.
```

Claude builds, runs the relevant checks, and inspects the browser when appropriate.

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

ChatGPT produces a focused `AUREX-REVIEW.md` style response with:

- blockers
- important revisions
- polish
- what should not change
- acceptance criteria

Claude applies only those revisions and verifies them.

Repeat only if necessary.

## What you should NOT do

Do not:

- paste entire ChatGPT conversations into Claude
- paste entire Claude transcripts into ChatGPT
- ask Claude to research the whole market again when ChatGPT already produced approved findings
- invoke every Aurex specialist for every task
- run a full-site audit after every small edit
- keep one Claude session alive forever just to preserve memory

## When to start a fresh Claude session

A fresh session is healthy when:

- the current work unit is complete
- the session has become large and noisy
- you are moving to a different page category or project stage

Before starting fresh, update `AUREX-STATUS.md` and durable project artifacts.

Then the new session can read the current state instead of depending on chat history.

## What you need to remember

Most of the time, remember only this:

```text
ChatGPT
  -> decide/research/review
  -> AUREX-BRIEF.md

Claude
  -> build/test
  -> AUREX-STATUS.md + GitHub branch/PR

ChatGPT
  -> review GitHub
  -> targeted revision

Claude
  -> fix/verify
```

And use:

- QUICK for small work
- STANDARD for normal production
- DEEP for major strategic or high-risk work

## Recommended first real test

Do not begin with a new paying client's full project.

Choose an existing website you know well.

1. Run a STANDARD or DEEP benchmark review.
2. Compare Aurex findings to your own judgment.
3. Choose one meaningful area to improve.
4. Create a focused build brief.
5. Let Claude implement it.
6. Review the GitHub result with ChatGPT.
7. Record any weaknesses in the OS itself.

This creates the feedback loop that will make Aurex Website OS better over time.
