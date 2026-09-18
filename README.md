# Brandon Mossop Research Website

A Quarto-based academic and research website designed for GitHub Pages and a custom domain.

## 1. Install Quarto

Download Quarto from https://quarto.org/docs/get-started/

## 2. Preview locally

From this folder run:

```bash
quarto preview
```

## 3. Create the GitHub repository

Recommended repository name:

```text
bdmossop.github.io
```

Then initialize and push:

```bash
git init
git add .
git commit -m "Initial research website"
git branch -M main
git remote add origin https://github.com/bdmossop/bdmossop.github.io.git
git push -u origin main
```

## 4. Enable GitHub Pages

After the first GitHub Action completes:

1. Open the repository on GitHub.
2. Go to Settings > Pages.
3. Set the publishing source to the `gh-pages` branch if GitHub has not selected it automatically.
4. Your site should then be available at `https://bdmossop.github.io`.

## 5. Add your custom domain

In GitHub:

1. Settings > Pages.
2. Under Custom domain, enter `www.brandonmossop.com`.
3. Save it.

At your domain registrar/DNS provider, configure:

- `CNAME` for `www` pointing to `bdmossop.github.io`
- GitHub Pages apex-domain DNS records for `brandonmossop.com` if you also want the bare domain to work.

Follow the current GitHub Pages custom-domain documentation when adding the apex A/AAAA records, because provider interfaces and recommended records can change.

## 6. Customize before publishing

Recommended edits:

- Add your final CV to `assets/Brandon_Mossop_CV.pdf`.
- Add Google Scholar, ORCID, LinkedIn, and preferred contact information to `about.qmd`.
- Add DOI/PDF links to `publications.qmd`.
- Replace or revise the sample research notes.
- Add a professional headshot only if you want one on the site.

## Adding a new research note

Create:

```text
posts/my-post/index.qmd
```

Use front matter like:

```yaml
---
title: "My Post Title"
date: 2026-09-18
categories: [Causal AI]
---
```

Then write the post in Markdown below it and push to GitHub.
