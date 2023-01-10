---
layout: default
title: "Research"
---

{% for topic in site.data.research_areas %}
  <section class="main-section-wrap research-area">
  <a name="{{ topic.category }}"></a>
    <div class="title-wrap">
      <h3>{{topic.name}}</h3>
    </div>
    <div class="content-wrap">
    {% if topic.desc %}
      <p>{{topic.desc}}</p>
    {% endif %}
    {% if topic.image %}
      <div class="image-wrap">
        {% for image in topic.image %}
        <img src="{{image | relative_url}}" alt="{{topic.name}} description image" />
        {% endfor %}
      </div>
    {% endif %}
    </div>
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
            url=item.link
          %}
        {% endif %}
      {% endfor %}
    </div>
  </section>
{% endfor %}
