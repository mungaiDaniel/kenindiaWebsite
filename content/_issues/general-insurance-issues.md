# General Insurance – content issues

Source: WebFetch structured extraction (not verbatim) on 2026-10-19. Firecrawl was rate-limited. motor-private was skipped because the coordinator already has it.

## Site-wide
- **Spam check:** I checked all 17 pages for injected or off-topic paragraphs and for unrelated external links such as sports, celebrity, NBA, cars or betting. **None were found in the main content.** The only external links are in the footer (AKI, IRA, social media, TermsFeed, job portal). Caveat: WebFetch reads through a summarising model, so a raw-HTML check is still advisable.
- **Same related products on every page:** "View Related Products" always shows Travel, Bonds, Motor Commercial and Motor Private, whatever the product. This looks like template text. On Bonds and Motor Commercial it links to the page itself.
- **Slug typo:** the Group Personal Accident URL is `croup-personal-accident`. Fire Insurance uses `fire-insurance-2`.
- **Phone mismatch:** the page shows "+254 111101000 / 600", but the links use `tel:0111101000` and `tel:+254 111101000`. The email is hidden by Cloudflare, so the actual address is not visible in the page.
- **Repeated boilerplate:** most pages share "Premiums form the basis **or** the consideration for indemnity" ("of" intended) and the fragment "The consideration for indemnity being premiums."
- **Brand spelling:** "KenIndia", "Kenindia", "Kenindia Assurance Company Ltd" and "Kenindia Assurance Co Ltd" are all used.
- **Placeholder menu links:** several menu items link to `#` (Downloads, Forms, Proposal Forms, Claim Forms, Individual, Corporate, Kenindia Medical). Some images have empty `![]()` sources.
- **Repeated "Need Help?" box:** "Need Help?", +254 111101000 / 600, an email hidden by Cloudflare, and a "Call NOW" button. The banner reads "We're here to protect your business, life and much more..." with a "Learn More" button linking to /about.

## Per page
- **plate-glass-insurance (critical):** there is no plate glass content at all. The page body is the Motor Commercial text, with a "Motor Commercial" heading and the same banner image (image-1-1024x320.png). Three of its related-product links are `#` placeholders. Real content is needed from Kenindia.
- **engineering-insurance:** the Erection All Risks section contains Motor Commercial text: settlement by "repair the motor vehicle", the market value of the vehicle, the "Radio Cassette" and "Windscreen" extensions, the excess paragraph and the Motor PSV paragraph. Deterioration of Stock and Engineering Business Interruption each appear twice. The banner is the All Risk image (all-risk-1-1024x320.jpg). Typos: "subject to of each and every item", "with consent of insures", "the insurance contain", "compliments" (should be complements), "e.t.c.", "etc.The", "( Sudden". The product list says "Contractors All Risks" but the heading says "Contractors All Risk".
- **motor-commercial:** the intro says "all private vehicles are covered", which looks copied from Motor Private. Also "the insurance contain an imposed excess", "repair the motor vehicle", "break in", the outdated "Radio Cassette", and the excess amount is not stated.
- **personal-accident / group-personal-accident:** the Cover, Age, Sum Insured and Benefits text is identical on both pages. The individual Personal Accident page talks about "the employee" and earnings multiples, which looks copied from the group product. "result into any contingencies"; "On permanent or total disablement." has no benefit amount. Currency formats are mixed: "Kshs 1,000/=" and "Kshs 25,000/-".
- **carrier-legal-liability:** the banner is the Bonds image (bonds-1-1024x320.jpg). "which ever may occur first"; "thereof" is unclear. No limits or exclusions are given.
- **public-liability:** the **empty section** "Limits Of Indemnity" says "as given below:" and nothing follows. "The consideration for indemnity being premiums" appears twice, once inside the Cover list. Also "guests personal effects", "employees of sub-contractors", and the US spelling "defense".
- **marine-insurance:** ICC(B) and ICC(C) are listed with no descriptions. "e.t.c" is used throughout; "physical and or presence of fog"; "marine Insurance". The intro sentence "The basis of the contract is the proposal" may be cut off. The Transport section reads like internal underwriting guidance. The image filename is misspelled "marinei_nsurance".
- **fire-insurance:** "lightening", "the basis of the contract are proposal forms", "furniture's", "Auditors Fees", "( LOSS OF PROFITS)", and "insurance for occurring fire cases". The domestic note refers to "contents under section B", but no Section B is defined for that product.
- **goods-in-transit:** "lighting" should be "lightning". The cover is called "All Risks" but is "subject to limited specific perils", which contradicts it. "(widely accepted)" is unexplained.
- **professional-indemnity:** "The covers caters for", a run-on sentence ("business notice of a claim"), "replacing or restoring such costs", "be a partner in the firm". The image filename is misspelled "proffesional".
- **work-injury-benefits:** "in the cause of employment" should be "course". "work injury benefits Act" should be capitalised as the Work Injury Benefits Act. The limit of liability is in the schedule and not shown.
- **bonds-insurance:** "commonly signed by insurers" (probably "issued"); "These guarantees that, dutiable goods…". The accordion is titled "Bond Insurance" but the page is "Bonds Insurance". There are no exclusions or limits. The banner has a generic filename (image-2-1024x320.png).
- **burglary-insurance:** "Stock in Trade the property of the insured…" is missing a connecting word. "hold up" is not defined. The Extensions section is a single sentence.
- **cash-in-transit:** "local Authority" has an odd capital. There are no exclusions, conditions or limits.
- **fidelity-guarantee:** "each of the employee". Otherwise clean.
- **all-risk-insurance:** the exclusions are one run-on paragraph. The hero image source is empty.
