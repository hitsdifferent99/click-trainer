# Click Trainer — Victoria Drums

A smart click track trainer for drummers. Practice with moving tempos, build song maps and memorise where tempo changes happen before they hit.

## Features

- 5 tempo modes: Fixed, Ramp, Build to target, Wind down, Wave
- Song map builder — label sections (Intro, Verse, Pre-chorus, Chorus, Bridge, Outro) with their tempos and direction
- Colour-coded beat dots and flash ring — green = speeding up, amber = steady, red = slowing down
- Tap tempo
- Subdivisions: quarter, 8th, triplet, 16th
- Time signatures: 2/4, 3/4, 4/4, 5/4, 6/8, 7/4
- Works offline as a PWA — installable on phone home screen

## Deploy to Vercel

### Option 1 — Vercel CLI (fastest)

```bash
npm i -g vercel
vercel
```

Follow the prompts. Done.

### Option 2 — GitHub + Vercel dashboard

1. Create a new GitHub repo and push this folder
2. Go to vercel.com → New Project → import the repo
3. No build step needed — framework preset: Other
4. Deploy

### Option 3 — Custom domain (click.victoriadrums.uk)

After deploying on Vercel:
1. Vercel dashboard → your project → Settings → Domains
2. Add `click.victoriadrums.uk`
3. In your DNS provider, add a CNAME record:
   - Name: `click`
   - Value: `cname.vercel-dns.com`
4. SSL is automatic

## PWA icons

Add two icon files to an `/icons/` folder:
- `icon-192.png` — 192×192px
- `icon-512.png` — 512×512px

Use your Victoria Drums logo. Without these, the app still works but won't have a custom icon when installed.

## Files

```
index.html    — the whole app (single file, no dependencies)
manifest.json — PWA metadata
sw.js         — service worker for offline support
vercel.json   — headers config
```

No npm, no build step, no dependencies. Pure HTML/CSS/JS.
