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

Basically, we keep everything (images, pdf, metadata, etc.) on Github. If you are not a master person, you should not need a local setup. The 2022-23 master is __Lily Ge__, and __Hyeok Kim__ (the developer) and __Fumeng Yang__ (the side worker) also have knowledge about this if you have any questions. 


## Adding a paper (for everyone)

The two folders you have to pay attention to are: 
  * `_posts`: This folder provides information for papers. You need to add a new `*.md` file when you want to add a paper. 
  *  `assets`: This folder provides the actual thumbnails and PDFs. 

You need to prepare the followings: 
  * __a unique ID__: say [awesome-paper] and it is published in `yyyy`. This ID is used everywhere to grab information for rendering the website. 
  * __a `.md` file__ (see below) that will be uploaded to `_posts` : you __must__ name it `yyyy-mm-dd-[awesome-paper].pdf` The month and date aren't important. You can use any values.  
  * __the paper PDF__ that will be uploaded to `assets/papers/`: you __must__ name it `yyyy-[awesome-paper].pdf`
  * __a thumbnail__ that will be uploaded to `assets/images/`: you __must__ name it `paper-banner-[awesome-paper].png|jpg|jpeg|gif|bmp`. The width should be less than 1200px, and we suggest to use a 4:3 aspect ratio.
  * authors, abstract, venue, year, awards
  * other links you want to show

### The `.md` file

This file must be called: `yyyy-mm-dd-[awesome-paper].md` It gives entries to render a paper. 

```yaml
---
layout: paper
category: //
title:  "Hypothetical Outcome Plots Outperform Error Bars and Violin Plots for Inferences about Reliability of Variable Ordering"
authors: "Jessica Hullman, Paul Resnick, Eytan Adar"
venue: "PLOS ONE 2015"
thumb: "assets/images/paper-thumb-hops.png"
banner: "assets/images/paper-banner-hops.png"
caption: "A) Representations of uncertainty compared in our study, B) HOPs limiting case, C) HOPs can express properties of a joint distribution."
pdf: "assets/papers/2015-hops.pdf"
---

<!-- abstract -->
Many visual depictions of probability distributions, such as error bars, are difficult for users to accurately interpret. We present and study an alternative representation, Hypothetical Outcome Plots (HOPs), that animates a finite set of individual draws. In contrast to the statistical background required to interpret many static representations of distributions, HOPs require relatively little background knowledge to interpret. Instead, HOPs enables viewers to infer properties of the distribution using mental processes like counting and integration. We conducted an experiment comparing HOPs to error bars and violin plots. With HOPs, people made much more accurate judgments about plots of two and three quantities. Accuracy was similar with all three representations for most questions about distributions of a single quantity.
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
