# Geethu Rajasekharan — Product Portfolio

Static site. No build step, no dependencies. All paths are relative — deploy the contents of this folder as-is.

## Structure

    index.html                    Home (about, products, contact)
    pages/bragsheet.html          Bragsheet case study
    pages/attuned-ai.html         Attuned AI case study
    pages/my-health-node-ai.html  My Health Node AI case study
    pages/naamaa-platform.html    Naamaa Platform case study
    pages/via-agent.html          VIA Agent case study
    pages/tivo-iptv.html          TiVo Managed IPTV case study
    support.js                    Component runtime (required by every page)
    image-slot.js                 Image placeholder component
    image-slots.state.json        Image manifest for index.html
    pages/image-slots.state.json  Image manifest for the case-study pages
    assets/portrait.png           Portrait
    assets/slots/                 All case-study and product-tile images (webp)
    uploads/                      NOT in this zip — add the promo videos yourself:
                                  bragsheet-pitch.mp4, rudra.mp4,
                                  via-agent-demo.mp4, tivo-sizzle.mp4
    netlify.toml                  Netlify config (publish root, no build)

## Run locally

Images load via `fetch`, which browsers block on `file://`. Use a local server:

    python3 -m http.server 8000

Then open http://localhost:8000

## Deploy

**Netlify** — Add new site → Import an existing project → GitHub → pick the repo.
Build command: leave empty. Publish directory: `.` (or `site` if you keep these
files in a `site/` subfolder). Every push to `main` redeploys.

**Vercel** — import the repo, framework preset "Other", no build command. Root
directory: repo root (or `site` if nested).

**GitHub Pages** — Settings → Pages → deploy from branch `main`, folder `/`
(or `/site` if nested).

## Notes

- Fonts load from Google Fonts at runtime; everything else is local.
- The TiVo hero is a muted-autoplay `<video>` with an Unmute pill, sourced from
  `uploads/tivo-sizzle.mp4`. If that file is missing the hero falls back to a
  placeholder after 8 seconds.
- To replace an image, swap the matching file in `assets/slots/` (keep the name).
