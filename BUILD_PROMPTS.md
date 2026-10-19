# Kenindia Website – Build Prompts for your IDE

Use these **one at a time, in order**. Check the result in the browser after each one.
Before you start: copy the whole `content/` folder, `AUDIT.md` and your `MOTION.md` / motion components from the Tosh project into the new project folder.

---

## K1 – Project brief (CLAUDE.md)

```
Create CLAUDE.md in the project root with the content below and follow it for every task.

# Project: Kenindia Assurance – website redesign
Kenindia Assurance Company Limited, Nairobi, Kenya. Founded 6 December 1978. Composite insurer: general insurance, life insurance, pensions and medical. Regulated by the Insurance Regulatory Authority (IRA). ISO 9001:2015 certified.
Existing site: kenindia.com (WordPress). We are rebuilding it with a modern design, all existing content, and an admin panel.

## Source content
- content/ contains every page of the current site as markdown, grouped by folder (general-insurance, life-insurance, medical, company, resources, news).
- content/_issues/ and AUDIT.md list known errors. FIX them in the new site (typos, wrong slugs, duplicated text) but NEVER invent product facts, figures, limits, benefits or testimonials. Where content is wrong or missing, show a clearly marked placeholder: [TO CONFIRM WITH KENINDIA: ...].
- Files marked `content_status: extracted-not-verbatim` contain paraphrased prose. Keep the facts, and flag in a list at /admin/content-review that the wording must be checked against Kenindia's WordPress export before launch.
- Do NOT migrate: the casino text on want-to-be-an-agent or the NBA paragraph on motor-private (injected spam).

## Tech stack
- Next.js (App Router) + TypeScript + Tailwind CSS. (React, but with server rendering so ~60 pages rank well on Google and load fast on phones.)
- Framer Motion + Lenis, using the motion system from MOTION.md (copy components into src/components/motion and src/lib/motion.ts).
- Supabase for database, auth and file storage (added in K8).
- lucide-react icons. Fonts self-hosted via next/font.
- Hosting: Vercel.

## Pages / information architecture
- / Home
- /insurance – hub with filters: "For me & my family" / "For my business", and categories (Motor, Property & Engineering, Liability, Marine & Transit, Travel, Life & Savings, Education, Pensions & Retirement, Health)
- /insurance/[category]/[product] – one shared product template
- /claims – how to make a claim (general, life, medical), steps, required documents, forms
- /downloads – proposal forms, claim forms, brochures, filterable
- /about, /about/board, /about/management, /about/csr
- /investors – financial statements by year
- /careers and /careers/[job]
- /news and /news/[slug]
- /faqs (searchable, grouped)
- /contact – head office + branch locator
- /get-a-quote – multi-step quote request
- /become-an-agent
- /privacy, /terms, /data-protection
- ePortal (https://eportal.kenindia.com/) and Job portal stay EXTERNAL links. Never build logins for customers.
- 301 redirects from every old URL (see content/_issues/all-urls.md), e.g. /croup-personal-accident/ → /insurance/personal-accident/group-personal-accident.

## Design direction
- Same principle as MOTION.md: dark, cinematic, 3D hero; light, very readable inner sections; shared motion language. Elegant, trustworthy, premium – a 47-year-old institution, not a startup.
- Colours: take the primary and accent colours from Kenindia's logo (public/brand/logo). Dark sections use a deep navy close to #070B1A. Define all colours as tokens in tailwind config so they're easy to change.
- Typography: JetBrains Mono for eyebrow labels, numbers, figures and small UI accents (as in the reference screenshot); a highly readable sans-serif (e.g. Inter) for body text and long product details, since insurance content is long.
- Decorative 3D elements themed for insurance: glass shields, umbrellas, soft spheres, a light beam – used sparingly.
- Mobile-first. Most Kenyan visitors are on mid-range Android phones and mobile data: keep pages light, images optimised, heavy effects lazy-loaded and disabled on low-end devices.
- Accessible: WCAG AA contrast, alt text everywhere, keyboard navigation.

## Preview safety
- Until Kenindia approves and launches, the deployed site must: require a password (Vercel password protection or simple middleware), send `noindex, nofollow`, and show a small banner "Design preview – not the official Kenindia website".
- All forms in preview mode show a success message but must not send real customer data anywhere.

## Contact data
- Main phone: +254 111 101 000 (show as "0111 101 000"), tel:+254111101000
- Address: Kenindia House, Loita Street, Nairobi. P.O. Box 44372-00100 G.P.O. Nairobi
- Emails are unverified – use [TO CONFIRM] placeholders.
- Branches: content/resources/contact-us.md (normalise phone formats; flag wrong emails).
- Social: X https://x.com/KenindiaKE, Facebook https://www.facebook.com/KenindiaAssurance/, Instagram https://www.instagram.com/kenindiaassurance
- Footer must show: "Regulated by the Insurance Regulatory Authority" with a link to ira.go.ke, plus AKI link and the ISO 9001:2015 badge.

## Legal (Kenya)
- Every form collecting personal data needs a consent checkbox referencing the Kenya Data Protection Act, 2019 and linking to /privacy.
- Privacy policy and terms must come from Kenindia's legal/compliance team. Use clearly marked placeholders until then.
- No analytics or tracking cookies until Kenindia confirms; then add a consent banner.
```

