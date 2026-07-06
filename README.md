# Banglalink Horizon Demo

Static single-page demo: the Banglalink app shell is a background PNG; the first
Horizon story-rail entry point (`HORIZON_ENTRY_1`) is overlaid in the blank gap
between the header and the first banner.

## Deploy to Vercel

1. Push this folder to a GitHub repo (or drag-and-drop it into Vercel).
2. In Vercel: **New Project → Import** the repo. No build settings needed —
   it's a static site (`index.html` + `mockup2.png` at the root).
3. Deploy.

## Local preview

Just open `index.html` in a browser, or serve the folder:

```
npx serve .
```

## Files

- `index.html` — the page (PNG background + Horizon embed container/script)
- `mockup2.png` — the static Banglalink app-shell image
