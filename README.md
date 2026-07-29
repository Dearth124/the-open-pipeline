# The Open Pipeline

A simple Jekyll blog for posting research papers and write-ups, built to be hosted on GitHub Pages.

## How posts work

Each post lives in `_posts/` as a Markdown file named `YYYY-MM-DD-some-slug.md`, with front matter like:

```yaml
---
title: "Your Paper Title"
author: Your Name
pdf: /assets/papers/your-paper.pdf   # optional — put the PDF in assets/papers/ first
---
```

Everything below the `---` is the post body (Markdown). If you set `pdf`, a "Download the full paper (PDF)" link appears at the top of the post automatically.

To add a new post:
1. Drop the paper's PDF into `assets/papers/`.
2. Create a new file in `_posts/` following the naming pattern above.
3. Write a summary/abstract in Markdown, commit, and push — GitHub Pages rebuilds the site automatically.

## Local preview (optional)

If you have Ruby installed:

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## Deploying on GitHub Pages

1. Create a new repository on GitHub (either `<your-username>.github.io` for the root domain, or any other name for a project site served at `<your-username>.github.io/<repo-name>`).
2. Push this project to it:
   ```bash
   git remote add origin <your-repo-url>
   git branch -M main
   git push -u origin main
   ```
3. In the repo's Settings → Pages, set Source to "Deploy from a branch", branch `main`, folder `/ (root)`.
4. The site will be live at your GitHub Pages URL within a minute or two of pushing.
