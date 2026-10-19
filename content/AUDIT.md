# Kenindia.com – Website Audit

Reviewed: 19 October 2026 · 76 URLs (55 pages, 15 news posts, legal pages, sitemaps)
Detailed per-page findings are in `content/_issues/`.

---

## 🔴 1. Urgent: signs the current site has been tampered with

Two pages contain content that has nothing to do with Kenindia and looks injected (a common attack on WordPress sites that inserts hidden advertising links):

| Page | What's there |
|---|---|
| /want-to-be-an-agent/ | French-language paragraphs promoting online casino bonuses, with an outbound casino link. Sitemap shows the post was last modified 12 Dec 2025. |
| /motor-private/ | Two paragraphs about NBA players' car collections with an outbound link to a sports website, in the middle of the product description. |

**Recommendation for Kenindia's IT team (do this now, independent of the redesign):** remove the content, check WordPress admin users for unknown accounts, update WordPress core/themes/plugins, change all admin and hosting passwords, and scan the rest of the site and database for similar links. For a regulated insurer, spam links on product pages also damage Google ranking and customer trust.

---

## 🟠 2. Broken or missing functionality

- **No forms available.** The Downloads page is empty. "Forms", "Proposal Forms", "Life General" and "Claim Forms" all link to `#`. Customers cannot download a claim form.
- **2020 financial statements** link is broken (empty link).
- **10+ menu items go nowhere** (`#`): Downloads, Forms, Individual, Corporate, Kenindia Medical, etc.
- **Homepage quote tabs** (Life / Housing / Motor / Health) link to `#`. "Housing insurance" is offered in the quote form but no such product exists.
- **Empty or near-empty pages still live:** /brochures/, /news-media/, /about-us/ (duplicate of /about/), /individual-pension-plan/ (heading only, yet linked from every life product page).
- **News Room** listing doesn't show the 2026 CSR posts.
- **Careers:** all listed jobs and the cleaning RFP are past their deadlines.

## 🟠 3. Wrong content on product pages (customer and regulatory risk)

- **Plate Glass Insurance** has no plate-glass content at all — the body is the Motor Commercial text.
- **Engineering Insurance:** the Erection All Risks section contains motor insurance wording; two sections appear twice.
- **Motor Commercial** says "all private vehicles are covered" (copied from Motor Private).
- **Kumi Bora** (life product) contains a stray motor insurance sentence.
- **All three medical plans** (Corporate Health, Health Save, Individual/Family) have identical text — no eligibility, limits, waiting periods or exclusions to tell them apart.
- **Personal Accident and Group Personal Accident** have identical text.
- **Public Liability:** "Limits of Indemnity" section is empty.
- **Marine:** ICC(B) and ICC(C) clauses listed without descriptions.
- **Travel Insurance:** "USS" instead of US$, "Personality Liability", and a confusing line "Death benefits for children over 70 years". Limits look low — verify they're current.
- **Group Life Cover:** two exclusions contradict each other on motorcycling.
- **Wrong banner images** on Carrier Legal Liability, Engineering, Economic Advantage and Multiple Advantage (they show other products' banners).
- **"Related products"** is the same four links on every page, regardless of the product.

## 🟡 4. Trust and credibility

- **Homepage testimonials are template placeholders:** one job title is literally "Designation", two quotes are identical and mention "Crystalo" (another company), the third is filler text. Photos are stock images and a blank profile icon.
- **About page progress bars** show "Insurance 0%" and "Protection 0%".
- **Inconsistent facts:** company age is "45 years" on About and "47 years" on Home; headline premium figure is from 2022 although 2023–2025 accounts are published; About's "12% growth" for 2023 doesn't match the figures shown.
- **Two different sets of company values** (About vs Careers).
- **Company name** written five different ways.
- **Board and Management pages:** names only — no photos or bios.
- **"Unbeatable" / "Highest returns"** claims on life and pension products, with return tables that stop at 2022.

## 🟡 5. Contact details

- Branch emails show as `name@www.kenindia.com` — a malformed address that likely doesn't receive mail.
- Eldoret branch shows the Westlands email; Kisii shows the Nakuru email; Machakos has none.
- Phone numbers written in 5+ formats (e.g. "0111101/000/452."); medical pages show older 020 numbers.
- No opening hours and no map links for any of the 15 branches.

## 🟡 6. Legal and data protection

- Privacy Policy and Terms are a generic online template referencing US/EU law (CCPA, CalOPPA, GDPR) with **no reference to Kenya's Data Protection Act 2019**, a liability cap in US dollars, and internal contradictions ("we do not sell data" vs "we may sell data").
- Quote, contact and newsletter forms collect personal data without a consent notice.
- Recommend Kenindia's legal/compliance team or Data Protection Officer provides updated policies.

## ⚪ 7. Quality and usability

- **Navigation:** ~35 products in three-level dropdowns, duplicated menus, hard to use on phones. No way to filter products ("for me / for my business") or compare them.
- **No claims guidance:** no "how to make a claim" page anywhere.
- **Typos** across most pages (e.g. "Health Insurace", "Frequently Ask Questions", "Perfomance", "lightening", "Pharmaceauticals", URL slugs "croup-…" instead of "group-…").
- **Images:** almost no alt text (accessibility and SEO), raw WhatsApp/camera filenames, oversized files.
- **Brand assets:** no vector logo; ISO badge text should read "ISO 9001:2015".

---

## How the new site fixes this

| Problem | New site |
|---|---|
| Hard-to-use menus | Insurance hub with filters (Individuals / Businesses / category) and a clean product template |
| No forms or claims help | Downloads centre + "Make a Claim" guide with steps and forms per product |
| Copied / wrong content | One structured template per product (cover, benefits, eligibility, exclusions, FAQs, forms) managed in an admin panel |
| Stale jobs, figures, news | Admin panel with expiry dates, auto-hiding closed jobs, editable figures in one place |
| Spam injection risk | No WordPress plugins; locked-down admin with roles, 2-factor login and an activity log |
| Contacts inconsistent | Branch locator with verified details, hours and map links |
| Legal gaps | Kenya Data Protection Act consent on every form, updated policies (supplied by Kenindia) |
