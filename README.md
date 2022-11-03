# MU Collective Website

This is (currently) an in-progress repo for mucollective.co renewal. This website will be built on Jekyll.

# People

Hyeok Kim - rebuilding the template.

Lily Ge - building the individual md files.

Fumeng Yang - documentation & style

# Prerequisites

Take a look on [this document for installing and configuring](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll) and [this document for testing](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll).

# How to Update

## Home

- Text on the top left section: `_data/home_text.yml`
- Thumbnail grid on the top right section: `_data/home-images.yml`

## Papers

### File name

Keep the format to make the papers sortable.

Format: `YYYY-MM-01-keywords.md`

Example: `2022-07-01-the-worst-of-both-words.md`

### Header

```yml
---
layout: paper # do not change
category: paper # do not change
title:  "Paper Title"
authors: "Author 1, Author 2"
venue: "Venue name"
thumb: "/assets/images/__thumbnail_image__.png"
banner: "/assets/images/__baner_imgage__.png"
caption: "Banner caption"
bestPaper: true # if it got best paper award
honorable: true # if it got best paper honorable mention
pdf: "/assets/papers/__pdf_file__.pdf"
supplementary: "supplementary_file" # github repo if exists
github: "http://github.com" # github repo if exists
additionals:  # additional information
  - name: "Website"
    link: "http://github.com"
  - name: "Medium Post"
    link: "http://medium.com"
---
```

### content

Provde an abstract only

## People

Edit `_data/people.yml` file

- For faculty/current student, provide their `name`, `role` (professor, phd student, post doc, etc), `department`, `school`, `image`, and website url (`link`).
- For alumni, provide their `name`, current `position`, and website url (`link`).

## Assets

All the images are stored under `assets/images` and pdfs are under `assets/papers`.
