---
layout: home
title: "Home"
---
<section class="main-section-wrap display-text">
  <div class="text">
    {% for text in site.data.home_text %}
      <p class="home-display">{{text}}</p>
    {% endfor %}
  </div>
</section>

<section class="main-section-wrap">
  <div class="title-wrap">
    <h3>News</h3>
  </div>
  {% for news in site.data.home_news %}
    {% include home-news.html title=news.title date=news.date content=news.content %}
  {% endfor %}
</section>

<section class="main-section-wrap">
  <div class="title-wrap">
    <h3>Research Areas</h3>
  </div>
  <div class="image-grid">
    {% for item in site.data.research_areas %}
       {% include research-area-thumb.html
          name=item.name
          category=item.category
          desc=item.desc
        %}
    {% endfor %}
  </div>

</section>

<section class="main-section-wrap">
  <div class="title-wrap">
    <h3>Recent Papers</h3>
    <a href="/mucollective.co/publications/">See all</a>
  </div>
  {% for post in site.posts | limit: 10 %}
    {% if post.category contains 'paper' %}
      {% assign currentdate = post.date | date: "%Y" %}
      {% if currentdate != date %}
        <h3 class="paper-year-title" id="y{{currentdate}}">{{ currentdate }}</h3>
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
