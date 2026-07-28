# Uptempo Enterprises Design Backlog

## CDO Readout

Uptempo Enterprises currently presents as a clean static catalog of apps. The design is simple, legible, and low-maintenance, but it does not yet communicate the more ambitious "Tiny.com-like" business idea: a focused company that builds, owns, operates, and possibly acquires a family of durable small software businesses.

Tiny's public site has a few strong patterns worth adapting rather than copying: a clear thesis, proof metrics, a portfolio family, founder/operator credibility, a simple contact motion, and language that makes the company feel like a long-term home for businesses. Uptempo can use the same strategic ingredients while keeping its own scale and voice.

## North Star

Make Uptempo feel like a professional product holding company: calm, credible, founder-led, product-minded, and long-term oriented.

Primary audience:
- Customers deciding whether the apps are trustworthy.
- Potential partners, sellers, or collaborators evaluating whether Uptempo is real and serious.
- App Store reviewers and support visitors looking for clear legal and support paths.

Design principles:
- Lead with the company thesis, not just the app list.
- Show the portfolio as a family with clear status, category, and maturity.
- Replace generic Apple-inspired styling with a more ownable editorial/holdco identity.
- Add proof before polish: metrics, screenshots, usage, launch status, testimonials, or founder notes.
- Keep the static site deployable through GitHub Pages.

## Independent Backlog

### 1. Reposition the Homepage Hero

Priority: P0
Effort: Small
Files: `docs/index.html`, `docs/styles.css`

Problem:
The current hero says "Digital Product Lab" and "simple products," which is pleasant but undersells the Tiny-like ambition.

Task:
Rewrite and restyle the hero around a clearer holdco/product studio thesis.

Suggested direction:
"We build and operate small, useful software businesses."

Acceptance criteria:
- Hero has a confident one-sentence thesis.
- Supporting copy explains what Uptempo owns or builds.
- Primary CTA points to the portfolio section.
- Secondary CTA points to contact.
- Hero no longer feels like a generic app developer landing page.

### 2. Create a Portfolio Grid Instead of Repeated Product Rows

Priority: P0
Effort: Medium
Files: `docs/index.html`, `docs/styles.css`

Problem:
The current product rows are very tall and repetitive. They make the company feel like a loose list of unrelated apps.

Task:
Replace the vertical product articles with a tighter portfolio grid.

Each product card should include:
- Icon or screenshot.
- Product name.
- Category.
- One-line promise.
- Status: Live, Coming Soon, In Development, Storefront, etc.
- Primary action: App Store, Learn More, Privacy Policy, or Visit Site.

Acceptance criteria:
- Six current products fit comfortably above the fold or close to it on desktop.
- Cards share a consistent information architecture.
- Incomplete products do not feel broken; they have intentional status labels.
- Mobile layout remains clean and scannable.

### 3. Add Company Proof Metrics

Priority: P0
Effort: Small
Files: `docs/index.html`, `docs/styles.css`

Problem:
Tiny leads with proof. Uptempo currently has no visible signals of momentum, scope, or seriousness.

Task:
Add a compact metrics band below the hero.

Possible metrics:
- Products launched.
- Active categories.
- Platforms supported.
- Years operating.
- "Founder-owned" or "independent" if accurate.

Acceptance criteria:
- Metrics are accurate and easy to update.
- Metrics support credibility without exaggeration.
- The section visually breaks up the hero and portfolio.

### 4. Add an "Our Approach" Section

Priority: P0
Effort: Medium
Files: `docs/index.html`, `docs/styles.css`

Problem:
The site does not explain how Uptempo thinks, chooses products, or operates. Tiny's appeal comes from a clear operating philosophy.

Task:
Add a section that explains Uptempo's operating principles.

Suggested pillars:
- Build for everyday workflows.
- Keep products simple and durable.
- Operate with long-term care.
- Respect customer privacy.

Acceptance criteria:
- Section is written in plain language.
- It creates a bridge between individual apps and the company vision.
- It avoids vague startup language.

### 5. Build an Acquisition / Partnership CTA

Priority: P1
Effort: Small
Files: `docs/index.html`, `docs/styles.css`

