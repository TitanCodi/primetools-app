# Changelog
All notable changes to PrimeTools.app will be documented here.

## [1.5.0] - 2026-10-13

### Changed
- "Why PrimeTools" cards show 4 across on desktop (they wrapped
  3 + 1 at 1024px); 2×2 at 768px and 1 column at 480px as
  before (#6)

### Removed
- Three hidden placeholder ad units (fake slot IDs) and their
  `push()` calls, which logged console errors on every visit.
  The AdSense loader stays; real units come after approval (#6)
- Unused `.ad-slot` CSS (#6)

## [1.4.0] - 2026-10-13

### Added
- Contact email (`hello@primetools.app`) on the Privacy and Terms
  pages, replacing "contact us through our website" (#5)

### Changed
- Homepage title shortened to 57 characters; `og:title` and
  `twitter:title` now match it (#5)
- `og:description` and `twitter:description` unified at 108
  characters (#5)
- Lastmod bumped for `/privacy` and `/terms` (#5)
- README: four tool sites (it said three); sitemap submission
  ticked (#5)

### Fixed
- Footer CSS comment now describes the actual grid (#5)

## [1.3.0] - 2026-10-11

### Added
- `favicon-32.png`, `apple-touch-icon.png` (180×180) and
  `favicon.ico` (16+32), generated from `favicon.svg`, plus a
  1200×630 `og-image.png` (#3)
- Icon links on every page, including `404.html`, with
  root-absolute paths (#3)
- `og:image:width`, `og:image:height`, `og:image:alt` and
  `twitter:image:alt` on the homepage (#3)

### Changed
- README updated for the new assets (#3)

### Fixed
- Icons and the share image referenced in page heads now exist.
  The soft 404 had served them as HTML with a 200, and they
  returned 404 once the real 404 page shipped (#3)

## [1.2.0] - 2026-10-11

### Added
- `404.html`: real 404 status for unknown URLs, `noindex`, no
  canonical, no AdSense (#2)
- `_headers`: X-Frame-Options DENY, Permissions-Policy and HSTS
  (`max-age=31536000; includeSubDomains`, no preload) (#2)
- `_redirects`: `/home` → `/` 301 (#2)
- Cloudflare zone Redirect Rule: www → apex, 301, query string
  preserved (dashboard change, no PR)

### Changed
- README describes Cloudflare Pages hosting instead of Vercel (#2)

### Fixed
- Unknown URLs no longer return the homepage with a 200
  (soft 404) (#2)

### Removed
- `vercel.json`, which Cloudflare Pages ignores (#2)

## [1.1.0] - 2026-10-11

### Changed
- Network links cut from 31, all followed, to 16, with one
  followed brand-name link per tool site (its tool card). Header
  nav and footer "Tool Sites" links are `nofollow` (#1)
- Hero chips scroll to the matching tool card instead of leaving
  the site; the label is now "Pick your goal to see the right
  tools" (#1)
- One "Explore tools" button jumps to `#tools`, replacing the
  four-button closing CTA (#1)
- Lastmod bumped for `/` (#1)

### Removed
- Footer "Calculators" column (#1)

## [1.0.0] - 2026-10-10

### Changed
- Site source moved to a local clone of `TitanCodi/primetools-app`.
  All edits now go through branches and pull requests. Production
  at this point: `27c2a29`
- Earlier versions (May–August 2026) were uploaded through the
  GitHub website and are not itemized here
