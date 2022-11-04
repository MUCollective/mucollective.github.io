---
layout: default
title: "Research"
---

<div class="posts-wrap">
  <div class="title-wrap">
    <h2>Research areas</h2>
  </div>
  {% for topic in site.data.research_areas %}
    <section class="research-area">
      <h3>{{topic.name}}</h3>
      {% if topic.desc %}
        <p>{{topic.desc}}</p>
      {% endif %}
      <h4>Related papers</h4>
      <div class="paper-grid">
        {% for post in site.posts %}
          {% if post.category contains 'paper' and post.category contains topic.cat %}
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
      </div>
    </section>
  {% endfor %}
</div>
