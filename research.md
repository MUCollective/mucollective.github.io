---
layout: default
title: "Research"
---

{% for topic in site.data.research_areas %}
  <section class="main-section-wrap research-area">
    <div class="title-wrap">
      <h3>{{topic.name}}</h3>
    </div>
    {% if topic.desc %}
      <p>{{topic.desc}}</p>
    {% endif %}
    <h4>Related contributions</h4>
    <div class="paper-grid">
      {% for post in site.posts %}
        {% if post.category contains 'paper' and post.category contains topic.category %}
          {% assign year = post.date | date: "%Y" %}
          {% include paper-thumb-item.html
            title=post.title
            thumb=post.thumb
            url=post.url
            authors=post.authors
            venue=post.venue
            year=year
          %}
        {% endif %}
      {% endfor %}
      {% for item in site.data.software %}
        {% if item.category contains topic.category %}
          {% include software-thumb-item.html
            title=item.title
            contributor=item.contributor
            type=item.type
            supplement=item.supplement
          %}
        {% endif %}
      {% endfor %}
      {% for item in site.data.prototype %}
        {% if item.category contains topic.category %}
          {% include software-thumb-item.html
            title=item.title
            contributor=item.contributor
            type=item.type
            supplement=item.supplement
          %}
        {% endif %}
      {% endfor %}
      {% for item in site.data.talks %}
        {% if item.category contains topic.category %}
          {% include talk-thumb-item.html
            title=item.title
            contributor=item.contributor
            link=item.link
          %}
        {% endif %}
      {% endfor %}
    </div>
  </section>
{% endfor %}