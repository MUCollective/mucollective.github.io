---
layout: default
title: "Selected Talks"
---

{% assign data = site.data.talks %}

<div class="main-section-wrap">
  <section class="talk-list">
  <h3 class="post-cat-title">Conference Keynotes</h3>
  {% for item in data %}
    {% if item.type == 'conference-keynotes' %}
      {% include talk-item.html
        title=item.title
        contributor=item.contributor
        venue=item.venue
        year=item.year
        link=item.link %}
    {% endif %}
  {% endfor %}
  </section>
</div>

<div class="main-section-wrap">
  <section class="talk-list">
  <h3 class="post-cat-title">Invited Talks and Panels</h3>
  {% for item in data %}
    {% if item.type == 'invited' %}
      {% include talk-item.html
        title=item.title
        contributor=item.contributor
        venue=item.venue
        year=item.year
        link=item.link %}
    {% endif %}
  {% endfor %}
  </section>
</div>

<div class="main-section-wrap">
  <section class="talk-list">
  <h3 class="post-cat-title">Podcasts and Webcasts</h3>
  {% for item in data %}
    {% if item.type == 'cast' %}
      {% include talk-item.html
        title=item.title
        contributor=item.contributor
        venue=item.venue
        year=item.year
        link=item.link %}
    {% endif %}
  {% endfor %}
  </section>
</div>
