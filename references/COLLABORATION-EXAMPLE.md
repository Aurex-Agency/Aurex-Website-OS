# Aurex Collaboration Example

This example shows how ChatGPT, Claude Code, GitHub, and the human creative lead should collaborate without transferring long chat histories.

## Scenario

Client: fictional roofing company

Current state: website strategy and homepage creative direction have been approved in ChatGPT with the human creative lead.

Current task: implement the approved homepage hero.

Mode: STANDARD

## 1. Strategy discussion stays outside Claude

ChatGPT and the human may have explored multiple concepts, competitor references, copy directions, and conversion ideas.

Claude does not need that whole conversation.

The approved decision is compressed into `AUREX-BRIEF.md`.

## 2. Example build brief

```md
# Aurex Build Brief

## Assignment
Task: Implement the approved homepage hero.
Operating mode: STANDARD
Business reason: Increase immediate clarity and lead intent while making the brand feel more premium and distinct from local roofing competitors.

## Approved context
Relevant artifacts:
- CREATIVE-DIRECTION.md
- DESIGN-SYSTEM.md
- WEBSITE-STRATEGY.md

Approved concept: Protection Over Everything

## Exact scope
In scope:
- desktop/mobile navigation behavior required by hero
- hero composition
- hero media treatment
- primary/secondary CTA
- hero trust signal
- approved hero motion

Out of scope:
- services section redesign
- site-wide footer
- internal pages

## Creative intent
The hero should feel architectural, protective, premium, and local. The visual should make the home feel like the object being protected rather than using generic roofer-at-work stock composition.

Motion should create one meaningful reveal and then get out of the way.

## Conversion requirements
Primary CTA: Request My Roof Inspection
Secondary CTA: Call Now

The primary value proposition and CTA must be understandable without waiting for animation.

## Must not change
- approved brand palette
- approved core headline
- global service taxonomy

## Acceptance criteria
- value proposition is immediately understandable
- imagery is dominant but does not reduce CTA legibility
- hero feels specific to the roofing concept
- primary CTA is visually obvious
- mobile composition is intentionally redesigned, not simply stacked
- reduced-motion experience remains complete

## Verification
- desktop browser inspection
- 390px mobile inspection
- CTA destination test
- reduced-motion test
- relevant typecheck/lint
```

## 3. Claude implementation

Claude reads the brief and approved artifacts, then only the source files required for the hero.

Claude should not:

- research local roofing competitors again
- invent three new creative directions
- run a full-site SEO audit
- invoke every specialist

Claude may use the Motion Director or Frontend Architect if a specific implementation problem justifies it.

## 4. Claude status handoff

After implementation Claude updates `AUREX-STATUS.md`.

Example:

```md
# Aurex Project Status

## Current state
Current operating mode: STANDARD
Current branch: feature/homepage-hero-v1
Current project stage: Homepage hero implementation

## What is already approved
- website strategy: approved
- creative direction: Protection Over Everything
- hero concept: approved

## Most recent work completed
Implemented the new homepage hero with responsive media, primary/secondary CTA, trust line, and reduced-motion fallback.

Material areas changed:
- app/page.tsx
- components/home/Hero.tsx
- styles/hero.css

## Verification performed
- desktop browser inspection: passed
- 390px mobile inspection: passed
- CTA destinations: passed
- reduced motion: passed
- typecheck: passed
- lint: passed

## Known issues
Polish:
- tablet crop around 820px may benefit from review

## Requested review
Review only creative-direction fidelity, conversion clarity, visual hierarchy, and mobile experience for the hero. Do not perform a full-site audit.

## Next recommended action
Review hero before continuing into the homepage body.
Suggested mode: STANDARD
```

## 5. ChatGPT GitHub review

The human asks ChatGPT:

```text
@GitHub Review feature/homepage-hero-v1. Read AUREX-STATUS.md, CREATIVE-DIRECTION.md, and the changed hero files. Review only creative fidelity, conversion clarity, visual hierarchy, and mobile UX.
```

ChatGPT inspects GitHub rather than asking the user to paste the source code.

## 6. Example focused review

```md
# Aurex Review

Status: REVISE

Summary:
The concept is clearly present and the hero feels substantially more client-specific. Keep the media treatment and headline hierarchy. Two issues prevent approval: the mobile CTA hierarchy becomes visually flat, and the trust line feels disconnected from the hero story.

## What is working
1. The image treatment reinforces protection rather than generic roofing labor.
2. Desktop headline hierarchy is strong.
3. Motion is restrained and does not delay comprehension.

## Required revisions

### Important revision 1
Issue: On mobile, the primary and secondary CTA receive nearly equal visual weight.
Why it matters: The desired lead action becomes less obvious at the most constrained viewport.
Intended outcome: Restore a clear primary action without making the secondary call path difficult to access.
Acceptance criteria: At 390px the inspection CTA reads as the dominant action at first glance.

### Important revision 2
Issue: The trust line is visually separated from the promise it is meant to support.
Why it matters: Proof is present but not reducing uncertainty at the decision point.
Intended outcome: Integrate the trust statement into the CTA/promise area without adding visual clutter.
Acceptance criteria: The proof reads as direct support for the primary claim and CTA.

## Do not change
- hero media treatment
- desktop headline composition
- motion concept

## Revision handoff
Suggested mode: QUICK
Specialist needed: none
Recommended next action: Make the two bounded revisions and re-check desktop/mobile.
```

## 7. Claude revision

Notice the revision drops from STANDARD to QUICK.

Claude does not rerun the homepage process. It fixes two bounded issues, verifies them, updates status, and pushes.

## Why this is efficient

The expensive reasoning happened once.

The approved decision became durable state.

Claude consumed only implementation context.

ChatGPT reviewed the GitHub result, not a transcript.

Revision context was small and precise.

No system repeatedly re-read the entire project.

That is the intended Aurex collaboration model.
