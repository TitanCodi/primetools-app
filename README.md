# PrimeTools.app — Hub Landing Page

Landing page and portal hub for [PrimeTools.app](https://primetools.app), linking to three specialized tool sites.

## Files

| File | Purpose |
|------|---------|
| `index.html` | Main hub landing page |
| `privacy.html` | Privacy Policy |
| `terms.html` | Terms of Use |
| `sitemap.xml` | XML sitemap for SEO |
| `robots.txt` | Search engine crawl directives |
| `404.html` | Custom 404 page (noindex, no ads), served by Cloudflare Pages for unknown URLs |
| `_headers` | Cloudflare Pages response headers (X-Frame-Options, Permissions-Policy, HSTS) |
| `_redirects` | Cloudflare Pages path redirects (/home → /) |

## Deployment

- Hosted on Cloudflare Pages, project `primetools-app`, connected to GitHub `TitanCodi/primetools-app` and auto-deploying from `main`.
- Domains (`primetools.app`, `www.primetools.app`) are managed in Cloudflare.
- Workflow: branch off `main`, push, open a PR, check the preview at `<branch-with-dashes>.primetools-app.pages.dev`, merge, and production redeploys.
- No build step: the repo root is served as-is.

## AdSense Setup

Ad slots are already wired with publisher ID `ca-pub-2548921396153742`. Replace the placeholder `data-ad-slot` values with your real ad unit IDs from the AdSense dashboard:

- **Leaderboard** (728×90): Search for `data-ad-slot="1234567890"` → replace with your slot ID
- **Rectangle** (300×250): Search for `data-ad-slot="0987654321"` → replace with your slot ID  
- **Banner bottom** (728×90): Search for `data-ad-slot="1122334455"` → replace with your slot ID

## SEO Checklist

- [x] Title tag & meta description
- [x] Open Graph tags (og:title, og:description, og:image, og:url)
- [x] Twitter Card tags
- [x] Schema.org WebSite structured data
- [x] Canonical URL
- [x] robots.txt
- [x] sitemap.xml
- [x] Semantic HTML (h1 → h2 hierarchy)
- [ ] Add real `og-image.png` (1200×630px) to repo root
- [ ] Update `sitemap.xml` lastmod dates when content changes
- [ ] Submit sitemap in Google Search Console

## Updating the Sitemap Date

After content changes, update `<lastmod>` in `sitemap.xml`:

```xml
<lastmod>2025-06-01</lastmod>
```

## Local Preview

```bash
npx serve .
# or
python3 -m http.server 3000
```
