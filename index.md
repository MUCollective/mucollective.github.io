---
layout: home
title: "Home"
---

<!-- <section class="main-section-wrap">
  <div class="title-wrap">
    <h3>News</h3>
  </div>
  {% for news in site.data.home_news %}
    {% include home-news.html title=news.title date=news.date content=news.content %}
  {% endfor %}
</section> -->

<!-- <section class="main-section-wrap">
  <div class="title-wrap">
    <h3>Research Areas</h3>
  </div>
  <div class="image-grid">
    {% for item in site.data.research_areas %}
       {% include research-area-thumb.html
          name=item.name
          category=item.category
          desc=item.desc
          image=item.image
        %}
    {% endfor %}
  </div>
</section> -->

<section class="main-section-wrap">
  <div class="title-wrap">
    <h3>Recent Papers</h3>
    <a href="/publications">See all <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi bi-caret-right-fill" viewBox="0 0 16 16">
  <path d="m12.14 8.753-5.482 4.796c-.646.566-1.658.106-1.658-.753V3.204a1 1 0 0 1 1.659-.753l5.48 4.796a1 1 0 0 1 0 1.506z"/>
</svg></a>
  </div>
  {% for post in site.posts | limit: 10 %}
    {% if post.category contains 'paper' %}
      {% assign currentdate = post.date | date: "%Y" %}
      {% if currentdate != date %}
        <!-- <h3 class="paper-year-title" id="y{{currentdate}}">{{ currentdate }}</h3> -->
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
</section>
