---
name: aurex-stack
description: Selects or validates the technical stack for an Aurex website based on project requirements, SEO, content, integrations, maintainability, motion, and deployment constraints. Use before scaffolding a new project or proposing a migration.
---

# Aurex Stack Selection

Do not choose technology because it is trendy or because it was used on the previous client.

## Default recommendation

For a new multi-page Aurex SMB marketing website without unusual requirements, start from:

- Next.js App Router
- TypeScript
- Tailwind CSS
- server components by default
- Motion for ordinary animation
- GSAP/ScrollTrigger only when the creative concept requires advanced choreography
- Radix/shadcn primitives only where useful, visually restyled to the client
- Vercel by default unless hosting constraints differ

## Validate against the project

Review:

1. page count and content structure
2. SEO and rendering requirements
3. CMS/editor requirements
4. forms and CRM integrations
5. ecommerce or authenticated functionality
6. motion complexity
7. expected traffic
8. hosting constraints
9. client ownership and handoff
10. developer maintenance burden
11. existing codebase
12. launch timeline

## Preserve versus migrate

If an existing site already has a maintainable stack, do not migrate simply to match Aurex defaults.

Recommend migration only when the benefit is material, such as:

- severe maintainability problem
- rendering/SEO limitation
- performance limitation that is architecture-driven
- security/unsupported framework risk
- major feature requirements
- deployment/ownership problem

Quantify or explain the benefit and cost.

## Dependency plan

Before scaffolding, classify dependencies as:

- required platform
- required design/interaction
- integration-specific
- optional convenience

Keep optional convenience dependencies out until they are justified.

## Output

Return:

### Recommendation
The selected stack and hosting approach.

### Why
How it fits the business, content, SEO, conversion, motion, and maintenance requirements.

### Non-default choices
Any choice that differs from Aurex defaults and why.

### Dependency plan
What should be installed initially versus only when needed.

### Risks
Known tradeoffs and future constraints.

### Human decision
Only ask when there are two materially different valid architectures or the choice changes cost/ownership significantly.