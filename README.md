# MU Collective Website

This is (currently) an in-progress repo for mucollective.co renewal. This website will be built on Jekyll.

# Staff

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

Basically, we keep everything (images, pdf, metadata, etc.) on Github. If you are not a master person, you should not need a local setup. The 2022-23 master is __Lily Ge__, and __Hyeok Kim__ (the developer) and __Fumeng Yang__ (the side worker) also have knowledge about this if you have any questions. 


## Adding a paper (for everyone)

The two folders you have to pay attention to are: 
  * `_posts`: This folder provides information for papers. You need to add a new `*.md` file when you want to add a paper. 
  *  `assets`: This folder provides the actual thumbnails and PDFs. 

You need to prepare the followings: 
  * __a unique ID__: say `awesome-paper` and it is published in `yyyy`. This ID is used everywhere to grab information for rendering the website. 
  * __a `.md` file__ (see below) that will be uploaded to `_posts` : you __must__ name it `yyyy-mm-dd-awesome-paper.pdf` The month and date aren't important. You can use any values.  
  * __the paper PDF__ that will be uploaded to `assets/papers/`: you __must__ name it `yyyy-awesome-paper.pdf`
  * __a teaser/banner__ that will be uploaded to `assets/images/`: you __must__ name it `paper-banner-awesome-paper.png|jpg|jpeg|gif|bmp`. The width should be less than 1200px, and we suggest to use a 4:3 aspect ratio.
  * __a thumbnail__ that will be uploaded to `assets/images/`: you __must__ name it `paper-thumb-awesome-paper.png|jpg|jpeg|gif|bmp`. The width should be less than 1200px, and we suggest to use a 4:3 aspect ratio.
  * authors, abstract, venue, year, awards
  * other links you want to show

### The `.md` file

This file must be called: `yyyy-mm-dd-awesome-paper.md` It gives entries to render a paper. You must specify year like `2022-12-01-awesome-paper.md`.

A toy example is: 

```
---
layout: paper
category: paper 
title:  "This is an awesome paper"
authors: "Author 1, Author 2, Author 3"
venue: "The Lucky Conference/Journal"
thumb: "assets/images/paper-thumb-[awesome-paper].png"
banner: "assets/images/paper-banner-[awesome-paper].png"
caption: "The caption for the banner/teaser."
pdf: "assets/papers/yyyy-mm-dd-[awesome-paper].pdf"
bestPaper: true
honorable: false
github: "github.com/awesome"
supplementary: "https://osf.io/awesome/"
additionals:
  - name: "Gallery"
    link: "https://awesomepaper.com"
---

<!-- abstract -->
This is our awesome paper published at the Lucky Conference. 
```

Explanation: 
* __layout: paper__: this must be `paper`.
* __category: paper__: This can take more than one keyword, like `paper quant-uncerntainty`. The second keyword is used to put the paper under a research area, which you can find under `_data/research_area.yml` (the `cat` field.) If you don't know, leave it as `paper`. 
* __title...pdf__: ordinary stuff. Notice that you must follow the naming style! 
* (optional) __bestPaper__ and __honorable__: true or false. You can also skip it if it is false. 
* (optional) __github__ and __supplementary__: You can also skip it if it is false.
* (optional) __additionals__: additional links. You can also skip it if it is false.

Now,

* upload `yyyy-mm-dd-awesome-paper.md` to `_posts`
* upload `yyyy-awesome-paper.pdf` to `assets/papers`
* upload `paper-banner-awesome-paper.png` and `paper-thumb-awesome-paper.png` to `assets/images`

Then check out [Mu website](https://mucollective.github.io/mucollective.co/) and you should be able to see the updates (you might need to wait for a few minutes.)


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
