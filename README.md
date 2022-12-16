# MU Collective Website

This is (currently) an in-progress repo for mucollective.co renewal. This website will be built on `Jekyll`. 

## Staff

Hyeok Kim - rebuilding the template :man_technologist:.

Lily Ge - building the individual md files and managing the website after it is done :woman_pilot:.

Fumeng Yang - writing documentation & nudging style :woman_juggling:

## How to update (for everyone)

Basically, we keep everything (images, pdf, metadata, etc.) on Github. If you are not a master person, you should not need a local setup. The 2022-23 master is __Lily Ge__; __Hyeok Kim__  and __Fumeng Yang__ also have knowledge about this if you have any questions.

In sum, you only need to touch `_data`, `_posts`, and `assets`. __Hyeok: "If you are touching anything else, it means you are doing something wrong."__

After your edits, wait for a few minutes and check out [Mu website](https://mucollective.github.io/mucollective.co/) and you should be able to see the updates.

### Add a [paper](https://mucollective.github.io/mucollective.co/publications) :page_facing_up:

The two folders you have to pay attention to are:

* `_posts`: This folder provides information for papers. You need to add a new `*.md` file when you want to add a paper.
* `assets`: This folder provides the actual thumbnails and PDFs.

You need to prepare the followings:

* __a unique ID__: say `awesome-paper` and it is published in `yyyy`. This ID is used everywhere to grab information for rendering the website.
* __a `.md` file__ (see below) that will be uploaded to `_posts` : you __must__ name it `yyyy-mm-dd-awesome-paper.md` The month and date aren't important. You can use any values.
* __the paper PDF__ that will be uploaded to `assets/papers/`: you __must__ name it `yyyy-awesome-paper.pdf`
* __a teaser/banner__ that will be uploaded to `assets/images/`: you __must__ name it `paper-banner-awesome-paper.png|jpg|jpeg|gif|bmp`. The width should be less than 1200px, and we suggest to use a 4:3 aspect ratio.
* __a thumbnail__ that will be uploaded to `assets/images/`: you __must__ name it `paper-thumb-awesome-paper.png|jpg|jpeg|gif|bmp`. The width should be less than 1200px, and we suggest to use a 4:3 aspect ratio.
* authors, abstract, venue, year, awards
* other links you want to show

#### The `.md` file

This file __must__ be called: `yyyy-mm-dd-awesome-paper.md` It gives entries to render a paper. Again, you must specify year like `2022-12-01-awesome-paper.md` but months and days are not important.

A toy example is below. You can copy it as your template file.

```{yaml}
---
layout: paper
category: paper 
title:  "This is an awesome paper"
authors: "Author 1, Author 2, Author 3"
venue: "The Lucky Conference/Journal"
thumb: "assets/images/paper-thumb-awesome-paper.png"
banner: "assets/images/paper-banner-awesome-paper.png"
caption: "The caption for the banner/teaser."
pdf: "assets/papers/yyyy-mm-dd-awesome-paper.pdf"
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

* __layout: paper__ - this must be `paper`.
* __category: paper__ - This can take more than one keyword, like `paper quant-uncerntainty`. The second keyword is used to put the paper under a research area, which you can find under `_data/research_area.yml` (the `cat` field.) If you don't know, leave it as `paper`.
* __title...pdf__ - ordinary stuff. Notice that you must follow the naming style!
* (optional) __bestPaper__ and __honorable__ - true or false. You can also skip it.
* (optional) __github__ and __supplementary__ - You can also skip it.
* (optional) __additionals__ - additional links and a name to show. You can also skip it.

Now,

* upload `yyyy-mm-dd-awesome-paper.md` to `_posts`
* upload `yyyy-awesome-paper.pdf` to `assets/papers`
* upload `paper-banner-awesome-paper.png` and `paper-thumb-awesome-paper.png` to `assets/images`

You are all set.

### Add a new [person](https://mucollective.github.io/mucollective.co/people) :frowning_person:

You need to prepare the followings:

* A 1x1 headshot named `people-first-last.png|jpg|jpeg|gif|bmp`. (Fumeng: I don't know if you want to use a gif, but it is possible?) You must follow the naming style `people-...`.

You only have to __edit__ `_data/people.yml` file and upload the image to `assets/images`.

An example:

```{yaml}
  - name: Jessica Hullman
    role: Ginni Rometty Associate Professor
    department: Computer Science
    school: Northwestern University
    image: assets/images/people-jessica-hullman.jpeg
    link: http://users.eecs.northwestern.edu/~jhullman/

```

Explanation:

* For a faculty/current student, you should provide their `name`, `role` (professor, phd student, post doc, etc), `department`, `school`, `image`, and website url (`link`).
* For alumni, you should provide their `name`, current `position`, and website url (`link`).

### Edit [research area](https://mucollective.github.io/mucollective.co/research) :mortar_board:

You only need to edit `_data/research_areas.yml` file.

An example:

```{yaml}
- name: Communicating unquantified uncertainty 
  category: unquant-uncertainty 
  desc: We aim at communicating unquantified uncertainty. 
  image:
    - "assets/images/research-image-...."
```

Explanation:

* __name__ is the name to show in the list
* __category__  is the catergory, which will be used to match and grab papers. 
* __desc__ is the description.
* __image__ is the list of related images to show (suggestion: upto 2). You can list images in the YAML list format.

### Add or edit a [public release](https://mucollective.github.io/mucollective.co/public-release) :earth_americas:

You need to prepare the followings:

* URLs to your release.

There are two files `_data/prototype.yml` and `_data/software.yml`. Our suggestion is that if it is a concrete thing, then it belongs to `software`. The entry should be very much self-explanatory.

An example from `_data/prototype.yml`:

```{yaml}
- title: Cicero
  contributor: Hyeok Kim
  type: JS library
  supplement:
    - type: Gallery
      link: https://see-mike-out.github.io/cicero-supplemental/
  description: Cicero is a declarative grammar for responsive visualization transformatons.
```

An example from `_data/software.yml`:

```{yaml}
 title: ggidst
  contributor: Matthew Kay
  type: R package
  supplement:
    - type: Documentation
      link: https://mjskay.github.io/ggdist/
    - type: Code Repository
      link: https://github.com/mjskay/ggdist
    - type: CRAN
      link: https://cloud.r-project.org/web/packages/ggdist/index.html 
  description: ggdist is an R package that provides a flexible set of ggplot2 geoms and stats designed especially for visualizing distributions and uncertainty.
```

### Add or edit a [talk](https://mucollective.github.io/mucollective.co/talks) :speech_balloon:

You only need to edit `_data/talk.yml` file.

```{yaml}
- title: Uncertainty visualization with tidybayes and ggdist
  year: 2021
  contributor: Matthew Kay
  venue: Bayes@Lund
  link: https://youtu.be/EtrmxMX8zWw
```

### Edit text on homepage on the top

* Text on the top left section: `_data/home_text.yml`

## How to update (for developer)

### Prerequisites

Take a look on [this document for installing and configuring](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll) and [this document for testing](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll).

### How to run it locally

1. Install Ruby. [Guide](https://mac.install.guide/ruby/12.html) If you could not open the link, try Incognito/Privacy mode or Safari browser. The followings are an overview:
  a. `brew install ruby-install chruby`.
  b. `ruby-install -V` At the end of installation, there are two lines `source /usr/local/...`.
  c. `open -e ~/.zshrc` and add the two lines from the above as well as `chruby ruby-3.1.2`  This is the version we are going to use.  
  d. Restart your terminal and run `ruby-install ruby 3.1.2`.
  e. It takes a few minutes and you confirm the version of ruby 3.1.2 by running `ruby -v`. If not, try to open a new Terminal.
2. Install Jekyll: `gem install jekyll` You might need to run this using `sudo`.
3. Run: `jekyll serve`
