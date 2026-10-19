# Issues found – news posts & extra pages

## CRITICAL
1. **Injected spam on /want-to-be-an-agent/** – the live post contains French-language paragraphs promoting online casino bonuses with an outbound casino link (post modified 2025-12-12 per sitemap). Classic WordPress SEO-spam injection → tell Kenindia to treat as a possible site compromise: remove content, audit users/plugins, change passwords, check other posts. NOT migrated.
2. **Extraction limitation** – Firecrawl free tier was rate-limited on first call and direct HTTP to kenindia.com is blocked from this environment; WebFetch refuses to output verbatim text. All news/extra bodies are **close paraphrases** (flagged `verbatim: false` in frontmatter) except IIK Golf, Want-to-be-an-Agent requirements, and Performance Trends which came back near-verbatim. Exact copy should be exported from WP admin (Tools > Export) before launch. Brand colours/fonts not extracted.

## Outdated content
- **kenindia-magazine-volume-6** – refers to ISO prep "into 2016"; ~10 years old. Archive.
- **kenindia-perfomance-trends** – pension rate chart 2000–2018 only. Archive or update.
- **want-to-be-an-agent** – old landline numbers "2248719 or 316099 extensions 280" (pre-0111101000 numbering); "C.O.P." undefined.
- **what-is-travel-insurance…** – 2023 republished interview; Subhash Deshkulkarni's title/role and "only insurer offering Schengen" claim need re-verification.
- **meet-our-team** (Nov 2023) contradicts 2025 posts: Irene Owiti is COO in posts but "DGM Marketing" there; COO listed as J Macharia. Use /management-team/.
- News Room listing appears to show only `blog` category – CSR posts (Mar/Apr 2026) missing from it.
- Featured image for 2023 posts are generic "Untitled-1920-x-600-px" banners.

## Broken / duplicate / empty pages & links
- `/croup-life-cover/` typo slug used in Group Life "View Related Products"; canonical is `/group-life-cover/`. Similarly `/croup-personal-accident/` (live canonical slug itself has the typo – redirect to `/group-personal-accident/` in rebuild).
- `/about-us/` duplicates `/about/` (footer-only). `/news-media/` empty (superseded by `/news-room/`). `/brochures/` empty. `/individual-pension-plan/` H1 only – but linked from Group Life related products.
- Many nav items link to `#`: Downloads, Forms, Proposal Forms, Claim Forms, Life General, Individual, Corporate, Kenindia Medical, Life Insurance, General Insurance; "Insurance" is `/insurance-page/` in one menu and `#` in another; "Downloads" vs "Forms" labelling inconsistent; "EPortal" vs "ePortal".
- "Learn More" CTA → `/about` (no trailing slash; fine but inconsistent).
- Phone shown as "+254 111101000 / 600" but tel: link is 0111101000.
- Emails are Cloudflare-obfuscated – get real addresses.

## Typos (by page)
- **Akuisi water post**: title/slug "Solutionsat" → "Solutions at"; "kitchen garden ," stray space; "Akuisi comprehensive school" capitalisation; location given as both Akuisi and "Bahati in Rongai, Nakuru County".
- **Walking for Hope**: "Getrudes Hospital Foundation" → likely "Gertrude's Children's Hospital Foundation" (verify).
- **Coastal Success**: "Irene Owiti ," stray space; division/name list punctuation garbled.
- **Customer Service Week**: "customers,have" missing space; hashtags lowercase with spaces ("#happy customer service week 2025").
- **IIK Golf**: "Stable ford" → "Stableford".
- **Performance Trends**: "Perfomance" (title + slug); "Below is graphical representation" → "a graphical"; "over year 2000 to 2018"; lowercase "kenindia".
- **Life Insurance guide**: "ask answer a few key questions"; "Whole Life policies in Kenyan".
- **Travel insurance**: "overlook return of mortal remains"; "hi-jacking"; "Are there any exclusion?"; "1-180days"; "Youths"; traveler/traveller mixed.
- **Magazine Vol 6**: PDF ligature breaks "certifi cation", "offi ces", "fl urry", "fi re drills", "Certifi ed"; "MagazineTeam".
- **Women's Day / Call for Love**: comma splices; hard line breaks mid-sentence; event date "25th March" without year; double space in "Company  Limited".
- **Group Life Cover**: "Phillips Pharmaceauticals"; "tax relieve"; "Compliment" → "complement"; "incase" ×2; "payable the Company"; "Eligibility start from 18 – 65 years"; "Next birth day"; exclusions 2 & 4 overlap.
- **Meet Our Team**: "Dr Manu" vs "Dr." inconsistency; "Hemnabh Khatau" spelling to verify; management names initials only.
- **Job Application**: experience options skip "2" (Less than 2, 3, 4, 5…) and lack "years"; awkward intro sentence.
- **Site-wide**: brand written "KenIndia", "Kenindia", "Kenindia Assurance Co Ltd", "Kenindia Assurance Company Limited"; "ISO 9001 2015" → "ISO 9001:2015".

## Placeholder / quality
- Homepage testimonials use Unsplash stock photos and a "blank-profile-picture" placeholder avatar.
- All news gallery images have empty alt text.
- Image filenames are raw camera/WhatsApp names (e.g. WhatsApp-Image-2025-10-07-at-16.10.12_21f81eea.jpg) – rename on migration.
- Some posts lack author (Customer Service Week, Yoga Day, Golf, Water, all 2023 posts); author "Nuru" vs "Nuru Abubakar".
- Newsletter form ("Subscribe … for discounts and more") – check it actually submits somewhere.
