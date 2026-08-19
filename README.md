# Portfolio site

One-page static site. No build step — edit `index.html` directly.

## Drop your files in

Create a `media/` folder next to `index.html` and add these. Anything missing shows a
labelled placeholder instead of a broken image, so you can deploy before you have all of them.

| File | What it should be |
|---|---|
| `media/tunabot-swim.mp4` | Short swim-test clip. Trim to 6–12s, no audio, loops silently. Keep under ~5 MB. |
| `media/tunabot-poster.jpg` | Single frame from that clip — shows before the video loads |
| `media/tunabot-build.jpg` | Platform on the bench, mid-assembly. Guts visible beats glamour shot. |
| `media/tunabot-cad.jpg` | SolidWorks screenshot of a subassembly |
| `media/mars.jpg` | MARS competition robot |
| `media/frc.jpg` | FRC competition robot |
| `media/allevion.jpg` | Optional — only if cleared. Otherwise delete that `.slot` block. |
| `resume.pdf` | Your résumé export, at the top level |

Compress photos before committing: resize to ~1600px on the long edge and save at ~80% JPEG
quality. Full-res phone photos will make the page slow on mobile.

## Deploy to GitHub Pages

1. Create a public repo named `vinaybhimavarapu.github.io` (swap in your GitHub username —
   the name has to match exactly for the root-domain URL to work).
2. Push `index.html`, `media/`, and `resume.pdf` to the `main` branch.
3. Repo → **Settings → Pages** → Source: *Deploy from a branch* → `main` / `/ (root)` → Save.
4. Live at `https://yourusername.github.io` in a minute or two.

### Custom domain (optional, ~$12/yr)

Buy `vinaybhimavarapu.com` from Cloudflare Registrar or Namecheap. In Settings → Pages, enter
it under Custom domain, then at your registrar add four `A` records for the apex pointing to
`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`, plus a `CNAME`
record for `www` → `yourusername.github.io`. Tick **Enforce HTTPS** once it validates.

## Editing notes

- All colors and fonts are CSS variables in the `:root` block at the top.
- To add a project, copy one `<article class="proj">` block. Alternate `class="proj"` and
  `class="proj flip"` to keep the media side switching.
- The `<dl class="readout">` strips only earn their space with real numbers. If a project has
  none, delete the strip rather than filling it with adjectives.
- The hero animation is the overlaid midline traces — the standard figure for showing a body
  wave travelling tail-ward. It freezes automatically under `prefers-reduced-motion`.
