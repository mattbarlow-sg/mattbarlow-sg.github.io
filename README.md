# mattbarlow-sg.github.io

Source for [mattbarlow-sg.github.io](https://mattbarlow-sg.github.io/).

This is a Jekyll-powered GitHub Pages site with a Tokyo Night-inspired color
palette and a self-hosted Iosevka typeface.

## Add a learning

Create `_posts/YYYY-MM-DD-short-title.md` with front matter followed by
Markdown:

```markdown
---
layout: post
title: "The post title"
date: YYYY-MM-DD
description: "A short summary for the homepage."
tags:
  - topic
---

Write the learning here.
```

Put images in `assets/images/` and downloadable files in `assets/files/`.
Reference them from Markdown with root-relative paths such as
`![Description](/assets/images/example.png)`.

## Preview locally

The site uses Ruby 3.3.4, matching GitHub Pages. With `mise` installed, run:

```shell
mise install
bundle install
bundle exec jekyll serve
```

The site will be available at `http://127.0.0.1:4000/`.

Iosevka is distributed under the SIL Open Font License 1.1. Its license is
included alongside the webfont files in `assets/fonts/OFL.txt`.