## K2 – Content model and import

```
Read every file in content/ and design a TypeScript content model in src/content/types.ts for: Product (title, slug, category, audience: individual|business|both, summary, heroImage, sections[] with type: overview|cover|benefits|eligibility|extensions|exclusions|premiums|claims|table|faq, relatedProducts, forms[], status: ok|needs-review, notes), Branch, Person (board/management), Document (forms, statements), NewsPost, Job, FAQ, CompanyFact (key figures with year and source).

Then write a script that converts all markdown in content/ into typed JSON in src/content/data/. Apply the fixes from content/_issues/ (typos, slugs, duplicated sections removed) and set status "needs-review" with a note on every product that has wrong, missing or paraphrased content (e.g. Plate Glass, the three medical plans, Engineering). Write a report CONTENT_REPORT.md listing every product, its status and what needs confirming. Do not invent anything.
```

## K3 – Design system, motion and layout

```
Set up the design system from CLAUDE.md: Tailwind tokens, fonts, and the motion system from MOTION.md (adapt colours to Kenindia's brand). Build the shared layout:
- Top utility bar: phone, email placeholder, "Make a claim", ePortal button.
- Navbar: glass pill that shrinks on scroll, logo, Insurance (mega-menu with the categories split into "For me & my family" / "For my business", each item with icon and one-line description), Claims, About, Downloads, News, Contact, and a primary "Get a quote" button. Mobile: full-screen menu with staggered links and an accordion for categories.
- Footer: about text, quick links, products, contact, social, newsletter (with consent), IRA/AKI/ISO, copyright with current year.
- Floating WhatsApp/Call button: [TO CONFIRM: does Kenindia have a WhatsApp business number?] – build it behind a config flag.
- Preview banner + noindex + password protection as in CLAUDE.md.
Then show me /motion-demo using Kenindia's colours.
```

## K4 – Home page

```
Build the Home page using content/company/home.md:
1. Dark cinematic hero: SplitText headline using Kenindia's real taglines ("Guarding Your Today – Shaping Your Tomorrow", "Your Stability – Our Priority", "We Have A Mutual Interest – You") as a slow rotating set, 3D glass shield/umbrella elements, light beam, CTAs "Get a quote" and "Make a claim".
2. Quick "What do you want to protect?" picker: Car, Home & Property, Family & Life, Health, Travel, Business – each linking to the filtered insurance hub.
3. Featured products as TiltCards.
4. "Who we are" story with the 1978 founding and CountUp figures – ONLY figures from content (years since 1978 computed dynamically; latest Gross Written Premium marked [TO CONFIRM latest year]).
5. "How claims work" timeline with DrawLine (Report → Submit documents → Assessment → Settlement).
6. Why choose us: Assistance, Claims, Online (ePortal), Feedback – staggered icon cards.
7. Testimonials section built but HIDDEN until real testimonials are added in the admin (the current ones are template placeholders).
8. Latest news (3 posts), ISO and IRA trust strip, the company video (YouTube 1MTkZPys7mU, loaded only when clicked – lightweight facade), final CTA band.
```

## K5 – Insurance hub and product template

```
Build /insurance and the product template.
Hub: filter chips (audience + category), search box, product cards with icon, category tag and summary, animated layout on filter.
Product page: compact animated header with breadcrumb and category eyebrow; sticky side navigation of sections on desktop (tabs on mobile); sections rendered from the content model (cover levels as comparison cards, benefits as icon list, tables responsive, exclusions in an accordion); "Downloads for this product" (proposal/claim forms); "Get a quote for this product" form; FAQ; related products chosen by category (not the old generic list); "Need help?" box with phone and nearest branch link.
If a product has status "needs-review", show a small admin-only notice (not visible to the public build) and render placeholders for missing parts.
Generate all ~37 product pages and check each one renders.
```

## K6 – Company, investors, careers, news, FAQs

```
Build: About (story, journey timeline 1978 → today with DrawLine, mission, ONE set of values [TO CONFIRM which set], ISO), Board and Management (cards with photo placeholders, hover reveal of bio placeholders), CSR (story cards from the news posts in the CSR category), Investors (financial statements by year as a timeline list linking to the PDFs from content/resources/financial-statements.md; 2020 marked [missing]), Careers (job cards with closing dates; closed jobs automatically move to "Past opportunities"; link to the external job portal), News list with categories and post pages, FAQs grouped and searchable with an accordion.
```

