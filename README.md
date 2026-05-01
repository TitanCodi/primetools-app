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
| `vercel.json` | Vercel deployment config (headers, redirects, clean URLs) |

## Deploy to GitHub + Vercel

### 1. Push to GitHub

```bash
git init
git add .
git commit -m "Initial commit: PrimeTools.app hub"
git remote add origin https://github.com/YOUR_USERNAME/primetools-app.git
git push -u origin main
```

### 2. Deploy on Vercel

1. Go to [vercel.com](https://vercel.com) → **Add New Project**
2. Import your GitHub repo
3. **Framework Preset**: Other (static site — no build step needed)
4. **Build Command**: *(leave blank)*
5. **Output Directory**: `.` (root)
6. Click **Deploy**

### 3. Add Custom Domain

In Vercel project → **Settings → Domains** → add `primetools.app`

Follow Vercel's DNS instructions (typically add an A record + CNAME to your domain registrar).

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
