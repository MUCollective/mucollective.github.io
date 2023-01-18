---
layout: default
title: "Software and Demo"
---

<div class="main-section-wrap">
  <div class="title-wrap">
    <h3>Open-sourced Software Products</h3>
  </div>
  <section class="software-list">
  {% for item in site.data.software %}
    {% include software-item.html
      title=item.title
      id=item.id
      contributor=item.contributor
      type=item.type
      description=item.description
      supplement=item.supplement %}
  {% endfor %}
  </section>
</div>

<div class="main-section-wrap">
  <div class="title-wrap">
    <h3>Research Prototypes</h3>
  </div>
  <section class="software-list">
  {% for item in site.data.prototype %}
    {% include software-item.html
      title=item.title
      id=item.id
      contributor=item.contributor
      type=item.type
      description=item.description
      supplement=item.supplement %}
  {% endfor %}
  </section>
</div>