Problem:
If the aspiration is Tiny-like, the site needs a clear path for founders, app owners, or partners to reach out.

Task:
Add a CTA section for small software businesses, apps, or product opportunities.

Suggested copy:
"Have a small software business that deserves a long-term home?"

Acceptance criteria:
- CTA is clearly distinct from product support.
- CTA uses `mailto:info@uptempoenterprises.com` or a dedicated acquisition email if created.
- Copy is modest and credible at Uptempo's current scale.

### 6. Improve the Header and Navigation

Priority: P1
Effort: Small
Files: `docs/index.html`, `docs/support.html`, `docs/stadium-music.html`, `docs/styles.css`

Problem:
Navigation is minimal and inconsistent across pages. The homepage has only Support; Stadium Music adds Privacy and Terms.

Task:
Create a consistent header across public pages.

Suggested links:
- Portfolio
- Approach
- Support
- Contact

Acceptance criteria:
- Header links work from all pages.
- Current page structure remains GitHub Pages-friendly.
- Mobile does not overflow.
- Legal links move to footer or product pages instead of crowding primary nav.

### 7. Use the Uptempo Wordmark as a Brand Asset

Priority: P1
Effort: Small
Files: `docs/index.html`, `docs/styles.css`, `docs/assets/uptempo-wordmark.png`

Problem:
The repo includes a wordmark, but the site currently uses plain text for the logo.

Task:
Evaluate and use the wordmark in the header or hero if it renders professionally at small sizes.

Acceptance criteria:
- Logo is crisp on standard and retina displays.
- Alt text is correct.
- Header height remains restrained.
- If the wordmark is not strong enough, document the decision and keep text logo.

### 8. Establish a More Ownable Visual System

Priority: P1
Effort: Medium
Files: `docs/styles.css`

Problem:
The current visual language is mostly Apple default: blue accent, SF/Inter, rounded app icons, light gray background. It is polished but generic.

Task:
Create a more distinctive but restrained design system.

Suggested changes:
- Introduce a warmer neutral background.
- Use a darker ink color.
- Replace default iOS blue with a more ownable accent.
- Define reusable tokens for surface, border, muted text, accent, and success/status colors.
- Keep border radii modest and consistent.

Acceptance criteria:
- Site no longer reads as a default Apple marketing page.
- Palette supports multiple product brands without clashing.
- Contrast remains accessible.

### 9. Add Product Detail Pages for Each App

Priority: P1
Effort: Large
Files: `docs/index.html`, new pages under `docs/`

Problem:
Only Stadium Music has a dedicated product page. Other products link directly to the App Store, support, or privacy pages.

Task:
Create lightweight product pages for GoTime, Growbie, Photo Packs, Race Ready 5K, and TheSavvyChefs.

Acceptance criteria:
- Each page has a hero, product promise, key features, support/legal links, and primary action.
- App Store products have App Store links.
- Products without a live destination have an intentional status and contact/support path.
- Homepage cards link to detail pages where available.

### 10. Replace Inline Stadium Music CSS With Shared Components

Priority: P2
Effort: Medium
Files: `docs/stadium-music.html`, `docs/styles.css`

Problem:
Stadium Music includes a large inline style block that duplicates button, card, grid, and section patterns.

Task:
Move reusable styles into `docs/styles.css` and convert Stadium Music to shared components.

Acceptance criteria:
- No broad inline style block remains in `docs/stadium-music.html`.
- Buttons, cards, chips, grids, and section titles are reusable across pages.
- Stadium Music visual layout is preserved or improved.

### 11. Add Founder / Operator Credibility

Priority: P2
Effort: Medium
Files: `docs/index.html`, `docs/styles.css`

Problem:
Tiny has trust through named founders, history, testimonials, and portfolio reputation. Uptempo currently has no human layer.

Task:
Add a concise founder/operator section.

Possible content:
- Who runs Uptempo.
- What kinds of products Uptempo likes.
- Why the company exists.
- A small portrait only if there is a good image.

Acceptance criteria:
- Section increases trust without becoming a personal bio page.
- Copy is specific and grounded.
- It helps potential partners understand who they are contacting.

