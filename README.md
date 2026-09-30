# spex.bets

Marketing site for [Spex Glance](https://github.com/davidmarcantonio/spex-glance), a free, open-source macOS app that shows your active Kalshi sports positions in one window and from the menu bar.

Static HTML, no build step, hosted on GitHub Pages at https://spex.bets.

## Layout

| File | Purpose |
|---|---|
| `index.html` | Landing page (single file, inline CSS, SEO meta + JSON-LD) |
| `privacy.html` | Privacy note |
| `404.html` | Not-found page |
| `assets/spex-mark.svg` | Logo / favicon |
| `assets/og.png` | Social share image (1200×630) — **add before launch** |
| `CNAME` | Custom domain for GitHub Pages |
| `robots.txt`, `sitemap.xml` | Search engine hints |
| `.nojekyll` | Tells Pages to serve files as-is |

## Editing

Edit the HTML directly and push to `main`. Pages redeploys in about a minute.

## To do before launch

- [ ] Replace the illustrative window mock with real screenshots once the first release ships
- [ ] Add `assets/og.png` (1200×630) for link previews
- [ ] Confirm the release URL once `spex-glance` has a tagged release

Not affiliated with Kalshi.
