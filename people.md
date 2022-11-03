---
layout: default
title: "People"
---

<div class="posts-wrap">
  <div class="title-wrap">
    <h2>Faculty</h2>
  </div>
  <section class="people-grid">
  {% for person in site.data.people.faculty %}
    {% include people-item.html
      name=person.name
      role=person.role
      department=person.department
      school=person.school
      image=person.image
      link=person.image %}
  {% endfor %}
  </section>
</div>

<div class="posts-wrap">
  <div class="title-wrap">
    <h2>Post Docs and Graduate Students</h2>
  </div>
  <section class="people-grid">
  {% for person in site.data.people.current %}
    {% include people-item.html
      name=person.name
      role=person.role
      department=person.department
      school=person.school
      image=person.image
      link=person.image %}
  {% endfor %}
  </section>
</div>

<div class="posts-wrap">
  <div class="title-wrap">
    <h2>Alumni</h2>
  </div>
  <div class="alumni-list-wrap">
    <ul class="people-list">
      {% for person in site.data.people.alumni %}
        {% if person.link %}
        <li><a href="{{person.link}}" target="_blank">{{person.name}}</a>, {{person.position}}</li>
        {% else %}
        <li><span class="name">{{person.name}}</span>, {{person.position}}</li>
        {% endif %}
      {% endfor %}
    </ul>
    <ul class="people-list">
      {% for person in site.data.people.alumni2 %}
        <li><span class="name">{{person.name}}</span></li>
      {% endfor %}
    </ul>
  </div>
</div>
