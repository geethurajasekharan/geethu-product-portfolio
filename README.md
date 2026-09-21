# Geethu Rajasekharan — Product Portfolio

Static site. No build step, no dependencies. Deploy the contents of this folder as-is.

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
    image-slots.state.json        Images dropped into placeholders
    assets/                       Portrait, TiVo video poster
    uploads/                      Promo videos
    netlify.toml                  Netlify config (publish root, no build)

## Deploy

**Netlify** — see the step-by-step below.

**Vercel** — import the repo, framework preset "Other", no build command, root directory `site`.

**GitHub Pages** — Settings → Pages → deploy from branch `main`, folder `/site`.

## Notes

- Fonts load from Google Fonts at runtime; everything else is local.
- The TiVo hero shows a poster image; clicking Play loads the Google Drive player. The Drive file must be shared "anyone with the link".
- Images dropped onto placeholders live in `image-slots.state.json`. Replacing them requires re-exporting from the design project.
