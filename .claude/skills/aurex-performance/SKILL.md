---
name: aurex-performance
description: Audits and improves an Aurex website's loading, interactivity, visual stability, JavaScript, media, fonts, third-party scripts, and Core Web Vitals without flattening the approved design. Use before launch and when performance regresses.
---

# Aurex Performance Audit

Use `FOUNDATION/PERFORMANCE-STANDARD.md`.

## Principle

Optimize the experience, not just a Lighthouse number.

Protect the approved creative concept, but require expensive effects to justify their cost.

## Step 1: Test production-like output

Do not audit only development mode.

Run the production build and serve/deploy it in a representative environment.

Audit representative templates, not only the homepage.

## Step 2: Identify likely user-facing bottlenecks

Inspect:

- LCP element
- image/video payloads
- font loading
- route JavaScript
- hydration/client boundaries
- third-party scripts
- long tasks
- layout shifts
- expensive continuous animation
- network waterfall

## Step 3: Core Web Vitals

Use current good thresholds as the long-term target:

- LCP <= 2.5s
- INP <= 200ms
- CLS <= 0.1

Prefer field data at the 75th percentile when enough real traffic exists.

Lab tools diagnose likely problems but do not replace field data.

## Step 4: Prioritize by impact

Classify findings:

### Blocker
Materially harms usability, conversion, crawlability, or accessibility.

### High impact
Likely meaningful user improvement.

### Medium impact
Worth fixing when practical.

### Low impact
Micro-optimization or score chasing.

Fix highest user/business impact first.

## Step 5: Creative-cost review

For every expensive visual effect, record:

- experience value
- loading/runtime cost
- mobile cost
- alternative implementation

Do not automatically remove premium media. First attempt to optimize loading, encoding, responsive delivery, or activation strategy.

## Step 6: Re-test

After changes, re-run the same representative tests.

Do not claim improvement from code changes alone.

## Output

### Performance verdict
Pass / Pass with improvements / Revise / Block launch

### Highest-impact findings
Ranked list with evidence.

### Core Web Vitals
Available field and lab signals, clearly distinguished.

### Payload/runtime findings
Media, JS, fonts, third parties, animation.

### Changes made
What was optimized and why.

### Remaining tradeoffs
Creative or integration costs that remain.

### Next measurement
What should be monitored after launch.