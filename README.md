# Banglalink × Horizon — bKash Deal Room entry point

A static mobile-web prototype. The Banglalink screen is a fixed static
background (the "empty" demo image); a single **Horizon** entry point
(`HORIZON_ENTRY_1`, code `#377585`) is overlaid on the circular story-rail
position under **bKash Deal Room** and is fully interactive.

`index.html` is completely self-contained (runtime + background image are
inlined). The only external dependency is the Horizon embed script, loaded
at runtime from `https://play.horizonexp.com/embed.js` — this is intentional
so it hydrates once your domain is whitelisted.

## Deploy to Vercel

### Option A — Vercel dashboard (drag & drop)
1. Push this folder to a GitHub repo (or use the Vercel "deploy a folder" flow).
2. In Vercel, **New Project → Import** the repo.
3. Framework preset: **Other**. No build command. Output/root: this folder.
4. Deploy. You get a live URL like `https://your-project.vercel.app`.

### Option B — Vercel CLI
```bash
npm i -g vercel
cd export
vercel --prod
```

### Option C — GitHub Pages
Push `index.html` to a repo and enable Pages on the branch/root.

## After deploy — whitelist the domain
1. Copy your live domain (e.g. `your-project.vercel.app`).
2. In the **Horizon Console**, add that domain to the allowed/whitelist list
   for reference `69359e05b62bd32a6d2ec964`.
3. Reload the live page — the bKash Deal Room circular video rail will
   hydrate in place.

> Until the domain is whitelisted you'll see a console message
> `License key is null - access denied`. That's expected and resolves once
> the domain is approved.

## The entry-point snippet (already wired in)
```html
<div data-horizon-ep="#377585" data-horizon-ep-skeleton="cs"></div>
<script src="https://play.horizonexp.com/embed.js"
        data-horizon-ref="69359e05b62bd32a6d2ec964"></script>
```
The embed script is guaranteed to load only once.
