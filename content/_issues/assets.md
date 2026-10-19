# Kenindia – brand & homepage assets

> Captured via WebFetch from https://kenindia.com/ (Firecrawl `images`/`branding` formats unavailable – free-tier rate limit hit; direct HTTP blocked). Colours/fonts could NOT be machine-extracted; see "Brand colours & fonts" for what to do.

## Logos
| URL | Notes |
|---|---|
| https://kenindia.com/wp-content/uploads/2023/11/KENINDIA-LOGO-1.webp | **Primary header logo** (used in header, mobile menu, footer). Largest/main variant available. No dimensions in filename. |
| https://kenindia.com/wp-content/uploads/2023/11/logo-e1700471114916.webp | WordPress-cropped logo (`-e<timestamp>` = edited copy); used as `msapplication-TileImage` / site icon. |

No SVG logo found. Ask Kenindia for vector (SVG/AI/EPS) master – WebP raster only on site.

## Favicon
- No `<link rel="icon">` / apple-touch-icon captured. Site icon appears to be the cropped logo: https://kenindia.com/wp-content/uploads/2023/11/logo-e1700471114916.webp (WordPress typically also serves `-32x32` / `-192x192` / `-180x180` derivatives of that file – unverified).

## Brand colours & fonts
- **Not detected** via this toolchain. Page meta generator shows: Elementor 4.3.2, `css_print_method-external`, `google_font-enabled`, `font_display-swap` → fonts are Google Fonts set in the Elementor Global Kit, and colours are `--e-global-color-*` vars in `/wp-content/uploads/elementor/css/post-<kitID>.css`.
- To get them: open the site in a browser → DevTools → `:root` computed styles (`--e-global-color-primary/secondary/text/accent`, `--e-global-typography-*-font-family`), or WP admin → Elementor → Site Settings → Global Colors / Global Fonts.
- Sample colours directly from KENINDIA-LOGO-1.webp as a fallback.

## Homepage images
| URL | What it shows |
|---|---|
| https://kenindia.com/wp-content/uploads/2023/11/KENINDIA-LOGO-1.webp | Logo |
| https://kenindia.com/wp-content/uploads/2025/11/img-2025-11-27-16-13-31-1024x926.png | Feature/hero image added Nov 2025 (screenshot-style filename; likely promo graphic) |
| https://kenindia.com/wp-content/uploads/2023/11/i4.webp | Section illustration (about/why-us block) |
| https://kenindia.com/wp-content/uploads/2023/11/etty-fidele-AzVexpHvuKY-unsplash-scaled.webp | Testimonial avatar – **Unsplash stock photo** |
| https://kenindia.com/wp-content/uploads/2023/11/freddy-kearney-o-ioeoATbIM-unsplash-scaled.webp | Testimonial avatar – **Unsplash stock photo** |
| https://kenindia.com/wp-content/uploads/2023/11/blank-profile-picture-973460_1280.webp | Testimonial avatar – **generic blank profile placeholder** |
| https://kenindia.com/wp-content/uploads/2025/11/assist.webp | Service icon/tile – Assistance |
| https://kenindia.com/wp-content/uploads/2023/11/claims.webp | Service icon/tile – Claims |
| https://kenindia.com/wp-content/uploads/2023/11/online.webp | Service icon/tile – Online/ePortal |
| https://kenindia.com/wp-content/uploads/2023/11/facebook.webp | Facebook / social block image |
| https://kenindia.com/wp-content/uploads/elementor/thumbs/iso-certification-badge-rgbyjundiv2c0sgw1bfkbt9oobm0tgsezadfu07pig.webp | ISO 9001:2015 certification badge |

Other banners seen on post pages (generic 1920x600 headers): https://kenindia.com/wp-content/uploads/2023/11/Untitled-1920-x-600-px.webp (and -1 … -4 variants). Group Life banner: https://kenindia.com/wp-content/uploads/2023/11/group-life-1-1-1024x320.jpg

## Video
- YouTube: https://www.youtube.com/watch?v=1MTkZPys7mU (embed: https://www.youtube.com/embed/1MTkZPys7mU; embedded with controls=0, autoplay off)

## ISO badge
- Text: "We are ISO 9001 2015 Certified" (should be "ISO 9001:2015")
- Image: https://kenindia.com/wp-content/uploads/elementor/thumbs/iso-certification-badge-rgbyjundiv2c0sgw1bfkbt9oobm0tgsezadfu07pig.webp (also inlined as base64 PNG). Elementor thumb – request original full-size badge / certificate from Kenindia.

## Social links
- X: https://x.com/KenindiaKE
- Facebook: https://www.facebook.com/KenindiaAssurance/
- Instagram: https://www.instagram.com/kenindiaassurance
- LinkedIn: **none found** anywhere on scraped pages
- YouTube channel: **none linked** (only the single embedded video above)
- TikTok: none

## Other brand/contact constants
- Phone: +254 111101000 / 600 (tel: link uses 0111101000)
- Address: Kenindia House, Loita Street, Nairobi
- Emails: Cloudflare-obfuscated in scraped HTML – obtain real addresses from Kenindia
- External: Job portal https://kenindiahr.peopleshr.com/jobportal · AKI https://www.akinsure.com/ · IRA https://www.ira.go.ke/
- Copyright: "© Copyright 2026 Kenindia Assurance Co Ltd. All rights reserved. Regulated by the Insurance Regulatory Authority"
