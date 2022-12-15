# MU Collective Website

This is (currently) an in-progress repo for mucollective.co renewal. This website will be built on Jekyll.

# People

Hyeok Kim - rebuilding the template.

Lily Ge - building the individual md files.

Fumeng Yang - documentation & style

# Prerequisites

Take a look on [this document for installing and configuring](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll) and [this document for testing](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll).

# How to run it locally

1. Install Ruby. [Guide](https://mac.install.guide/ruby/12.html) If you could not open the link, try Incognito/Privacy mode or Safari browser. The followings are an overview: 

   * a. `brew install ruby-install chruby`. 
   
   * b. `ruby-install -V` At the end of installation, there are two lines `source /usr/local/...`.  
   
   * c. `open -e ~/.zshrc` and add the two lines from the above as well as `chruby ruby-3.1.2`  This is the version we are going to use.  
   
   * d. Restart your terminal and run `ruby-install ruby 3.1.2`. 
   
   * e. It takes a few minutes and you confirm the version of ruby 3.1.2 by running `ruby -v`. If not, try to open a new Terminal. 
 
2.  Install Jekyll: `gem install jekyll` You might need to run this using `sudo`.

3.  Run: `jekyll serve`

# How to Update

Basically, we keep everything (images, pdf, metadata, etc.) on Github. If you are not a master person, you should not need to a local setup. The 2022-23 master is Lily Ge, and Hyeok Kim (the developer) and Fumeng Yang (the side worker) also have knowledge about this if you have any questions. 


## Adding a paper (for everyone)

The two folders you have to pay attention to are: 
* `_posts`: This folder provides information for papers. You need to add a new `*.md` file when you want to add a paper. 
*  `assets`: This folder provides the actual thumbnails and PDFs. 

You need to prepare the followings: 
* a unique ID: say [awesome-paper] and it is published in `yyyy`. This ID is used everywhere to grab information for rendering the website. 
* a `.md` file (see below) that will be uploaded to `_posts` : you __must__ name it `yyyy-mm-dd-[awesome-paper].pdf` The month and date aren't important. You can use any values.  
* the paper PDF that will be uploaded to `assets/papers/`: you __must__ name it `yyyy-[awesome-paper].pdf`
* a thumbnail that will be uploaded to `assets/images/`: you __must__ name it `paper-banner-[awesome-paper].png|jpg|jpeg|gif|bmp`. The width should be less than 1200px, and we suggest to use a 4:3 aspect ratio.
* authors, abstract, venue, year, awards
* other links you needed

### File name

Keep the format to make the papers sortable.

Format: `YYYY-MM-01-keywords.md`

Example: `2022-07-01-the-worst-of-both-words.md`

### Header

```yml
---
layout: paper # do not change
category: paper research_area_category # do not change "paper"
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


## Home

- Text on the top left section: `_data/home_text.yml`
- Thumbnail grid on the top right section: `_data/home-images.yml`


## People

Edit `_data/people.yml` file

- For faculty/current student, provide their `name`, `role` (professor, phd student, post doc, etc), `department`, `school`, `image`, and website url (`link`).
- For alumni, provide their `name`, current `position`, and website url (`link`).

## Assets

All the images are stored under `assets/images` and pdfs are under `assets/papers`.

## Research

Edit `_data/research_areas.yml` file to add/remove research areas.

Example research area definition:

```yaml
- name: Communicating unquantified uncertainty # name to show in the list
  cat: unquant-uncertainty # category to query for
  desc: We aim at communicating unquantified uncertainty. # description
```

In paper post files, make sure to include a topic category and to match it to the category name in the research area definitions.
