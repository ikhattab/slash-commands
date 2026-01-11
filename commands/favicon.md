---
id: favicon
name: Generate Favicons
slug: favicon
category: code-quality
description: Generate favicons from a source image
argument-hint: "[path to source image]"
---

Generate favicons from the source image at `$1`.

## Prerequisites

Run `which magick` to verify ImageMagick v7+ is installed. If missing: `brew install imagemagick` (macOS) or `sudo apt install imagemagick` (Linux).

## Steps

1. **Validate**: Confirm `$1` exists and is PNG/JPG/SVG/WEBP/GIF. Note if SVG (copy as `favicon.svg` later).

2. **Find static dir**: Check for existing favicon files first. Otherwise detect framework:

   - Rails (`config/routes.rb`), Next.js, Astro, Vite, CRA, Vue CLI → `public/`
   - Gatsby, SvelteKit, Hugo → `static/`
   - Angular → `src/assets/`
   - Static HTML → same dir as `index.html`

3. **Get app name**: From existing `site.webmanifest`, `package.json`, or directory name. Title-case it.

4. **Generate files** (replace `[DIR]` with static dir):

```bash
magick "$1" \( -clone 0 -resize 16x16 \) \( -clone 0 -resize 32x32 \) \( -clone 0 -resize 48x48 \) -delete 0 -alpha on -background none [DIR]/favicon.ico
magick "$1" -resize 96x96 -background none -alpha on [DIR]/favicon-96x96.png
magick "$1" -resize 180x180 -background none -alpha on [DIR]/apple-touch-icon.png
magick "$1" -resize 192x192 -background none -alpha on [DIR]/web-app-manifest-192x192.png
magick "$1" -resize 512x512 -background none -alpha on [DIR]/web-app-manifest-512x512.png
```

If source is SVG: `cp "$1" [DIR]/favicon.svg`

5. **Create/update `site.webmanifest`** with app name and icon paths. Preserve existing `theme_color`/`background_color`/`display` if updating.

6. **Update HTML `<head>`** (omit svg line if source wasn't SVG):

```html
<link rel="icon" type="image/png" href="/favicon-96x96.png" sizes="96x96" />
<link rel="icon" type="image/svg+xml" href="/favicon.svg" />
<link rel="shortcut icon" href="/favicon.ico" />
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png" />
<meta name="apple-mobile-web-app-title" content="[APP_NAME]" />
<link rel="manifest" href="/site.webmanifest" />
```

For Next.js, update `metadata.icons` in layout file instead.

7. **Report**: project type, static dir, files generated, app name used, files overwritten.
