# K-Wire Network

A directory site for a small, growing family of independent, unofficial English-language K-pop fan wires. This repo is special: named exactly `fhzl0117-hue.github.io`, so GitHub Pages serves it at the account's root domain instead of a `/repo-name/` subpath — making it the natural front door for every other "Wire" site under this account.

**Not affiliated with, endorsed by, or sponsored by HYBE, BIGHIT MUSIC, YG Entertainment, THEBLACKLABEL, Odd Atelier, Warner Records, LLOUD, JYP Entertainment, or any artist linked from this page.**

## What's in this repo

A single static page — `index.html` — with everything (HTML, CSS) inlined. No build step, no dependencies, no backend. It links out to:

- [Bangtan Wire](https://fhzl0117-hue.github.io/bangtan-wire/)
- [Blackpink Wire](https://fhzl0117-hue.github.io/blackpink-wire/) (plus its four member desks: Jennie, Jisoo, Rosé, Lisa)
- [Stray Kids Wire](https://fhzl0117-hue.github.io/stray-kids-wire/)

## Adding a new site to the directory

When a new "Wire" site launches, add a new `.site-card` block inside `#directory` in `index.html`, following the existing markup pattern (bar color, eyebrow, name, one-line description, tag, link, optional sub-links). Keep the accent color consistent with that site's own primary color for quick visual recognition. Update `sitemap.xml` if the new addition changes this page's content meaningfully.

## Deploying with GitHub Pages

1. Push this repo to GitHub (or upload these files through the GitHub web UI) under the exact name `fhzl0117-hue.github.io`.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch," branch `main`, folder `/ (root)`.
4. Save. GitHub will publish the site at `https://fhzl0117-hue.github.io/` within a minute or two — this is the account's root domain, not a project subpath.

## License / ownership

Internal company project. Not licensed for redistribution outside the team without checking with whoever owns this repo.
