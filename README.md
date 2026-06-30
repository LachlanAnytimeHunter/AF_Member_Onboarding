# Anytime Fitness — Around The Club in 30 Days

Member onboarding journey app for Anytime Fitness Newcastle Region.
A single self-contained web app — no build step, no dependencies, no backend.

## Files

- `index.html` — the entire app (HTML/CSS/JS in one file)
- `manifest.json` — enables "Add to Home Screen" / installable behaviour on Android
- `icon-192.png`, `icon-512.png` — app icons used on the home screen

## How to publish this on GitHub Pages (free, ~5 minutes)

1. Create a new repository on GitHub (e.g. `af-onboarding`). Keep it **public**
   (GitHub Pages on free accounts requires a public repo, unless you're on GitHub
   Pro/Team/Enterprise where private repos are also supported).
2. Upload all 4 files in this folder to the root of that repository
   (drag-and-drop works fine via the GitHub web UI — "Add file" → "Upload files").
3. Go to the repo's **Settings → Pages**.
4. Under "Build and deployment", set **Source** to "Deploy from a branch".
5. Set **Branch** to `main` (or `master`) and folder to `/ (root)`. Save.
6. GitHub will give you a live URL within a minute or two, typically:
   `https://YOUR-USERNAME.github.io/af-onboarding/`
7. Test that URL on your phone — confirm the checklist loads and "Add to Home
   Screen" works on both iPhone (Safari) and Android (Chrome).
8. Generate your QR code pointing to that exact URL.

## Updating the app later

Any time you want to change wording, add/remove checklist items, or update
branding: edit `index.html` directly in the GitHub web UI (click the pencil
icon on the file) and commit the change. GitHub Pages redeploys automatically
within a minute or two. No QR code regeneration needed — the URL stays the same.

## Important limitation to know about

Member progress is stored in `localStorage` on **their own phone/browser**.
This means:
- Progress is private to that device — there's no central dashboard showing
  you which members have completed what across your 6 clubs.
- If a member clears their browser data, uses a different phone, or switches
  from Safari to Chrome, their saved progress will reset.

This is fine for a personal checklist experience at this stage. If you want
network-wide visibility (e.g. to verify a t-shirt redemption code is genuine,
or report completion rates as regional manager), the next step is adding a
lightweight shared backend — happy to build that when you're ready to scale.

## Custom domain (optional, later)

GitHub Pages supports custom domains for free. If you'd rather members see
`start.anytimefitnessnewcastle.com.au` instead of a `github.io` URL:
1. Buy the domain (any registrar, ~$15/year).
2. In repo Settings → Pages, add the custom domain.
3. Add the DNS records GitHub provides at your domain registrar.
4. Enable "Enforce HTTPS" once the certificate provisions (usually within an hour).
