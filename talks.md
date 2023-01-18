---
layout: default
title: "Talks"
---

{% assign data = site.data.talks %}

<div class="main-section-wrap">
  <section class="talk-list">
  <h3 class="post-cat-title">Selected Online Talks and Interviews</h3>
  {% for item in data %}
    {% include talk-item.html
      title=item.title
      contributor=item.contributor
      venue=item.venue
      year=item.year
      link=item.link %}
  {% endfor %}
  </section>
</div>