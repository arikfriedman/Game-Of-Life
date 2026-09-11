# Field Notes — standalone app

This folder is a complete, self-contained web app (no build step needed to run
it — it's already built). To use it, it just needs to be hosted somewhere
that serves static files over HTTPS, then added to your phone's home screen.

## Easiest free hosting: GitHub Pages

1. Go to https://github.com and sign in (or create a free account).
2. Click "+" (top right) → "New repository." Name it anything, e.g.
   `field-notes`. Keep it Public. Create it without a README.
3. On the new repo's page, click "uploading an existing file," then drag in
   every file from this folder (index.html, manifest.json, sw.js, bundle.js,
   the icons folder — keep the icons folder structure intact). Commit.
4. Go to the repo's Settings → Pages. Under "Source," choose the `main`
   branch and `/ (root)` folder, then Save.
5. GitHub will give you a URL like
   `https://yourusername.github.io/field-notes/` — that's your live app.
   It can take a minute or two to go live the first time.

## Add it to your Android home screen

1. Open the URL from step 5 in Chrome on your phone.
2. Tap the three-dot menu → "Add to Home screen" (Chrome may also prompt
   you automatically with an "Install app" banner).
3. It'll now open full-screen, like a normal app, with its own icon.

## Notes

- Your data is stored locally in the phone's browser storage for that site.
  It stays on your device and isn't sent anywhere. It will **not** show up
  in your old Claude-artifact version, and switching phones or clearing
  browser data will reset it — there's no account or sync involved.
- Because everything (including React) is bundled into `bundle.js`, the app
  also works offline once you've opened it at least once.
- If you want to make changes later (add fields, tweak actions, adjust
  styling), the easiest path is to come back here and ask Claude to update
  the source and rebuild — then just re-upload the changed files to the
  same GitHub repo.
