# Content issues – Life, Medical, Travel pages

**Capture caveat:** Firecrawl hit its free rate limit and direct HTTP to kenindia.com was blocked by the sandbox proxy (CONNECT 403). All 19 pages loaded through WebFetch, which gives a model-processed reading and won't return full verbatim text. Every content file is marked `content_status: extracted-not-verbatim`. Typo detection below covers only the phrases that were quoted exactly. Re-scrape with a working Firecrawl key, or get the copy from the client's CMS, before launch.

No pages returned 404. No SEO-spam or injected external links were found in the main content of any page. The only external links are site-wide footer and social links (akinsure.com, ira.go.ke, kenindiahr.peopleshr.com, x.com, facebook, instagram, eportal.kenindia.com).

## Site-wide (affects every page)
- **"croup" slug:** Group Life Cover lives at `/croup-life-cover/` and Group Personal Accident at `/croup-personal-accident/`. The pages work, but the slugs are typos. Use `/group-…` and add 301 redirects.
- **Generic "View Related Products" block:** Every life and medical page shows the same 4 links (Individual Pension Plan, Group Life Cover, Staff Retirement Benefit, Nguzo ya Jamii). These links aren't related to the product, and medical pages list no health products. Nguzo ya Jamii and Staff Retirement Benefit link to themselves.
- **Individual Pension Plan** (`/individual-pension-plan/`) is linked everywhere but isn't in the site navigation. Check whether it exists.
- **Many nav items link to `#`:** Downloads, Forms, Proposal Forms, Claim Forms, Insurance, Life Insurance, Individual, Corporate, Kenindia Medical.
- **Phone numbers differ:** the header and "Need Help?" show "+254 111101000 / 600", "Call NOW" dials tel:0111101000, and the medical pages show 020 2227275 / 020 316099.
- **Footer "About" mentions "housing insurance":** no such product is listed.
- **Privacy and Terms pages** sit under `/termsfeed/`, which suggests generated template text. Have legal review them.
- Many images have empty alt text or `![]()` placeholders.

## Life – Individual
- **15-years-money-back:** No typos found. The "Benefits" section says payouts are not deducted. Confirm the bonus terms ("vested bonus", "final additional bonus") match the other products.
- **academic-advantage:** The payout schedule adds up to 120% of the Sum Assured plus bonus (20+20+30+50). Confirm with the client.
- **anticipated-whole-life:** No obvious issues.
- **bima-account:** The return figure is from 2022 ("11%"), so it's stale for 2026. Its image is a generic screenshot filename (`img-2025-09-01-10-46-13…png`).
- **capital-advantage:** The return is the "11% … 2022 valuation", which is stale. "Unbeatable advantage" is an unsupported marketing claim (regulatory risk).
- **christmas-bonus:** Currency is written inconsistently ("KShs. 100,000/-" and "KShs. 2,500/="). The site elsewhere uses KES.
- **dynamic-advantages:** The slug is plural but the title is "Dynamic Advantage". The page has the grammar error "became payable" (should be "becomes") and "Joint Life Cover,Level Term Benefit" (missing space). It gives no ages, terms or amounts, so the content is thin.
- **economic-advantages:** The slug is plural but the title is "Economic Advantage". **Wrong banner image:** `bima-account-1-1024x320.jpg` belongs to Bima Account. The content is thin, with no ages or amounts.
- **education-endowment:** "Last but 1 years" should be "year". The monthly benefit line "on 1% of the sum assured is payable monthly" is missing a word. The table has no headers and an empty third column. The banner filename is generic (`Untitled-design-6…png`). No entry age, term or sum assured is given.
- **kumi-bora:** **Off-topic text from another product:** "Under motor commercial insurance, all private vehicles are covered. The covers given are classified into three levels as below:" The promised list is missing, and the sentence contradicts itself (motor *commercial* covering *private* vehicles). Other typos: "his/ her", "there after", "non- medical", "10years". The "extra 30%" wording is unclear because the 30% is already paid as survival benefits.
- **multiple-advantage:** **Wrong banner image:** `capital_advantage_2-1-1024x320.jpg`. The table has an unlabelled 5th column ("& Bonus"). "Joint Life Cover,Level Term Benefit" is missing a space. For the 20-year and 25-year terms, the first instalment comes late (year 10 and year 15), unlike the pattern for the other terms. Verify.
- **nguzo-ya-jamii:** "KES.50, 000" has a stray space. "stand alone" should be "standalone". The text "In the event of occurrence of death of any member insured the documents required include:" is followed by an empty list (the documents appear in another section). The "CLAIM PROCESSED WITHIN 48 HOURS" promise is in all caps. Confirm it's still accurate.
- **terms-assurance:** The slug and nav say "Terms Assurance" but the page heading says "Term Assurance". "NO ride is allowed" should be "No rider". The banner filename has a typo (`TERM-ASSURANCCE`). The age limit "over the age of fifty" is vague (entry or cover-ceasing age?). "Kshs 1,000,000.00" uses a different currency format from the rest of the site.

## Life – Corporate
- **staff-retirement-benefit:** "of the of the" is duplicated. "benefits are become payable" is a grammar error. The "Tax Benefits & Contributions." bullet has no detail. The early-leaver and death bullets appear in both the pension section and "Basic features". The "Highest returns" table ends at 2022, which is stale, doesn't say whether rates are gross or net, and the "highest" claim is unsupported. A "4% minimum guaranteed" rate is stated. Confirm it's current.
- **croup-life-cover (Group Life Cover):** Several sections have no headings on the page (labels were added in the file). **Contradiction:** exclusion 2 excludes motorcycling in general, but exclusion 4 allows motorcycles up to 500cc. Typos: "incase" (twice), "compliment" (should be "complement"), "tax relieve" (should be "relief"), "Phillips Pharmaceauticals", "birth day", "Air Line", "stage of siege" (should be "state of siege"), and "Benefits are payable the Company" (missing "to"). The company name varies between "Kenindia Assurance Co. Ltd" and "Kenindia Assurance Company". The client list names third parties. Get permission before republishing. The extraction found no related-products block or banner, so check the live page.

## Medical
- **corporate-health-plan, health-save-plan, individual-family-plan:** **All three pages have identical content.** The "Key Benefits" (8 bullets) and "Contact Us" sections are copied word for word, so nothing tells the products apart. None gives eligibility, ages, limits, premiums, waiting periods or exclusions. "Provision for ensuits and pavilions" is a typo for "en-suites" and is unclear. "Smart systems" is vague. "24 – hour" has stray spacing. The related products are all life or pension products. The email address is Cloudflare-obfuscated, so get the real address from the client.

## General – Travel
- **travel-insurance:** "USS" is used throughout instead of "US$". "Personality Liability" should be "Personal Liability" (it appears twice). The section "1" should be "I". **Suspicious figure:** "Death benefits for children over 70 years" makes no sense (perhaps "adults over 70" or "children under …"). The Section A amounts are merged into one cell and the table headers are malformed. "pre- existing" has a stray space. Hospital benefit "USS10 per day up to USS 100" and travel delay "USS10/hr up to USS 50" look low. Confirm current limits.
