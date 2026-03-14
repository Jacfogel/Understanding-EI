# Understanding EI

Unofficial educational documentation website about Employment Insurance (EI) in Canada, built with MkDocs and Material for MkDocs.

> **Disclaimer:** This is not an official Government of Canada or ESDC website. It is informational only, not legal advice.

## What this project is

- A plain-language learning resource based on publicly available EI materials
- A documentation-style website designed for clarity and navigation
- A starter structure that can be expanded with verified official links and visuals

## Local development

1. Create a virtual environment (recommended)
2. Install dependencies
3. Run the local docs server

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

Open `http://127.0.0.1:8000`.

## Deployment (GitHub Pages)

This repository includes a GitHub Actions workflow at `.github/workflows/deploy.yml`.

1. Push to `main`
2. In GitHub, ensure **Settings → Pages → Build and deployment** is set to **GitHub Actions**
3. The workflow builds and publishes the `site/` output automatically

## Enable GitHub Pages (step-by-step)

I can’t directly click your GitHub settings from this environment, so I can’t enable Pages on your account for you. I **did** set up the deploy workflow so once Pages is enabled, deploys are automatic.

### In GitHub UI

1. Open your repository: `https://github.com/jacfogel/Understanding-EI`
2. Go to **Settings** → **Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.
4. Save.
5. Push to `main` (or re-run the deploy workflow from **Actions**).
6. Wait for the workflow **Deploy MkDocs to GitHub Pages** to complete.
7. Your site URL will be: `https://jacfogel.github.io/Understanding-EI/`

### Optional: using GitHub CLI (PowerShell)

```powershell
gh repo edit jacfogel/Understanding-EI --enable-pages --pages-source-build-type workflow
```

If that command errors, update GitHub CLI and ensure you are logged in:

```powershell
gh auth login
```

## Where to edit content

- Site configuration: `mkdocs.yml`
- Main pages: `docs/`
- Topic pages: `docs/topics/`
- Process pages: `docs/process/`
- Reference pages: `docs/reference/`
- Visual placeholders and planning notes: `docs/assets/README.md`
