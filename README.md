# yanirtadmor.com

Personal site for Yanir Tadmor: marketer, content creator and author of *זיכרונות מהקיר המתקלף* (Memories from the Peeling Wall).

Static site, no framework, no build step required on Vercel. Everything in this folder is served as-is.

## Structure

- `index.html` – Hebrew (default, RTL)
- `en/index.html` – English (LTR)
- `img/` – portrait, book cover, Open Graph images
- `favicon.svg`, `favicon.ico`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`, `site.webmanifest` – icon set
- `sitemap.xml`, `robots.txt` – search engines
- `yanir-tadmor.vcf` – "Save contact" card
- `vercel.json` – clean URLs, trailing slashes, caching and security headers

## Deploy on Vercel

1. Push this folder to a GitHub repository (the folder contents are the repo root).
2. In Vercel: **Add New Project → Import** the repo. Framework preset: **Other**. Leave build command and output directory empty.
3. Add the domain `yanirtadmor.com` (and `www.yanirtadmor.com`, redirecting to the apex) under **Settings → Domains**, then point the DNS where Vercel tells you.
4. After the first deploy, add the site in Google Search Console and submit `https://yanirtadmor.com/sitemap.xml`.

## Editing content

Both pages are generated from one bilingual template by `build.py` (kept in the parent folder of this repo, not deployed).
To add a press item, edit the `press` array in the template and run `python3 build.py`; it rewrites both pages,
the sitemap and the OG images. If you prefer to edit by hand, the same card markup appears in both
`index.html` and `en/index.html`, and the `press` array in the inline script must be updated too so the filters stay in sync.

## Contact details used

- Email: yanirtad@gmail.com
- WhatsApp: +972 50-922-2640
- Book: https://nivbook.co.il/product/%D7%96%D7%99%D7%9B%D7%A8%D7%95%D7%A0%D7%95%D7%AA-%D7%9E%D7%94%D7%A7%D7%99%D7%A8-%D7%94%D7%9E%D7%AA%D7%A7%D7%9C%D7%A3/
