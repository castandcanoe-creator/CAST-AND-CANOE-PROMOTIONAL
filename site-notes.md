# Cast & Canoe™ — Press Kit Site (prototype)

This folder is the source of the future **CAST-AND-CANOE-PROMOTIONAL** site:
a one-page press / info kit for the game Cast & Canoe. It is a preparation
prototype only — it is **not deployed and not a public launch page yet**.

## Contents

- `index.html` — the single press-kit page (About, Fact Sheet, Features,
  The Lakes, Screenshots, Key Art, Links)
- `style.css` — all styling; warm field-paper look, self-contained
- `assets/andre-canoe.png` — key art (Andre fishing from a canoe at sunset).
  NOTE (2026-11-08): the PNG itself is NOT in this repo yet — the GitHub
  connector used for the initial push only handles text files, so the binary
  image could not be committed through it. Add it by uploading the file
  directly on github.com (repo → assets/ → Add file → Upload files) or via a
  local git push. Until then the Key Art <img> on the page will 404; the file
  lives locally at workspace/promo-prep/press-kit-site/assets/andre-canoe.png.

The page is pure static HTML/CSS: no build step, no framework, and no
external requests (system font stack only). Screenshot slots in the page are
clearly marked dashed placeholders; replace each slot with a real capture
(`<img>` in the same grid) when the screenshot library is ready.

## Deploy (when launch prep is approved)

This site is designed to be deployed to **Cloudflare Pages connected to the
CAST-AND-CANOE-PROMOTIONAL GitHub repo**:

1. Copy/commit these files to the root of the `CAST-AND-CANOE-PROMOTIONAL`
   repo (so `index.html` sits at the repo root).
2. In Cloudflare: Workers & Pages → Create → Pages → Connect to Git →
   select `CAST-AND-CANOE-PROMOTIONAL`.
3. Build settings:
   - **Build command:** none (leave empty)
   - **Build output directory:** the site root (`/`)
   - Framework preset: None
4. Deploy. The site is served as-is; every later push to the repo's main
   branch redeploys automatically.

Do not announce or link the resulting `*.pages.dev` address publicly until
the launch plan says so.
