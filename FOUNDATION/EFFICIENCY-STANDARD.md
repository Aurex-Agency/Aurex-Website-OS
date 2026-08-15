# Aurex Efficiency Standard

Aurex Website OS should spend reasoning and tool usage in proportion to the value and risk of the task.

The goal is not to minimize quality. The goal is to avoid spending premium effort on routine work while preserving deep thinking for decisions that materially affect business results, creative direction, search visibility, conversion, technical risk, or launch quality.

## Core principle

Use the smallest operating mode that can reliably produce an excellent result.

More agents, more research, and more context are not automatically better.

## Operating modes

### QUICK

Use QUICK for small, bounded, low-risk work inside an already approved strategy and design system.

Typical examples:

- change copy in one known section
- replace an image
- fix a responsive bug
- update a CTA label or destination
- adjust spacing or styling within the approved design language
- fix a small accessibility issue
- repair a known technical bug
- add a simple page using an already approved page pattern

Default behavior:

- one primary Claude session
- no broad research
- no specialist agent unless the task genuinely requires one
- read only directly relevant files
- make the change
- run targeted verification
- report what changed and anything still unverified

QUICK should not trigger a full Aurex discovery, strategy, SEO, creative, or QA process.

### STANDARD

Use STANDARD for meaningful work that affects a page, flow, page category, or feature but does not require rethinking the whole website.

Typical examples:

- build a new service-page pattern
- redesign one major section
- create a new lead flow
- add a major new page
- implement an approved homepage concept
- add meaningful motion
- improve a cluster of related pages
- perform a targeted SEO, conversion, accessibility, or performance audit

Default behavior:

- one primary Claude session
- load only relevant Aurex skills
- use at most one or two specialist agents when independent deep work materially improves the result
- reuse approved project artifacts instead of repeating discovery
- perform browser verification for user-facing changes
- update durable project artifacts when a decision should survive the session

STANDARD is the default mode for most day-to-day Aurex production work.

### DEEP

Use DEEP only when the business value, strategic uncertainty, creative stakes, or technical risk justify broad analysis.

Typical examples:

- a new client website
- major redesign or repositioning
- homepage creative direction before approval
- site architecture or SEO migration
- major conversion-system redesign
- complex technical architecture decision
- final pre-launch review
- high-stakes performance, accessibility, analytics, or migration work

DEEP may use multiple specialist agents and broader research, but each specialist must have a defined question and deliverable.

Do not invoke specialists merely because they exist.

## Mode selection test

Choose the mode by asking:

1. Does this change alter the approved strategy or visual language?
2. Is the decision expensive to reverse?
3. Could it materially affect revenue, conversion, rankings, accessibility, security, analytics, or launch safety?
4. Is there meaningful uncertainty that research or an independent specialist could resolve?
5. Is this a new pattern that will be reused widely?

If most answers are no, prefer QUICK.

If one or two are meaningfully yes, prefer STANDARD.

If several are yes or the task is a major project gate, use DEEP.

## Specialist cost discipline

Before invoking a specialist agent, define:

- the exact question
- why the primary session should not answer it directly
- the expected artifact or decision
- what information the agent actually needs

Do not ask multiple specialists to independently analyze the entire project unless their disagreement is valuable.

Prefer one focused specialist over an agent team.

## Context discipline

Do not repeatedly load the entire repository.

Start with durable project artifacts and only open source files relevant to the current task.

Recommended project memory includes:

- `PROJECT-BRIEF.md`
- `WEBSITE-STRATEGY.md`
- `SITE-ARCHITECTURE.md`
- `CREATIVE-DIRECTION.md`
- `DESIGN-SYSTEM.md`
- `ENGINEERING-PLAN.md`
- `AUREX-STATUS.md`

These files exist to prevent every new session from rediscovering settled decisions.

## Session discipline

When the current task is complete, do not keep an enormous conversation alive solely because more work remains elsewhere in the project.

Before resetting or compacting a session:

1. write any durable decision into the appropriate project artifact
2. update `AUREX-STATUS.md`
3. record unresolved blockers
4. record the recommended next action

A fresh session should be able to understand the current state without reading the previous chat transcript.

## Research discipline

Do not research broadly when the decision is already settled or can be answered from project evidence.

Research is justified when:

- the information is current or unstable
- a material SEO/CRO/technical claim needs evidence
- competitor or market context affects strategy
- a business fact is unknown
- the decision has meaningful cost or risk

Separate factual research from creative judgment.

## Verification discipline

Efficiency does not mean skipping verification.

Match verification to the task.

QUICK examples:

- targeted typecheck or lint
- inspect the changed route
- test the changed interaction

STANDARD examples:

- browser inspection at representative widths
- relevant tests
- conversion-path verification when touched

DEEP examples:

- full build
- representative route smoke tests
- accessibility review
- performance review
- conversion, analytics, SEO, and launch checks as relevant

## Escalation rule

A task may start QUICK or STANDARD and escalate when new evidence reveals greater risk or ambiguity.

State the reason for escalation instead of silently expanding scope.

## Anti-token-waste rules

Do not:

- rerun discovery because a new session started
- ask every specialist to read the entire repo
- regenerate approved strategy documents unnecessarily
- perform full-site audits for one bounded UI change
- repeatedly summarize information already stored in durable project artifacts
- invoke DEEP mode because the project feels important while the current task is small
- use agent teams when a focused subagent or primary session can solve the problem
- generate lengthy internal reports when a concise decision artifact is sufficient

## Definition of efficient excellence

Aurex is operating efficiently when:

- the right amount of reasoning is applied to the decision
- approved context is reused rather than recreated
- specialists are invoked deliberately
- durable files preserve state between sessions
- verification is proportional to risk
- the human creative lead receives concise, high-level decisions rather than process noise
- quality remains high while unnecessary model usage is reduced
