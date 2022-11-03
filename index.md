---
layout: default
title: "Home"
---
<div class="main-wrap">
  <div class="text">
    {% for text in site.data.home_text %}
      <p class="home-display">{{text}}</p>
    {% endfor %}
  </div>
  <div class="image-grid">
    {% for image in site.data.home_images %}
       {% include home-image.html url=image.url img=image.img alt=image.alt %}
    {% endfor %}
  </div>
</div>
