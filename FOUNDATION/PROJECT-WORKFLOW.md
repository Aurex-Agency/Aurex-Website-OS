# Aurex Project Workflow

This workflow defines how Aurex moves from a new client to a launched website. It is designed to keep the process collaborative without slowing production unnecessarily.

## Phase 0: Intake

Collect the minimum information needed to understand the project.

Required inputs:

- business name and current website
- primary business objective
- primary conversion
- services or products
- target market and geography
- existing brand assets
- available photography and video
- known competitors
- known technical or platform constraints
- desired launch timing

Output: completed `PROJECT-BRIEF.md` draft.

Human gate: confirm that the brief represents the business accurately enough to begin discovery.

## Phase 1: Discovery and research

Research the business, customers, market, competitors, search landscape, and current digital presence.

Analyze:

- business model
- audience segments
- customer intent
- strongest differentiators
- objections
- proof assets
- competitive positioning
- competitor website patterns
- current site strengths and weaknesses
- content gaps
- search intent and organic opportunities
- local-search opportunities where relevant
- likely conversion paths

Separate facts from assumptions. Flag unknowns that materially affect strategy.

Output: discovery findings and strategic opportunity summary.

Human gate: review major findings and correct misunderstandings before creative direction.

## Phase 2: Positioning and conversion strategy

Define how the website should persuade.

Establish:

- primary audience
- primary promise
- primary conversion
- secondary conversions
- CTA hierarchy
- major objections
- proof strategy
- message hierarchy
- offer structure
- trust strategy
- page-level conversion roles

Output: website strategy summary.

Human collaboration: review the primary message and conversion strategy before visual exploration.

## Phase 3: Site architecture and content map

Design the site around user intent, conversion, content depth, and organic visibility.

Determine:

- global navigation
- primary pages
- service/product page groups
- location pages where genuinely useful
- proof/case-study pages
- educational/resource pages
- utility/legal pages
- internal linking relationships
- primary search intent for each important page
- primary conversion role of each page

Output: proposed sitemap and page-category bundles.

Human gate: approve or adjust the site architecture before full content production.

## Phase 4: Creative direction

Develop three meaningfully different creative directions unless the project clearly calls for a narrower exploration.

Each direction should include:

- concept name
- visual thesis
- emotional tone
- typography direction
- color strategy
- image/video treatment
- layout philosophy
- shape language
- motion personality and intensity
- hero concept
- section-transition approach
- reasons the direction fits the business
- risks or tradeoffs

The directions should be strategically valid, not superficial palette swaps.

Recommendation: identify the strongest direction and explain why.

Human gate: select, combine, or refine a direction before detailed design/build.

## Phase 5: Design system and homepage structure

Translate the chosen direction into a practical system.

Define:

- typography roles and scale
- color tokens and contrast rules
- container and grid behavior
- spacing rhythm
- button hierarchy
- form style
- card and surface philosophy
- image treatment
- icon style
- motion tokens
- section transition patterns
- breakpoint behavior

Then create the homepage information architecture and section sequence.

Output: `DESIGN-SYSTEM.md` and homepage page spec.

Human collaboration: review the homepage structure before the build becomes visually expensive to change.

## Phase 6: Hero build and first visual proof

Build the navigation, hero, and enough surrounding context to prove the selected direction in the browser.

Evaluate:

- immediate message clarity
- perceived quality
- brand fit
- imagery
- color balance
- typography
- CTA visibility
- motion restraint
- desktop composition
- mobile composition

Use actual browser inspection, not code review alone.

Human gate: approve or redirect the hero and visual language.

Do not build the entire site while the visual foundation is still uncertain.

## Phase 7: Homepage build

Build the complete homepage as the primary proof of the system.

The homepage should create a coherent journey rather than a collection of components.

Review:

- storytelling and pacing
- conversion sequencing
- objection handling
- proof placement
- section rhythm
- imagery needs
- transition quality
- accessibility
- responsive behavior
- performance implications

Use explicit media placeholders when final assets are missing.

Human gate: homepage approval.

## Phase 8: Page-category bundles

After the homepage is approved, build the remaining site in logical page bundles.

Example bundles may include:

### Services bundle
- services overview
- individual service pages
- process page

### Products/commerce bundle
- category pages
- product/detail templates
- financing or purchase support

### Trust bundle
- about
- team
- testimonials
- case studies/projects
- credentials

### Local visibility bundle
- locations
- service-area pages where genuinely useful
- local contact/location detail pages

