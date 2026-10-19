# Company & Resources — content issues (kenindia.com, extracted 2026-10-19)

## Extraction caveat (read first)
- Firecrawl was rate-limited and direct HTTP to kenindia.com was blocked by the proxy, so all pages were captured with WebFetch, which caps verbatim quotes at ~125 chars.
- Exact: headings, names, titles, figures, dates, URLs, form labels, FAQ questions, short paragraphs. NOT verbatim: longer paragraphs marked `[paraphrase]` in home.md, about.md, careers.md, faqs.md, and nearly all of privacy-policy.md and terms-and-conditions.md. Re-copy these from the live site before go-live.
- Branch emails on Contact are Cloudflare-obfuscated; decoded values are unverified.

## Broken / placeholder links
- Financial Statements: **2020 "Download >>" has an empty/invalid href** — the 2020 accounts are not downloadable.
- Downloads page (/downloads/) body is **empty**: no proposal forms, claim forms or documents.
- Header menu items with `href="#"`: Downloads, Forms, Proposal Forms, Life General, Claim Forms, General Insurance, Life Insurance, Individual, Corporate, Kenindia Medical; homepage quote tabs (Life/Housing/Motor/Health Insurance).
- "Proposal Forms > Life General" — odd label (Life vs General mixed); no forms exist behind it.
- Homepage "Life Insurance" quick link goes to /croup-life-cover/ — a page not in the menu (typo slug "croup"; target likely missing/unlisted). Verify.
- Slug typo `/croup-personal-accident/` (should be "group").
- Homepage "Property Insurance" card links to /engineering-insurance/ (mismatch).
- Privacy policy refers to a "Cookies Policy" that is not linked/does not exist.
- CSR post slug typo: `...water-solutionsat-akuisi...` (missing hyphen).

## Placeholder / template text
- Homepage testimonials are template content: Sophia Murage's designation is literally **"Designation"**; Sophia and Steve Juma have identical quotes mentioning **"Crystalo"** (another company/template name) — "A true to work with Crystalo."; Wyclife Abayo's quote is lorem-ipsum-derived ("Same as saying through shrinking from all pain…"). All use a blank-profile stock photo.
- Homepage "Get Right Solutions" and "Professional advices" have identical text.
- Homepage "KenIndia's mission is to provide the best insurance services" heading has no body; real mission is on About page — inconsistent.
- About page progress bars: "Insurance 0%", "Protection 0%" (unconfigured template widgets).
- Hero slide 4 "Capital Advantage Plan - you" looks unfinished.
- Insurance page: medical section titled "Kenindia Insurance" (menu calls it "Kenindia Medical"); several cards reuse the same image (property-insurance-1.webp used for Professional Indemnity, Terms Assurance, Corporate Health Plan; kenindia-19 used 3x); no descriptive copy; all images lack alt text.
- Privacy policy/terms are a generic TermsFeed template: US/EU frameworks (CCPA/CPRA, CalOPPA, GDPR) with no reference to Kenya's Data Protection Act 2019; liability cap in "100 USD"; refers to "the Application"; "Usage Date" vs "Usage Data"; "FRCA" typo; CCPA "By email:" with no address; contradictory "we do not sell" vs "we may sell and may have sold"; geolocation "No" (cat. G) vs collected (cat. L); minor age 13 vs 16; Company address "Nairobi.." double period; "Country: Nairobi Municipality, Kenya".
- Board/Management pages: no bios and no photos in markup for any person.

## Typos / grammar
- "Health Insurace" (homepage quick link); "insurace" and "can keep you protection to keep you moving forward" (About).
- "Frequently Ask Questions" (FAQ page title).
- FAQ: "inform of cheque" (in the form of), "January 2003and" (missing space), "Enter you M-PESA Pin", "ANY ONE ESLE".
- Homepage: "quotation.. but first" (double period); "Why choose us for your all types of insurance"; "Professional advices".
- CSR excerpts missing spaces: "CompanyLimited", "battlingcancer", "struggledwith".
- Management: "HOD Credits Control" (likely Credit Control); "Head of Human Resource"; "Carol Wauw" — verify spelling.
- Board: "Mr. Hemnabh Khatau" — verify spelling; inconsistent honorifics ("Dr Manu Chandaria" without period vs "Dr. Patricia King'ori").

## Outdated / inconsistent figures
- Company age: About says "over a period of 45 years"; homepage says 47 years. Both tied to year-end 2022 (1978→2022 = 44 years). Pick one, ideally computed dynamically.
- Latest headline figure is 2022 (Ksh 11.1B GWP) though 2023/2024/2025 accounts are published; About "Our Journey" stops at 2023.
- About journey: 2021 = Kshs 13.7B, 2022 = Kshs 11.1B, 2023 = Kshs 13.1B with "12% growth" — 11.1→13.1 is ~18%, and 2021→2022 is a drop. Terminology varies ("Gross Written Premium" vs "gross return premium" vs "returns").
- Company name varies: Kenindia Insurance Ltd (About), Kenindia Assurance Co Ltd / Co. Ltd / Company Limited, KenIndia / KENINDIA.
- Careers: "multi-award-winning" claim with no awards listed. Careers intro says closing 28 Aug 2026 but listed jobs close up to 25 Sep 2026; all deadlines (and the RFP, due 7 Aug 2026) are now past as of 19 Oct 2026 — openings appear stale.
- Careers image is a WhatsApp photo from Dec 2023 (WhatsApp-Image-2023-12-04...jpeg).

## Emails / phones
- Contact page branch emails decode to `name@www.kenindia.com` (e.g. life@www.kenindia.com, branch1@www.kenindia.com) — malformed domain (should presumably be @kenindia.com). Head office header email decodes to kenindia@kenindia.com, so the two disagree. Careers "Email Us" also decodes to recruitment@www.kenindia.com.
- Eldoret Branch email = westlands@… and Kisii Branch email = nakuru@… (copy-paste errors). Machakos has no email.
- Phone formats inconsistent: "+254 111101000 / 600" (header/footer) vs "0111101000/600" vs "0111101/000/452." (misplaced slash, trailing period) for Enterprise Road, Eldoret, Machakos, Meru ("622," trailing comma), Kisii.
- Nyeri P.O. Box "884-100" — postal code looks truncated (Nyeri is 10100).
- Thika Office P.O. Box "7478-00100, Thika" — 00100 is Nairobi GPO code (Thika is 01000). Verify.
- Enterprise Road Branch address given as "Bamburi Road, G.T. Bank House" — branch name vs street mismatch; verify.
- No working hours and no map links anywhere on Contact.
- Footer emails are obfuscated and could not be read.

## Missing content
- No proposal/claim forms anywhere (Downloads empty).
- No board/management bios or photos.
- CSR page only lists 3 posts with no thumbnails (empty image tags).
- About page "Our Values" PITAR vs Careers "Shared Company Values" (Respect, Innovation, Customer Focus, Integrity) — two different value sets.
