# K-Wire Network

A directory site for a small, growing family of independent, unofficial English-language K-pop fan wires. This repo is special: named exactly `fhzl0117-hue.github.io`, so GitHub Pages serves it at the account's root domain instead of a `/repo-name/` subpath — making it the natural front door for every other "Wire" site under this account.

**Not affiliated with, endorsed by, or sponsored by HYBE, BIGHIT MUSIC, YG Entertainment, THEBLACKLABEL, Odd Atelier, Warner Records, LLOUD, JYP Entertainment, or any artist linked from this page.**

## What's in this repo

A single static page — `index.html` — with everything (HTML, CSS) inlined. No build step, no dependencies, no backend. It links out to:

- [Bangtan Wire](https://fhzl0117-hue.github.io/bangtan-wire/)
- [Blackpink Wire](https://fhzl0117-hue.github.io/blackpink-wire/) (plus its four member desks: Jennie, Jisoo, Rosé, Lisa)
- [Stray Kids Wire](https://fhzl0117-hue.github.io/stray-kids-wire/)

## Adding a new site to the directory (fully automatic)

This page no longer needs to be hand-edited when a new site or a new member solo desk launches. `index.html` includes a small inline script that, on every page load, calls the GitHub API to list every repo under this account whose name ends in `-wire`, then fetches each repo's `manifest.json`. Any repo not yet shown gets a new card appended automatically; any repo already shown has its solo-desk sub-links merged in from its manifest. There's no build step, no scheduled job, and nothing to commit here — a visitor's browser does the discovery live.

To make a new site (or a new member subpage) show up:

1. **New group site** (e.g. a repo named `some-group-wire`): add a `manifest.json` to that repo's root:
   ```json
   {
     "name": "Some Group Wire",
     "description": "One-line description of the site.",
     "tag": "Group / Fandom",
     "accent": "#RRGGBB",
     "accentTint": "#RRGGBB",
     "url": "https://fhzl0117-hue.github.io/some-group-wire/",
     "eyebrow": "Est. 2026",
     "members": []
   }
   ```
   It'll appear as a new card here automatically — no edits needed on this repo.

2. **New member solo subpage inside an existing site** (e.g. a new member page in `blackpink-wire`): add an entry to that repo's `manifest.json` `members` array:
   ```json
   { "name": "Member Name", "url": "https://fhzl0117-hue.github.io/blackpink-wire/member.html" }
   ```
   It'll be merged into that site's existing card's "Solo desks" line automatically.

If the GitHub API call fails (rate limit, offline, etc.), the page silently keeps the static fallback cards already baked into `index.html` — visitors never see a broken directory. It's still worth periodically syncing the static fallback cards in `index.html` to match the manifests, so the page looks right even before the script runs (e.g. slow connections, JS disabled). Update `sitemap.xml` only if this page's own URL structure changes — new site cards don't require a sitemap change here since they live on their own domains' sitemaps.

## Deploying with GitHub Pages

1. Push this repo to GitHub (or upload these files through the GitHub web UI) under the exact name `fhzl0117-hue.github.io`.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch," branch `main`, folder `/ (root)`.
4. Save. GitHub will publish the site at `https://fhzl0117-hue.github.io/` within a minute or two — this is the account's root domain, not a project subpath.

## License / ownership

Internal company project. Not licensed for redistribution outside the team without checking with whoever owns this repo.
