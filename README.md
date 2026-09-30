# spex.bet

Landing site for the Spex family of Kalshi sports-position tools. `/` is the brand page, `/glance/` is [Spex Glance](https://github.com/davidmarcantonio/spex-glance) (macOS). Future apps get their own folder (`/board/`, `/ios/`).

Static HTML, no build step, hosted on GitHub Pages at https://spex.bet.

## Layout

| File | Purpose |
|---|---|
| `index.html` | Spex brand landing (app cards) |
| `glance/index.html` | Spex Glance product page |
| `assets/site.css` | Shared styles |
| `privacy.html` | Privacy note |
| `404.html` | Not-found page |
| `assets/app-icon.png` | App icon, used for logo and favicon |
| `assets/og.png` | Social share image (1200×630) — **add before launch** |
| `CNAME` | Custom domain for GitHub Pages |
| `robots.txt`, `sitemap.xml` | Search engine hints |
| `.nojekyll` | Tells Pages to serve files as-is |

## Editing

Edit the HTML directly and push to `main`. The `Deploy spex.bet` workflow builds and deploys Pages (source: GitHub Actions, not branch).

## Version stamping

The workflow looks up the latest `spex-glance` release and writes it into every `<span data-version>` and the `softwareVersion` schema field before deploying. It runs on push, daily, on demand, and on a `repository_dispatch` with `event_type: release`. To trigger it from `release.sh --publish`:

```sh
gh api repos/davidmarcantonio/spex.bets/dispatches -f event_type=release
```

The committed HTML carries whatever version was current at the last edit; the deployed site always carries the latest release.

## To do before launch

- [x] Real screenshots (assets/screenshot-*.png, screenshot-menubar.png, captured 2026-09-29)
- [x] `assets/og.png` (1200×630) for link previews
- [x] Space Grotesk self-hosted in `assets/fonts/` (OFL), no Google Fonts call
- [ ] Confirm the release URL once `spex-glance` has a tagged release

Not affiliated with Kalshi.
