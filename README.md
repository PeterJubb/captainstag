# Peter Jubb — Portfolio

A focused, single-page portfolio with six case studies. Static HTML/CSS/JS — no build step, no framework, no dependencies.

## Files

```
index.html              Main portfolio (single page)
case-playnow.html       Case file 001 — PlayNow.com
case-keno.html          Case file 002 — Keno
case-terminal.html      Case file 003 — Lottery Retail Terminal
case-lastknown.html     Case file 004 — LastKnown NFT marketplace
case-nike-acg.html      Case file 005 — Nike ACG (archival)
case-nintendo.html      Case file 006 — Nintendo Europe (archival)
404.html                Custom not-found page
styles.css              Shared design system
netlify.toml            Netlify config (caching, headers, redirects)
assets/
  images/               Project imagery
  PeterJubb_CV.pdf      Résumé download
```

## Deploy to Netlify (3 ways, easiest first)

### Option A — Drag & Drop (fastest, no Git needed)

1. Zip up this folder (or just the contents — Netlify takes either)
2. Go to <https://app.netlify.com/drop>
3. Drag the folder/zip onto the page
4. Netlify gives you a live URL in about 10 seconds, e.g. `random-name-12345.netlify.app`
5. In **Site settings → Domain management → Site name**, change the subdomain to something like `peterjubb.netlify.app`

### Option B — Git-connected deploy (recommended for ongoing edits)

1. Push this folder to a GitHub/GitLab/Bitbucket repo
2. <https://app.netlify.com/start> → "Import from Git" → select the repo
3. **Build settings:**
   - Build command: *(leave blank)*
   - Publish directory: `.` (or wherever `index.html` lives)
4. Click Deploy. Every push to `main` redeploys automatically.

### Option C — Netlify CLI (for power users)

```bash
npm install -g netlify-cli
cd /path/to/this/folder
netlify deploy            # preview
netlify deploy --prod     # live
```

## Custom domain

Once deployed, **Site settings → Domain management → Add custom domain** — Netlify walks you through the DNS step. Free SSL certificate, automatic.

## Local preview before deploying

Any of these from inside the project folder:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

```bash
npx serve .
```

## Editing notes

- All six case studies share `styles.css`. Update once, applies everywhere.
- The `[001]`, `[002]` etc. are just text — change them in the HTML directly.
- Live PST clock + scroll-reveal are inline scripts at the bottom of `index.html`. No build step.
- Images are cached for a year via `netlify.toml` — if you replace one, give it a new filename or version-stamp it.

## Fonts

Loaded from Google Fonts at the top of `styles.css`:
- **Fraunces** — display headlines (italic capable)
- **Geist** — body / UI sans
- **JetBrains Mono** — metadata, system chrome

To self-host them later, download the woff2 files from <https://fonts.google.com> and replace the `@import` line with `@font-face` blocks.

---

© Peter Jubb · hand-coded in Vancouver.
