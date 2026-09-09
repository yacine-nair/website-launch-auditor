# Website Launch Auditor

A Manus skill that turns “build me a website” into a complete build-and-launch workflow. It helps an AI agent create the requested website, then audit its launch readiness across SEO, privacy, accessibility, responsive design, forms, links, metadata, and performance.

## What it does

The skill instructs the agent to:

- Understand the website type, audience, conversion goal, data flows, jurisdictions, and deployment constraints.
- Build the requested pages, components, routes, content, and interactions.
- Add or assess the launch essentials: privacy policy, terms, CTA, FAQ, `robots.txt`, `sitemap.xml`, custom 404, image alt text, analytics, meta titles, meta descriptions, social metadata, favicon, canonical URLs, cookie consent, mobile behavior, accessibility, form behavior, broken links, and performance.
- Decide conditionally rather than blindly adding every item to every project.
- Distinguish verified results from assumptions and blocked production configuration.
- Produce a final launch report with `PASS`, `CONDITIONAL`, `BLOCKED`, and `N/A` statuses.

## Why it is useful

AI-generated websites often look finished while missing important production details. This skill adds a repeatable quality gate so that the agent does not stop at visual implementation. It checks whether the site is discoverable, usable, accessible, testable, privacy-aware, and ready for deployment.

The checklist is intentionally context-aware. For example, analytics and cookie consent are not added automatically to a site that does not need them, private application routes are not exposed in a sitemap, and a contact form is not described as functional unless its delivery backend is connected.

## The 20-point launch checklist

1. Privacy policy
2. Terms page
3. Clear primary CTA
4. FAQ when useful
5. `robots.txt`
6. `sitemap.xml`
7. Custom 404 page
8. Image alt text
9. Analytics when requested or appropriate
10. Unique meta titles
11. Useful meta descriptions
12. Social sharing metadata
13. Favicon
14. Canonical URLs
15. Cookie consent when required
16. Mobile-responsive behavior
17. Accessibility
18. Form testing
19. Broken-link checks
20. Performance optimization and verification

## Installation in Manus

1. Download or clone this repository.
2. Add the `SKILL.md` file to your Manus skills directory, preserving the directory name `website-launch-auditor`.
3. Enable or install the skill in your Manus environment.
4. Ask Manus to create or improve a website as usual.

The skill is activated by requests involving website creation, rebuilding, improvement, shipping, SEO, accessibility, legal pages, responsive behavior, forms, analytics, or launch readiness.

## Example prompts

```text
Build a responsive landing page for my consulting business and make it ready to launch.
```

```text
Audit this existing SaaS website before deployment and fix everything you can.
```

```text
Create an ecommerce site, including the production-readiness checklist, metadata, mobile layout, forms, and a final launch report.
```

## Expected final report

The agent should finish with a table similar to this:

| Check | Status | Evidence or finding | Action needed |
|---|---|---|---|
| Mobile behavior | PASS | Tested at narrow and wide viewports | None |
| Contact form | BLOCKED | Delivery service is not configured | Add backend or form provider |
| Privacy policy | CONDITIONAL | Draft uses owner placeholders | Review business data practices |
| Sitemap | PASS | Public routes included; private routes excluded | None |

The report must end with one of:

- **Ready to launch**
- **Ready after listed fixes**
- **Not ready to launch**

## Important limitations

This skill does not provide legal advice or guarantee compliance with any law. Generated privacy and terms content must be reviewed and completed by the website owner, and professional legal advice may be necessary. It also does not invent credentials, domain configuration, analytics IDs, payment settings, backend endpoints, or business identity details.

A check is marked `BLOCKED` when the agent cannot verify it because required information, credentials, backend integration, or production configuration is missing.

## Repository structure

```text
website-launch-auditor/
├── SKILL.md    # Instructions loaded by Manus when the skill is triggered
└── README.md   # Human-facing documentation for GitHub
```

## License

Choose and add a license appropriate for your project before publishing this repository. If you want a permissive default, consider the MIT License.
