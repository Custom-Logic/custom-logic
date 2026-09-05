# Website Expansion Design

## Architecture

The existing Cloudflare Pages deployment is a dependency-free static site. Phase 1 keeps that model: shared `site.css` and `site.js`, with static HTML routes represented by folder `index.html` files. This gives each public route a canonical URL without adding a framework or CMS.

## Content structure

Phase 1 publishes `/`, `/company/` and `/contact/`. Global navigation exposes only those live sections and product/work/service/engineering/insights anchors are intentionally deferred until their pages are complete. The homepage contains the approved product proof and links to the canonical Tenders-SA domain.

## Interaction design

- Desktop navigation presents Company and Contact; the primary action is “Build with us”.
- Mobile navigation uses a native disclosure panel, keyboard-operable with Escape-to-close behaviour.
- The contact form validates required fields locally. Because there is no approved server endpoint, submission shows a clear non-transmitting acknowledgement and preserves direct email as the actionable fallback.
- Motion is decorative only and disabled for reduced-motion preferences.

## Content safeguards

Claims are sourced from the supplied, verified expansion brief. Tenders-SA is described as a live procurement intelligence product with more than 2,000 registered users as of September 2026. Public screenshots will be integrated as optimised local assets; no fictional people, customer logos or testimonials are used.

## Future phases

Phase 2 adds Products, Work and the canonical Tenders-SA case study after approved screenshots are supplied. Phase 3 adds Services and Engineering. Phase 4 adds Insights, sitemap expansion, structured-data refinements, analytics and an approved server-side contact delivery route.

## Engineering and editorial evidence

The Engineering and Insights sections use the verified Tenders-SA implementation material as their primary evidence base: the local `F:\projects\tendersa` repository and the public Tenders-SA engineering articles. Tender data is sourced through OCPO/OCDS; the separate government intelligence pipeline covers policy, audit, enforcement and gazette information. Corporate pages summarise outcomes and link to the original product articles instead of duplicating consumer procurement guidance.