### 12. Build a Support Hub by Product

Priority: P2
Effort: Medium
Files: `docs/support.html`, `docs/styles.css`

Problem:
The support page is too generic and does not list all current products or legal links.

Task:
Turn Support into a product support hub.

Acceptance criteria:
- Each product has a support row or card.
- App-specific privacy and terms links are easy to find.
- Contact instructions are clear.
- Race Ready 5K is not the only product called out.

### 13. Improve Metadata and Social Sharing

Priority: P2
Effort: Small
Files: `docs/index.html`, `docs/stadium-music.html`, `docs/support.html`, `docs/assets/og-image.svg`

Problem:
Metadata is basic and some paths are likely incorrect or inconsistent. The homepage uses `../assets/og-image.svg` from `docs/index.html`, which may not resolve as intended on the deployed domain.

Task:
Audit and update title, description, Open Graph, Twitter card, canonical URLs, and favicon paths.

Acceptance criteria:
- Homepage social preview uses the correct absolute or root-relative asset path.
- Every public marketing page has a clear title and description.
- Product pages have product-specific sharing metadata.

### 14. Optimize Image Assets

Priority: P2
Effort: Medium
Files: `docs/assets/`

Problem:
Several 1024x1024 icons are over 700 KB to 1.1 MB. This is heavy for a simple static site.

Task:
Create optimized web versions of icons and screenshots.

Acceptance criteria:
- Use appropriately sized images for display contexts.
- Preserve high-quality source assets if needed.
- Reduce homepage image payload materially.
- Add width and height attributes to key images to reduce layout shift.

### 15. Add a Footer With Company, Product, Legal, and Contact Links

Priority: P2
Effort: Small
Files: `docs/index.html`, `docs/support.html`, `docs/stadium-music.html`, `docs/styles.css`

Problem:
The footer only says "Uptempo Enterprises LLC." It misses a chance to make the site feel complete and trustworthy.

Task:
Create a structured footer.

Suggested groups:
- Company: Home, Approach, Contact.
- Products: GoTime, Growbie, Stadium Music, Photo Packs, Race Ready 5K, TheSavvyChefs.
- Legal: Privacy/terms links where applicable.
- Contact: email.

Acceptance criteria:
- Footer is consistent across pages.
- Legal links are findable without dominating the header.
- Footer looks complete on mobile.

### 16. Create a Small Content System for Product Statuses

Priority: P3
Effort: Medium
Files: `docs/index.html`, `docs/styles.css`

Problem:
Some products are live, some coming soon, some have only privacy links, and some have no destination. Right now this inconsistency feels accidental.

Task:
Define status badges and actions.

Statuses:
- Live
- Coming Soon
- In Development
- Storefront
- Support Only

Acceptance criteria:
- Every portfolio item has one status.
- Status labels use consistent colors and wording.
- Actions match the status.

### 17. Add Case Study Modules for Mature Products

Priority: P3
Effort: Large
Files: new pages under `docs/`

Problem:
For a Tiny-like business, the portfolio needs depth over time: why a product exists, who it serves, and what changed after launch.

Task:
Create reusable case study sections for products that have enough substance.

Acceptance criteria:
- Case studies include customer, problem, solution, product screenshots, and outcome.
- They can be added one product at a time.
- They support both customer trust and acquisition/partner credibility.

### 18. Add Analytics Event Tracking for CTAs

Priority: P3
Effort: Small
Files: `docs/index.html`, `docs/stadium-music.html`

Problem:
Google Analytics is installed, but CTA clicks are not explicitly tracked.

Task:
Add lightweight event tracking for key outbound actions.

Acceptance criteria:
- App Store links, email links, support links, and learn-more links send named events.
- Tracking does not break links if analytics fails.
- Event names are consistent.

## Recommended First Sprint

1. Reposition the homepage hero.
2. Convert product rows to a portfolio grid.
3. Add proof metrics.
4. Add "Our Approach."
5. Add partnership/acquisition CTA.
6. Improve header/footer consistency.

This sprint would make the biggest strategic difference without requiring new product pages, new photography, or a CMS.
