---
layout: default
title: "Papers"
---

<div class="posts-wrap">
  <div class="title-wrap">
    <h2>Papers</h2>
  </div>
  {% for post in site.posts %}
    {% if post.category == 'paper' %}
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
