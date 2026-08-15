# Aurex ChatGPT and Claude Collaboration Protocol

Aurex Website OS is designed so ChatGPT and Claude Code can collaborate without both systems continuously ingesting the entire project.

The collaboration model uses GitHub and durable project artifacts as shared state.

## Role separation

### Human creative lead

Owns:

- final taste and brand judgment
- client knowledge not available elsewhere
- major strategic approvals
- major creative approvals
- scope and business priorities
- final launch authority

### ChatGPT

Default role: strategy, research, creative direction, conversion reasoning, review, prioritization, and project-level synthesis.

ChatGPT is especially useful for:

- business and competitor research
- website strategy
- sitemap reasoning
- creative concept development
- conversion and messaging strategy
- reviewing GitHub branches and pull requests
- identifying where implementation drifted from approved strategy
- preparing concise implementation briefs for Claude
- prioritizing revision requests

ChatGPT should avoid duplicating local implementation work that Claude Code can perform directly unless a second engineering opinion is useful.

### Claude Code

Default role: implementation, local repository understanding, coding, browser interaction, debugging, testing, responsive refinement, and technical execution.

Claude is especially useful for:

- understanding the active local codebase
- implementing approved designs and flows
- editing components and styles
- running local tools and tests
- browser-based implementation QA
- debugging build/runtime issues
- carrying out focused engineering audits
- applying concise review feedback

### GitHub

GitHub is the shared source of truth between ChatGPT and Claude.

Use it to preserve:

- code
- branches and pull requests
- approved project artifacts
- build briefs
- current status
- review findings
- implementation history

Do not use chat transcripts as the only source of important decisions.

## The collaboration loop

### 1. Strategy or review begins with ChatGPT when appropriate

The human provides the business context, goal, or review request.

ChatGPT produces a concise decision or build brief.

### 2. The approved brief becomes durable state

Store important instructions in the client repository using `AUREX-BRIEF.md` or the appropriate strategy artifact.

The brief should contain decisions, not the entire discussion that produced them.

### 3. Claude implements locally

Claude reads the brief plus only the project files required to execute it.

Claude should not repeat strategic research unless the brief contains a material uncertainty that implementation exposes.

### 4. Claude updates status

After a meaningful work unit, Claude updates `AUREX-STATUS.md` with:

- what was completed
- branch or relevant commit/PR
- verification performed
- decisions made
- unresolved issues
- exact next recommended action

### 5. GitHub becomes the review handoff

Claude commits/pushes the work.

ChatGPT reviews the relevant branch, PR, or changed files from GitHub rather than requiring the user to paste the codebase.

### 6. ChatGPT returns a prioritized review

Review should classify findings by impact and distinguish:

- blocker
- important revision
- polish
- optional experiment

ChatGPT should provide exact intent and acceptance criteria, not dictate unnecessary implementation detail when Claude can choose the best technical method.

### 7. Claude executes the revision brief

Claude reads only the review and affected project context, fixes the work, verifies it, and updates status.

Repeat only as needed.

## Handoff files

### `AUREX-BRIEF.md`

Use for a focused assignment from strategy/review into implementation.

It should answer:

- what are we trying to accomplish?
- why does it matter?
- what has already been approved?
- what must not change?
- what are the acceptance criteria?
- what requires human approval before proceeding?

### `AUREX-STATUS.md`

Use as the concise current-state checkpoint.

It should allow a fresh ChatGPT or Claude session to answer:

- where are we?
- what is approved?
- what changed most recently?
- what is broken or uncertain?
- what should happen next?

### Existing strategy artifacts

Do not duplicate information that already belongs in:

- `WEBSITE-STRATEGY.md`
- `CREATIVE-DIRECTION.md`
- `DESIGN-SYSTEM.md`
- `ENGINEERING-PLAN.md`
- `QA-REPORT.md`

`AUREX-BRIEF.md` should reference these artifacts when useful instead of copying them wholesale.

## GitHub branch and PR workflow

For meaningful work:

1. create or use a focused branch
2. Claude implements the approved brief
3. Claude verifies locally
4. Claude pushes the branch
5. ChatGPT reviews the branch or PR through GitHub
6. revision feedback is captured in a concise review or updated brief
7. Claude applies revisions
8. final review occurs only when useful

Avoid creating a new branch for trivial edits when the project's existing workflow does not require one.

## Information compression rules

When moving work from ChatGPT to Claude:

Do not paste the whole strategy conversation.

Compress it into:

- objective
- approved direction
- constraints
- required content
- required interactions
- acceptance criteria
- open decisions

When moving work from Claude to ChatGPT:

Do not paste the whole Claude transcript.

Provide:

- branch/PR
- `AUREX-STATUS.md`
- the exact question or review goal

ChatGPT can inspect GitHub for the implementation details.

## Review scope control

A review request should specify the scope.

Examples:

- review only the homepage hero against the approved creative direction
- review this PR for conversion and mobile UX
- audit the service-page template for SEO, visual repetition, and CTA flow
- perform final pre-launch review

Do not trigger a full website review after every implementation commit.

## Resolving disagreement

If ChatGPT and Claude disagree:

1. identify whether the disagreement is factual, technical, strategic, or aesthetic
2. factual or technical disagreements should be resolved with current evidence, tests, standards, or code behavior
3. strategic disagreements should compare expected business impact and tradeoffs
4. aesthetic disagreements should return to the approved creative direction and human creative lead

The human creative lead owns final subjective judgment.

## When ChatGPT should do research instead of Claude

Prefer ChatGPT for broad external research when the result can be compressed before implementation, such as:

- competitor analysis
- market context
- current best-practice research
- strategic SEO research
- conversion research
- reference-site analysis

Prefer Claude for research that depends heavily on the local repository or running application.

This separation reduces repeated context and keeps Claude focused on implementation.

## When Claude should use a subagent

A Claude subagent is justified when:

- the task needs deep isolated repository analysis
- a specialist needs to read many files but only return a concise conclusion
- an independent technical review is valuable
- the task can be clearly bounded

Do not invoke a subagent for routine implementation that the primary session already understands.

## Agent team policy

Do not use multi-agent teams by default.

Use them only when:

- multiple independent workstreams genuinely need to proceed in parallel
- the additional usage cost is justified by project value or urgency
- the workstreams have clear ownership and deliverables

A new client website does not automatically require an agent team.

## Human experience goal

The human should not feel like a messenger copying long prompts between two AIs.

The intended workflow is:

```text
Human
  -> ChatGPT strategy/review
  -> concise durable brief in GitHub
  -> Claude implementation
  -> concise status + code in GitHub
  -> ChatGPT review
  -> targeted revision brief
  -> Claude revision
```

The handoff itself should be short because the shared details live in the repository.
