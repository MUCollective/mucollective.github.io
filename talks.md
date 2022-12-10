---
layout: default
title: "Talks"
---

{% assign data = site.data.talks | sort: 'year' | reverse %}

<div class="main-section-wrap">
  <section class="talk-list">
  {% for item in data %}
    {% assign currentdate = item.year %}
    {% if currentdate != date %}
      <h3 class="post-cat-title" id="y{{currentdate}}">{{ currentdate }}</h3>
      {% assign date = currentdate %}
    {% endif %}
    {% include talk-item.html
      title=item.title
      contributor=item.contributor
      venue=item.venue
      link=item.link %}
  {% endfor %}
  </section>
</div>
