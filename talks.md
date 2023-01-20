---
layout: default
title: "Selected Talks"
# subtitle: "Selected Online Talks and Interviews"
---

{% assign data = site.data.talks %}

<div class="main-section-wrap">
  <section class="talk-list">
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