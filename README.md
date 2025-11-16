EDTA (client-side)
====================

This is a small client-side web app (HTML/CSS/JS) that uses localStorage for authentication, goals and XP tracking. It is static and can be hosted on any static hosting provider (GitHub Pages, Netlify, Vercel, Surge, etc.).

Quick local run
---------------
You can run the site locally in a simple static server.

Option A (recommended - uses npx):

```bash
npx serve -s . -l 8080
```

Option B (Python 3 builtin):

```bash
python3 -m http.server 8080
# then open http://localhost:8080/welcomepage.html
```

Option C (install `serve` globally):

```bash
npm install -g serve
serve -s . -l 8080
```

Deploying online
----------------
1) GitHub Pages (automated via GitHub Actions)
   - Push this repository to GitHub (prefer branch `main`).
   - The included GitHub Actions workflow will automatically deploy the repository contents to GitHub Pages when you push to `main`.
   - After the first successful run, check the repository Settings → Pages to view the site URL.

2) Netlify
   - Drag-and-drop the site folder in the Netlify dashboard, or connect the repository and set the publish directory to the repository root.
   - No build step required.

3) Vercel
   - Use `vercel` cli or connect the repo in the Vercel dashboard and deploy.

Notes & Recommendations
-----------------------
- The app uses `localStorage` for data. If you want server-side persistence or real authentication, you'll need a backend.
- For development, use `welcomepage.html` as the entry point.

Files added to help deployment:
- `package.json` — convenience scripts
- `.github/workflows/deploy.yml` — GitHub Actions workflow to publish to GitHub Pages
- `.gitignore` — ignores node_modules, system files

If you want, I can also:
- Create a small README section with environment variables for a custom domain
- Set up a `CNAME` file for GitHub Pages
- Configure Netlify redirects