## K7 – Claims, downloads, contact, quote, agent

```
Build:
- /claims: choose claim type (Motor, Property, Life, Medical, Travel, Personal Accident…), steps for each, documents required (from product content; placeholders where missing), downloadable form, contacts.
- /downloads: filter by type (Proposal form, Claim form, Brochure) and product; each item shows file type and size. All current form links are placeholders – Kenindia must supply the PDFs.
- /contact: head office card, branch locator (list + search by town; each branch with address, P.O. Box, phone, email placeholder, opening hours placeholder and "Open in Google Maps" link), contact form.
- /get-a-quote: multi-step form (what to insure → details → contact → consent), progress bar, validation, calm motion, celebratory success state.
- /become-an-agent: requirements from content/news/…want-to-be-an-agent.md (without the spam) and an application form.
All forms: consent checkbox (Kenya Data Protection Act), honeypot + rate limiting against spam. Preview mode: don't send data.
```

## K8 – Backend (Supabase)

```
Add Supabase for content and leads. Explain how to create the project. Choose the region with Kenindia's IT team and note in CONTENT_REPORT.md that Kenya's Data Protection Act has rules on storing personal data outside Kenya.

Tables: products (+ product_sections), categories, branches, people, documents, news_posts, jobs, faqs, company_facts, testimonials, site_settings (contacts, social links, announcement banner, WhatsApp flag), leads (quote requests, contact messages, agent applications – with type, product, branch, status: new/in progress/closed, assigned_to), newsletter_subscribers (with consent timestamp), audit_log.
Storage buckets: images (public), documents (public PDFs), private-uploads (if any form takes files).
Row Level Security on everything: the public can only read published content and insert leads/subscribers; staff permissions come from roles (K9).
Seed all content from src/content/data. The website reads from Supabase with caching (Next.js revalidation) and falls back to the JSON if Supabase is unavailable.
```

## K9 – Admin panel

```
Build the admin at /admin for Kenindia staff (non-technical). English UI, clean light theme, mobile-friendly, help tip on each section.

Auth & security: email + password with mandatory 2-factor (TOTP), no public sign-up, session timeout, password reset. Roles:
- Super Admin (IT): everything, manage users and roles, settings.
- Marketing/Editor: products, home page, news, testimonials, FAQs, banners.
- HR: careers only (and job applications).
- Finance: investors/financial statements.
- Customer Service: leads inbox and branches.
Every change is written to an audit log (who, what, when) visible to Super Admin.

Content workflow: Draft → Published, preview before publishing, scheduled publishing, revision history with restore. Unsaved-changes warning, confirmation before deleting, trash with 30-day restore.

Sections:
1. Dashboard: new leads, drafts awaiting publishing, jobs closing soon, products marked needs-review.
2. Products: edit all sections with a structured editor (no raw HTML), reorder sections, attach forms, set related products, upload banner (auto-compressed to WebP with alt text required).
3. Home page: hero slides, featured products, key figures (with year and source), announcement banner.
4. News & CSR: rich-text editor, featured image, category, gallery.
5. Careers: jobs with closing date (auto-hide after deadline), PDF upload.
6. Downloads: upload forms/brochures, tag by product and type.
7. Investors: upload financial statements by year.
8. Branches & contacts.
9. People: board and management with photos and bios.
10. FAQs and Testimonials (with "permission obtained" checkbox required before publishing).
11. Leads inbox: filter by type/product/branch/status, assign to staff, notes, one-click call/email, export CSV, automatic deletion after a retention period set in Settings (Data Protection Act).
12. Users & roles, Settings, Activity log.
13. Content review: the list of items marked needs-review/paraphrased, to tick off before launch.

Write ADMIN_GUIDE.md: short, friendly how-tos for each role. Test the admin on a 375px phone.
```

## K10 – SEO, performance, launch

```
1. SEO: titles and descriptions per page, Open Graph images, sitemap.xml, robots.txt (noindex while in preview), JSON-LD InsuranceAgency/Organization with head office and branches, BreadcrumbList on product pages, 301 redirects for every old URL.
2. Performance: Lighthouse ≥ 90 on mobile for Home, a product page and Contact. Test on throttled "Fast 3G".
3. Accessibility audit and fixes.
4. Check every link and every product page renders; list remaining [TO CONFIRM] items in LAUNCH_CHECKLIST.md.
5. Give me step-by-step instructions to deploy the preview on Vercel with password protection, and (later, after Kenindia approves) how their IT team points kenindia.com to it without breaking their email, keeping eportal.kenindia.com as it is.
```
