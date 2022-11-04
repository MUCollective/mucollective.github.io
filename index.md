---
layout: default
title: "Home"
---
<div class="main-wrap">
  <div class="text">
    {% for text in site.data.home_text %}
      <p class="home-display">{{text}}</p>
    {% endfor %}
  </div>
  <div class="image-grid">
    {% for image in site.data.home_images %}
       {% include home-image.html url=image.url img=image.img alt=image.alt %}
    {% endfor %}
  </div>
</div>

<div class="posts-wrap">
  <div class="title-wrap">
    <h2>News</h2>
  </div>
  {% for news in site.data.home_news %}
    {% include home-news.html title=news.title date=news.date content=news.content %}
  {% endfor %}
</div>

<div class="posts-wrap">
  <div class="title-wrap">
    <h2>Recent Papers</h2>
    <a href="/mucollective.co/papers/">See all</a>
  </div>
  {% for post in site.posts | limit: 20 %}
    {% if post.category contains 'paper' %}
      {% assign currentdate = post.date | date: "%Y" %}
      {% if currentdate != date %}
        <h3 class="post-cat-title" id="y{{currentdate}}">{{ currentdate }}</h3>
        {% assign date = currentdate %}
      {% endif %}
        {% include paper-list-item.html
          title=post.title
          thumb=post.thumb
          url=post.url
          authors=post.authors
          venue=post.venue
          bestPaper=post.bestPaper
          honorable=post.honorable
          pdf=post.pdf
          supplementary=post.supplementary
          github=post.github
          additionals=post.additionals
        %}
    {% endif %}
  {% endfor %}
</div>
