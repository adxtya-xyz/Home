# adxtya.xyz

The off-script half of Aditya Nair. Side quests across mind, body, build and road.

A single static page, no build step. Everything you edit lives in one block at the top of the `<script>` in `index.html`.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The site |
| `404.html` | "Off the grid" page for broken links (GitHub Pages serves it automatically) |
| `favicon.ico`, `favicon.svg`, `favicon-16x16.png`, `favicon-32x32.png` | Browser tab icons |
| `apple-touch-icon.png` | iPhone home-screen icon |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | Android / install icons |
| `site.webmanifest` | Lets the site be added to a home screen like an app |
| `og.jpg` | Preview image when the link is shared (WhatsApp, LinkedIn, X, iMessage) |
| `robots.txt`, `sitemap.xml` | Search engine hints |
| `CNAME` | Tells GitHub Pages to serve the site at adxtya.xyz |
| `.nojekyll` | Stops GitHub from processing the files with Jekyll |

## Deploy on GitHub Pages

1. Create a repository (for example `adxtya.xyz`) and upload every file in this folder to the root, including `.nojekyll` and `CNAME`.
2. Repository **Settings → Pages**: Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`. Save.
3. At your domain registrar, add these DNS records for `adxtya.xyz`:
   - Four `A` records for `@` pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One `CNAME` record for `www` pointing to `<your-github-username>.github.io`
4. Back in **Settings → Pages**, confirm the custom domain shows `adxtya.xyz`. Once the DNS check passes (minutes to a few hours), tick **Enforce HTTPS**.

## Updating content

Open `index.html` and edit the block under `CONTENT: edit these to update the site.`

- `QUESTS`: projects. `pillar` is `mind`, `body`, `build` or `road`. `stage` is 0 Idea, 1 In progress, 2 Beta, 3 Live. `wide: true` makes a double-width tile (keep it to three). Add a `url` when a project goes live.
- `NOW` and `NOW_UPDATED`: the "Right now" status board.
- `NOTES`: travel stories (a commented example is included).
- `RACE`, `PLAN_WEEKS`, `PHASES`: the training countdown and week strip.

Commit, and GitHub Pages republishes in about a minute.

## Notes

- `og.jpg` is referenced by its full URL (`https://adxtya.xyz/og.jpg`), so share previews only work once the custom domain is live. To refresh a cached preview on LinkedIn, use their Post Inspector.
- After changing `favicon.*`, browsers can hold the old icon for a while; a hard refresh or private window shows the new one.
