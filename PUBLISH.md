Publishing your static site
==========================

This file contains step-by-step instructions to publish the site in this folder to GitHub Pages, Netlify, or Vercel.

1) Quick checklist before publishing
  - Open `index.html` in your browser locally to confirm it looks right.
  - Ensure `css/style.css` and `assets/` are present and referenced with relative paths (they are in this project).
  - Ensure backups/ is present and ignored by git (we added `.gitignore`).

2) GitHub Pages (recommended for a personal project)

  a) Create a GitHub repository on github.com (e.g., `yourusername/bank`).
  b) Run these commands in PowerShell (from the `c:\Users\lenovo\OneDrive\Desktop\bank` folder):

```powershell
git init ;
git add . ;
git commit -m "Initial site publish" ;
git branch -M main ;
# replace <URL> with the repository URL you created (HTTPS or SSH)
git remote add origin <URL> ;
git push -u origin main
```

  c) On GitHub > Repository settings > Pages: set branch to `main` and folder `/ (root)` and save.
     After a minute or two your site will be available at `https://<yourusername>.github.io/<repo-name>/`.

  d) Common issue: CSS or images 404 on GitHub Pages. Fixes:
     - Make sure paths in HTML/CSS are relative (like `css/style.css` not `/css/style.css`).
     - Ensure files are committed and not in `.gitignore`.
     - If you used an index at root, ensure Pages is set to `/(root)`.

3) Netlify (drag-and-drop or repo connect)

  - Drag and drop the site folder into Netlify Drop (https://app.netlify.com/drop) or connect your GitHub repo to Netlify
  - For SPA or redirects, add a `_redirects` file. Not required for simple static site.

4) Vercel (connect repo)

  - Sign in to Vercel and import the GitHub repository. Default settings work for a static site.

5) If you prefer, I can prepare a ZIP of the project for upload to Netlify's drag-and-drop interface. Reply "ZIP please".

If you want, tell me your preferred provider and repository URL (if you've already created one). I can then generate the exact PowerShell commands with your repo URL filled in, and help verify the live site after you push.
