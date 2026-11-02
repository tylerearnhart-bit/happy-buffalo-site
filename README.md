# gohappybuffalo.com — holding page

The Happy Buffalo coming-soon page. Plain HTML, no build step, no dependencies.
Deployed by Cloudflare Pages: push to `main` and the live site updates.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole page. Fonts, logo and artwork are embedded in it. |
| `social-1200x630.png` | The preview image for shared links |
| `favicon.ico` | Browser tab icon |
| `apple-touch-icon.png` | Icon when saved to a phone home screen |
| `_headers` | Cloudflare Pages caching and security headers |

## Editing the page

Open `index.html` in any text editor. The copy lives near the bottom, in plain
HTML — search for the phrase you want to change.

| Bit | Find this |
|---|---|
| Greeting | `class="eyebrow"` |
| Headline | `<h1>` — the amber half is the `<em>` |
| Paragraph | `class="sub"` |
| Buttons / email | `mailto:hello@gohappybuffalo.com` (two places) |
| Footer line | `class="footnote"` |

Save, commit, push. Cloudflare rebuilds in under a minute.

The styling is in the `<style>` block in the head. Brand colours are the custom
properties at the top of it:

```css
--cream: #F7F1E6;   --rust:  #A75430;
--amber: #E8A33D;   --brown: #1B1815;
```

## Deploying

Cloudflare Pages watches this repo. Every push to `main` deploys automatically.
Pushes to other branches get their own preview URL, which is a safe way to check
a change before it goes live.

Setup instructions are in `DEPLOY-CLOUDFLARE.md` in the download this came from.

## Gotchas

- The home page must stay named `index.html`.
- `index.html` has no external requests — everything is inlined as data URIs.
  That's deliberate: nothing to break, one file to serve, very fast.
- The share-preview tags point at `https://gohappybuffalo.com/`. If the live
  address changes, search `index.html` for that domain and replace it.
