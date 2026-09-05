# Website Expansion Requirements

## Introduction

Custom Logic will expand from a single landing page into a credible, conversion-focused corporate site. The initial release must distinguish owned products from selected custom work and establish a clear, evidence-led route to enquiry.

## Requirements

### Requirement 1: Credible positioning

**User story:** As a prospective client, I want to understand what Custom Logic builds and why it is credible, so that I can decide whether to contact the company.

#### Acceptance criteria

1. The homepage states that Custom Logic builds and operates software for complex industries.
2. The homepage presents Custom Logic as a South African product engineering company, not a general web-design agency.
3. The site presents the verified fact that Tenders-SA passed 2,000 registered users in September 2026 without making unsupported claims.
4. The footer shows Custom Logic SA Pty Ltd and registration number 2024/853353/07.

### Requirement 2: Phase-one journeys

**User story:** As a visitor, I want clear routes to learn about the company and start the right kind of conversation.

#### Acceptance criteria

1. Primary navigation links to Products, Work, Services, Engineering, Company and Insights only when each destination exists.
2. The homepage provides product exploration and project-enquiry calls to action.
3. The Company page explains operating principles and legal identity without invented biographies.
4. The Contact page distinguishes product, improvement, partnership, enterprise Tenders-SA, and media/investment intent.

### Requirement 3: Qualified contact experience

**User story:** As a potential customer or partner, I want to provide enough context for Custom Logic to respond appropriately.

#### Acceptance criteria

1. The form collects the approved fields and consent using accessible labels and help text.
2. Client-side validation prevents incomplete submissions and associates errors with fields.
3. The static release does not expose form content in URLs or transmit it to analytics.
4. Direct email remains available as a fallback.

### Requirement 4: Quality baseline

**User story:** As a visitor using any device or assistive technology, I want the site to remain fast and usable.

#### Acceptance criteria

1. New pages use unique title, description and canonical metadata.
2. Navigation works by keyboard and at mobile widths.
3. Interfaces maintain visible focus, sufficient contrast and reduced-motion support.
4. No new framework, CMS, stock photography or unverified screenshots are introduced.

## Implementation dependencies

- Current public Tenders-SA screenshots and descriptive alternative text must be added as optimised local assets.
- Founder name, photo and biography are published when supplied for the Company page.
- A server-side form endpoint, spam protection and analytics provider configuration are required before production enquiry capture.
