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

## Add a podcast

Run the helper with the audio file, one image, and a title:

```shell
bin/new-podcast ~/episode.mp3 ~/cover.jpg "Episode title" "A short description."
```

It copies both files into `assets/podcasts/` and creates the episode in
`_podcasts/`. Edit the description there if needed, then commit and push.

To add one by hand instead, put the files in `assets/podcasts/` and create
`_podcasts/YYYY-MM-DD-short-title.md`:

```markdown
---
title: "Episode title"
date: YYYY-MM-DD
description: "A short description."
audio: /assets/podcasts/short-title.mp3
audio_bytes: 12345678
image: /assets/podcasts/short-title.jpg
---
```

`audio_bytes` is the audio file size in bytes, which podcast apps read from
the feed. Optional extras are `duration` (such as `"32:10"`) and Markdown
show notes below the front matter. The image displays 500px wide on the
episode page and as a thumbnail in the list, so a square image of at least
500px works best. GitHub rejects files over 100 MB.

Episodes are listed at `/podcasts/` and published to podcast apps through
the feed at `/podcasts/feed.xml`. Show-level feed details live under
`podcast` in `_config.yml`.

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
