---
layout: default
title: Blog
permalink: /blog/
---

<h1>{{ page.title }}</h1>

<div class="tile-grid compact-tiles">
  {% for post in site.posts %}
    <a class="tile" href="{{ post.url | relative_url }}">
      {% if post.image %}
        <img class="tile-thumb" src="{{ post.image | relative_url }}" alt="">
      {% endif %}
      <div class="tile-body">
        <div class="tile-title">{{ post.title }}</div>
        <div class="tile-meta">{{ post.date | date: "%b %d, %Y" }}</div>
      </div>
    </a>
  {% endfor %}
</div>
