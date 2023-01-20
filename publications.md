---
layout: default
title: "Publications"
---

<div class="main-section-wrap">
  <!-- <div class="search-wrap">
    <div class="form-row">
      <label for="paper-search">Search by title or author name</label>
      <input name="paper-search" id="paper-search" type="text" onkeyup=" search(event)" />
    </div>
    <div class="year-filters form-row">
      <label for="paper-year">Filter by year</label>
      <div id="year-buttons"></div>
    </div>
    <div class="category-filters form-row">
      <label for="paper-year">Filter by categories</label>
      <div id="category-buttons"></div>
    </div>
    <div class="form-row">
      <label><span id="n-papers"></span> paper(s)</label>
      <button id="clear-all" onclick="clear_all()">Clear all</button>
    </div>
  </div> -->
  {% for post in site.posts %}
    {% if post.category contains 'paper' %}
      {% assign currentdate = post.date | date: "%Y" %}
      {% if currentdate != date %}
        <div class="title-wrap">
          <h3>{{ currentdate }}</h3>
        </div>
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
          category=post.category
          year=currentdate
        %}
    {% endif %}
  {% endfor %}
</div>
