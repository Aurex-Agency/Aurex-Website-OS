# Aurex Adaptive Model Routing Standard

Aurex Website OS should use the least expensive model class that can reliably complete the task to Aurex quality, then escalate only when reasoning difficulty, uncertainty, or consequence of error justifies it.

The goal is not to maximize use of the strongest model. The goal is to reserve premium reasoning for the decisions where it creates real value.

## Core rule

Route by two variables:

1. Reasoning difficulty
2. Consequence of being wrong

Task size alone is not enough.

A small DNS change may be technically simple but high risk. A long copy replacement may be low risk even if it touches many files.

## Model classes

Use model classes rather than hard-coding version numbers into Aurex doctrine.

### FAST

Use the smallest suitable fast model available in the user's Claude environment for low-complexity, low-risk work.

Typical work:

- copy replacement
- image replacement
- simple spacing/style changes
- routine file transforms
- straightforward status updates
- simple repetitive implementation from an approved pattern
- known accessibility fixes
- basic code cleanup where behavior is well understood

FAST should not make high-leverage creative, architectural, migration, security, launch, or conversion decisions.

### STANDARD

Use the normal production model, generally Sonnet-class in Claude Code, for most implementation and technical work.

Typical work:

- page implementation
- responsive engineering
- component development
- forms
- routine debugging
- SEO implementation
- accessibility remediation
- performance implementation
- motion implementation
- browser QA
- testing
- most STANDARD-mode Aurex work

STANDARD is the default model class for meaningful production work.

### PREMIUM

Use the strongest reasoning model available, generally Opus-class in Claude Code, only when the value or risk warrants it.

Typical work:

- creative direction synthesis
- difficult positioning decisions
- ambiguous high-impact architecture
- major conversion strategy
- complex migration planning
- difficult debugging after focused lower-cost attempts fail
- high-risk launch or DNS reasoning
- final high-level creative review
- decisions with multiple strategically valid options and material consequences

PREMIUM should be an executive reasoning resource, not the default implementation worker.

## Relationship to operating modes

Operating mode and model class are related but not identical.

### QUICK

Default model class: FAST when the environment supports it, otherwise STANDARD.

Escalate to STANDARD when the task becomes ambiguous, behavior is not understood, or the change affects meaningful user/business outcomes.

Do not use PREMIUM for QUICK work unless risk is unexpectedly high.

### STANDARD

Default model class: STANDARD.

Use FAST for clearly mechanical subtasks when practical.

Escalate individual questions to PREMIUM only when there is a defined reason.

### DEEP

DEEP does not mean PREMIUM everywhere.

A DEEP project should mix model classes.

Example:

- evidence gathering: STANDARD
- competitor extraction: STANDARD
- creative synthesis: PREMIUM
- page implementation: STANDARD
- repetitive approved page production: FAST or STANDARD
- final creative judgment: PREMIUM
- technical verification: STANDARD

## Routing matrix

### Low difficulty + low risk

Route: FAST

Examples:

- change CTA text
- replace an image
- adjust known spacing
- create repeated approved pages from an established pattern

### Medium difficulty + low/medium risk

Route: STANDARD

Examples:

- build a service page
- fix responsive behavior
- add an ordinary lead form
- implement approved motion

### High difficulty + medium risk

Route: STANDARD first, with focused escalation to PREMIUM if needed.

Examples:

- obscure hydration issue
- difficult animation bug
- performance regression with multiple possible causes

### Medium difficulty + high risk

Route: PREMIUM or specialist review even if the task appears technically simple.

Examples:

- production DNS change
- redirect migration
- canonical/indexation change on a large existing site
- analytics change affecting revenue attribution

### High difficulty + high risk

Route: PREMIUM with human approval at the appropriate gate.

Examples:

- site migration architecture
- major conversion-system redesign
- creative direction for a flagship project
- ambiguous production incident

## Start cheap, escalate intelligently

Do not start with PREMIUM solely because the problem might become difficult.

Use this escalation ladder:

1. Attempt with the assigned lower-cost model when appropriate.
2. Gather concrete evidence.
3. If blocked after focused attempts, stop repeating the same approach.
4. Create a compressed escalation brief.
5. Escalate the unresolved question, not the whole project context.

## Escalation brief

Before escalating, summarize:

- exact problem
- desired outcome
- relevant evidence
- relevant files/components
- what has already been tried
- observed results/errors
- constraints
- specific question requiring stronger reasoning

Do not send a complete chat transcript to the stronger model.

## Retry limit

For ambiguous technical problems, two focused attempts with substantially different hypotheses are normally enough before reassessing model class or strategy.

Do not burn tokens on repeated near-identical attempts.

## Specialist routing

Specialist agents should also use proportionate model classes.

Suggested default classes:

- Research Director: STANDARD
- Creative Director: PREMIUM
- Conversion Strategist: STANDARD normally, PREMIUM for high-stakes strategy
- SEO Strategist: STANDARD
- Content Strategist: STANDARD
- Motion Director: STANDARD
- Frontend Architect: STANDARD
- Performance Engineer: STANDARD
- Accessibility Reviewer: STANDARD
- QA Reviewer: STANDARD
- Launch Engineer: STANDARD normally, PREMIUM when production risk or ambiguity is high

Do not force a premium model assignment into every specialist file if that would make low-risk uses unnecessarily expensive. The task router may override based on stakes.

## Session reality

Claude Code supports selecting a model for a session with `--model`. Aurex should not pretend the primary interactive session can transparently switch its base model for every tiny tool action unless the current Claude Code environment explicitly supports that behavior.

Practical routing can happen through:

- launching the session at the appropriate model class
- delegating a bounded specialist/subagent with an appropriate model where supported
- running a separate focused Claude invocation for a specific escalated question
- using the configured small/fast model capabilities of supported provider setups

## Cost awareness

Do not quote or hard-code model prices into the permanent routing logic. Pricing and model availability change.

When cost comparison matters, verify current Anthropic pricing or the user's actual provider/subscription behavior.

## Quality floor

Cost savings never justify:

- shipping unverified high-risk changes
- allowing a fast model to make unsupported major strategic decisions
- skipping browser verification
- weakening accessibility, security, SEO, conversion, or launch gates
- accepting visibly generic work because a cheaper model produced it

If the cheaper route cannot meet Aurex quality efficiently, escalate.

## Routing output

When routing is materially relevant, use a compact declaration:

```text
MODE: STANDARD
MODEL CLASS: STANDARD
REASONING DIFFICULTY: Medium
RISK: Medium
SPECIALISTS: None
ESCALATION TRIGGER: Escalate only if implementation requires changing approved architecture or two focused debugging attempts fail.
```

Do not print routing metadata for trivial tasks unless it helps the human understand the decision.
