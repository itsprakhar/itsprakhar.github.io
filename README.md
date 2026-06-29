# Prakhar Thakur — blog

A Jekyll site for GitHub Pages. Writing-first, with categories, tags, SEO, sitemap, and RSS.

## Deploy to GitHub Pages

1. Create a repo named **`itsprakhar.github.io`** (this exact name makes it a user site served at the root domain).
2. Put everything in this folder at the root of that repo and push to the `main` branch.
3. In the repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
4. Wait a minute. The site goes live at `https://itsprakhar.github.io`.

No build step is needed on your machine. GitHub builds the Jekyll site for you.

> Before first deploy, open `_config.yml` and confirm `url` is correct. If you ever use a custom domain, update `url` and add a `CNAME` file.

## Write a new post

Drop a markdown file in `_posts/` named `YYYY-MM-DD-title.md`:

```markdown
---
title: "Your title"
description: "One or two sentences. This is what search engines and link previews show."
date: 2026-07-01
categories: [research]      # one of: engineering, research, ideas, philosophy
tags: [jepa, ssl]           # as many as you like
---

Opening paragraph that shows on the home page.

<!--more-->

The rest of the post.
```

That is the whole workflow. Categories and tags pages update themselves.

## Categories

The four threads, used as categories: `engineering` (applied ML and MLOps), `research` (representation and self-supervised learning), `ideas` (mental models and epistemics), `philosophy` (mind and AI). Use whichever fits; add new ones any time.

## Local preview (optional)

If you ever want to preview locally, install Ruby, then:

```bash
gem install bundler
bundle install
bundle exec jekyll serve
```

Open `http://localhost:4000`.

## SEO

Handled by `jekyll-seo-tag` (titles, meta descriptions, Open Graph, Twitter cards, JSON-LD), `jekyll-sitemap` (`/sitemap.xml`), and `robots.txt`. Give every post a good `description` and you are set.
