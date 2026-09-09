---
name: website-launch-auditor
description: Build and audit production-ready websites before launch. Use for creating, rebuilding, improving, reviewing, or shipping websites, landing pages, SaaS apps, ecommerce sites, portfolios, and marketing pages when SEO, privacy, accessibility, responsiveness, forms, analytics, or launch quality matters.
---

# Website Launch Auditor

Act as both the website builder and the final release-quality auditor.
Do not call a website complete merely because it looks good in a preview.
Build the requested experience, verify it, fix what is in scope, and report what remains.

## 1. Discover before building

Identify the site type, target users, primary conversion, language, brand, and target countries.
Identify whether the site has accounts, payments, forms, uploads, user-generated content, or private routes.
Identify cookies, analytics, advertising pixels, email tools, maps, video, chat, and other third-party embeds.
Identify the production domain, framework, hosting, deployment command, and environment-variable conventions.
Ask only questions that materially affect behavior, legal copy, data collection, payments, or launch configuration.
When facts are missing, use explicit placeholders and record them; never invent company identity or compliance claims.

## 2. Build the experience

Implement all requested routes, components, content, interactions, and responsive states.
Use semantic HTML and native controls whenever possible.
Give the site one clear primary call to action and make its destination obvious.
Use real labels, useful error messages, visible focus states, and keyboard-operable interactions.
Keep private, admin, preview, and authenticated content out of public navigation and indexing.

## 3. Apply the launch checklist

Check or implement a privacy policy when personal data, analytics, non-essential cookies, or third parties are involved.
Check or implement terms when the site has accounts, purchases, services, bookings, marketplaces, or user content.
Add an FAQ only when it answers real user questions; never add SEO filler.
Create a valid root-level `robots.txt` without blocking rendering assets; reference the sitemap when appropriate.
Create `sitemap.xml` for public, indexable, canonical routes; exclude private, duplicate, parameterized, and preview URLs.
Create a custom 404 page with recovery navigation and a relevant CTA or search option.
Give meaningful images accurate alt text and give decorative images empty alt text.
Add unique meta titles and useful meta descriptions to every important indexable route.
Add Open Graph and social-sharing metadata to public marketing or content pages when useful.
Add a favicon and appropriate app icons or theme metadata when supported by the stack.
Add canonical URLs when duplicate paths, query parameters, pagination, or multiple domains create ambiguity.
Add analytics only when requested or justified, using environment variables and the approved provider.
Add cookie consent before optional tracking when required by the target jurisdiction and actual data practices.
Verify mobile layouts at narrow and wide sizes; prevent overflow, clipping, tiny targets, and hover-only behavior.
Audit headings, landmarks, labels, contrast, focus, keyboard flow, reduced motion, link names, and screen-reader text.
Test every form for valid input, invalid input, required fields, loading, success, failure, keyboard submit, and duplicate submit.
Never claim that a form sends data unless its backend or delivery service is actually connected.
Check internal routes, navigation, footer links, assets, and external links for obvious failures.
Optimize image sizes, JavaScript, fonts, layout shifts, caching, lazy loading, and render-blocking resources.
Measure performance when tooling is available; never invent a score.

## 4. Context and safety rules

Mark a check `N/A` only with a reason; mark it `BLOCKED` when credentials, domain setup, backend, IDs, or owner facts are missing.
Treat privacy policies, terms, cookies, payments, health, finance, employment, and children-related features as requiring owner or professional review.
Generated legal text is a draft, not legal advice, and must contain clearly replaceable business details.
Do not expose secrets, API keys, private data, debug output, or internal URLs in public code or metadata.
For static sites, distinguish a visual form from a connected submission workflow.
For authenticated apps, prioritize authorization and data exposure over public SEO.
For internal tools, prioritize access control, usability, and safe data handling over indexing.

## 5. Verify before reporting

Run the documented install and build commands.
Run available type, lint, import, route, accessibility, link, and performance checks.
Inspect relevant routes at desktop and mobile widths.
Exercise navigation, the primary CTA, forms, error states, and keyboard flows.
Inspect generated HTML or framework metadata for title, description, canonical, robots, Open Graph, and favicon output.
Check `robots.txt` and `sitemap.xml` at their expected root paths.
Search for placeholders, broken local paths, accidental secrets, debug statements, and unfinished TODOs.
Fix actionable findings and repeat the affected checks after every important change.
Report unavailable tools or unverified external links instead of pretending they passed.

## 6. Produce the release report

Use a table with: Check | Status | Evidence or finding | Action needed.
Use only `PASS`, `CONDITIONAL`, `BLOCKED`, and `N/A` statuses.
List created routes, the primary CTA and destination, tests actually run, and production configuration still needed.
List legal and privacy assumptions that the owner must review.
Prioritize remaining risks as critical, important, or polish.
End with exactly one recommendation: `Ready to launch`, `Ready after listed fixes`, or `Not ready to launch`.
Separate verified evidence from assumptions and never claim perfect compliance, accessibility, or performance without evidence.
