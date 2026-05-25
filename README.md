# jiehanL.github.io

Personal academic website for Jiehan Liu — PhD student, Department of Political Science, Stanford University.

## Local preview

Open `index.html` directly in your browser, or run a local server:

```bash
cd ~/Desktop/Stanford/personal_website
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

Your site URL will be **https://jiehanL.github.io**. Steps:

### 1. Create the GitHub repository

1. Go to https://github.com/new
2. Set **Repository name** to exactly: `jiehanL.github.io`
   (must match your GitHub username `jiehanL` + `.github.io`)
3. Set visibility to **Public**
4. Do **not** initialize with README / .gitignore / license — your folder already has files
5. Click **Create repository**

### 2. Push this folder to GitHub

Open Terminal and run from this folder:

```bash
cd ~/Desktop/Stanford/personal_website

git init
git branch -M main
git add .
git commit -m "Initial site"

# Replace with the URL GitHub showed you after step 1
git remote add origin https://github.com/jiehanL/jiehanL.github.io.git

git push -u origin main
```

If git asks for credentials, use a **Personal Access Token** in place of your password:
https://github.com/settings/tokens (Classic, scope: `repo`).

### 3. Enable Pages (usually automatic for user sites)

For repos named `<username>.github.io`, GitHub Pages is enabled automatically and serves
from the `main` branch root. If it isn't live within a couple of minutes:

1. Go to your repo → **Settings** → **Pages**
2. Under "Build and deployment":
   - **Source:** Deploy from a branch
   - **Branch:** `main` / `(root)`
3. Save. Wait 1–2 minutes, then visit https://jiehanL.github.io

### 4. Updating the site

Edit any file locally, then:

```bash
git add .
git commit -m "Update bio / publications / etc."
git push
```

GitHub Pages will redeploy within a minute.

## File structure

```
personal_website/
├── index.html            # About / home page
├── publications.html     # Research: peer-reviewed, working papers, WIP
├── teaching.html         # Teaching record
├── README.md             # This file
└── assets/
    ├── css/style.css
    ├── img/profile.jpg   # ← drop your profile photo here
    └── pdf/cv.pdf        # ← drop your CV PDF here (the "cv" nav link opens this)
```

## Things to personalize

- [ ] Save your profile photo as `assets/img/profile.jpg` (≈400×400 square)
- [ ] Save your CV as `assets/pdf/cv.pdf` — the **cv** nav link opens this file directly
- [ ] Update the bio paragraphs in `index.html`
- [ ] Replace placeholder abstracts in `publications.html` (search for `TODO`)
- [ ] Add a "News" item every time something happens

## Style

The design is loosely inspired by [al-folio](https://github.com/alshedivat/al-folio):
clean serif/sans typography, a Stanford-red accent, simple navigation, and a publication
list with collapsible BibTeX. It uses **plain HTML + CSS** (no Jekyll), so it deploys to
GitHub Pages with zero build configuration.

Dark mode is supported automatically via `prefers-color-scheme`.
