# Love Cards — A Letter in Butterflies 🦋

An interactive, single-file romantic experience:

- A stack of **13 handwritten cards** (Caveat / Dancing Script) with unique love notes
- Swipe, drag, or tap the top card and it **shatters into hundreds of canvas butterflies** that fly in bundles and scale up along the Z-axis, toward the viewer
- The final **Master Card** asks *"DO YOU REALLY LOVE ME"* — but the Yes/No buttons **run away** every time you get close
- After **10 chase attempts**, the buttons freeze and a full-screen finale blooms:
  *"You don't need to say, I always Know your Answer"*

## Run locally

Just open `public/index.html` in a browser — no build step, no dependencies.

## Deploy on Render

This repo includes a `render.yaml` blueprint.

1. Push this repo to GitHub
2. On [Render](https://dashboard.render.com) → **New → Static Site**
3. Connect the repo, set **Publish Directory** to `public` (or use **New → Blueprint** and Render reads `render.yaml` automatically)
4. Deploy — every push to `main` redeploys

## Tech

Vanilla HTML/CSS/JS. Butterflies are pre-rendered sprite atlases (6 palettes × 16 flap frames) drawn on a single `<canvas>` with perspective projection (`scale = focal / (focal + z)`), additive glow when near the lens, and motion-trail fading. No frameworks.
