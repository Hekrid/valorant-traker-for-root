# Valorant Tracker demo site

A GitHub Pages site: a landing page with an interactive mock of the app (sample data only),
a stand-in for Riot sign-in, and the privacy policy.

- `index.html` landing page (explains that this is a mock of an upcoming Root app)
- `demo/` the app's real screens, built with sample data instead of the Root server
- `privacy.html` privacy policy (same text as `../privacy.md`)

## Publish on GitHub Pages

1. Create a public repository, e.g. `valorant-tracker`.
2. Upload everything in this folder (keep the `demo/` folder as it is).
3. Repository **Settings → Pages → Build and deployment**: Source "Deploy from a branch",
   branch `main`, folder `/ (root)`, Save.
4. After a minute the site is at `https://<your-user>.github.io/valorant-tracker/`.

## Rebuild the demo after app changes

From `client/`:

```bash
npx vite build --config preview/vite.demo.ts
```

It rewrites `site/demo/`. The sample data is in `client/preview/mock.ts`.