### Education bundle
- resources
- FAQs
- guides
- blog/article templates

### Conversion bundle
- contact
- quote/request form
- booking
- financing/application
- campaign landing pages

Not every site requires every bundle.

For each bundle:

1. define the role of the pages
2. establish shared template logic
3. build representative pages
4. review content, conversion, SEO, and UX
5. get human approval
6. complete the bundle

Human gate: approve each meaningful bundle before moving to the next when the visual or strategic pattern is new.

## Phase 9: Content, SEO, and organic-depth pass

Review the complete website as an information system.

Verify:

- page purpose is distinct
- search intent is matched appropriately
- titles and metadata are intentional
- heading structure is logical
- copy is useful and specific
- no keyword stuffing
- internal links connect related content
- important entities/services/locations are explained clearly
- schema is used only where supported and useful
- indexability/canonical decisions are correct
- sitemap and robots behavior are intentional
- local signals are accurate where applicable

Research current guidance for material SEO decisions rather than relying on outdated memory.

## Phase 10: Conversion review

Review the entire website as a conversion system.

Assess:

- value proposition clarity
- CTA hierarchy
- form friction
- trust and proof
- objection coverage
- offer clarity
- contact accessibility
- mobile CTA access
- page-to-page conversion continuity
- message match
- conversion tracking requirements

Do not confuse more CTAs with better CRO.

## Phase 11: Motion and interaction pass

Finalize animation after the content and layout are stable enough to judge correctly.

Review:

- page entrance behavior
- section transitions
- asset reveals
- hover feedback
- navigation interactions
- interactive components
- scroll-linked motion
- mobile motion
- reduced-motion behavior

Default to motion intensity 3-7 depending on the brand.

Use sophisticated animation only where it improves story, comprehension, attention, or perceived quality.

## Phase 12: Responsive and accessibility QA

Inspect representative pages across meaningful viewport sizes.

At minimum evaluate:

- large desktop
- laptop/tablet landscape
- tablet/small desktop
- common mobile width

Check:

- hierarchy
- line length
- tap targets
- navigation
- forms
- image cropping
- overflow
- content order
- focus states
- keyboard use
- contrast
- landmarks and semantics
- reduced motion

Mobile must be actively designed, not merely functional.

## Phase 13: Technical, performance, and analytics QA

Verify as appropriate:

- production build passes
- no material console errors
- optimized images/media
- lazy loading decisions
- font loading
- layout stability
- Core Web Vitals considerations
- crawlability
- redirects
- 404 behavior
- canonical URLs
- analytics installation
- conversion events
- consent requirements where applicable
- forms and integrations
- security-sensitive configuration

## Phase 14: Final creative-director review

Review the website with fresh eyes.

Ask:

- Does this look like it belongs uniquely to this business?
- Is the main thing still the main thing?
- Does every major page have a purpose?
- Does the site feel premium without feeling self-indulgent?
- Is color doing enough work?
- Is imagery doing enough work?
- Are there obvious AI-generated patterns?
- Are repeated templates becoming visually monotonous?
- Is the conversion path natural and clear?
- Are weak client assets exposed honestly through placeholders/recommendations rather than hidden with generic design?
- Is mobile equally intentional?
- Would we confidently put the Aurex name on this project?

Fix critical and important issues before launch readiness.

## Phase 15: Launch readiness and handoff

Confirm:

- approvals are complete
- production environment is configured
- forms deliver correctly
- tracking is live
- domains/DNS are correct
- important redirects are prepared
- search-engine requirements are satisfied
- backups/version control are in place
- client-owned accounts and credentials are handled appropriately
- launch checklist is complete

Human gate: final launch approval.

## Phase 16: Post-launch learning

The project is not finished at deployment.

After meaningful traffic accumulates, review available evidence:

- conversion activity
- user behavior
- search visibility
- landing-page performance
- form completion
- call/contact patterns
- page engagement
- technical issues

Document repeatable lessons for future projects.

If a lesson is systemic, propose an update to Aurex Website OS.

## Collaboration principle

The human creative lead should be involved frequently enough to prevent expensive wrong turns, but not so frequently that the system becomes a sequence of tiny approvals.

Default human gates:

1. intake/brief accuracy
2. discovery and strategic findings
3. sitemap/page bundles
4. creative direction
5. homepage structure
6. hero/visual proof
7. full homepage
8. each new page-category pattern
9. final creative review
10. launch

The system may compress gates for simple projects or expand them for high-risk, high-budget, or unusually complex projects.
