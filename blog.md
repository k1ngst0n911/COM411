---
layout: default
title: Blog
permalink: /blog/
---

<h1>{{ page.title }}</h1>

<div class="tile-grid">
  {% for post in site.posts %}
    <a class="tile" href="{{ post.url | relative_url }}">
      {% if post.image %}
        <img class="tile-img" src="{{ post.image | relative_url }}" alt="">
      {% endif %}
      <div class="tile-body">
        <div class="tile-title">{{ post.title }}</div>
        {% if post.description %}
          <div class="tile-desc">{{ post.description }}</div>
        {% endif %}
        <div class="tile-meta">{{ post.date | date: "%b %d, %Y" }}</div>
      </div>
    </a>
  {% endfor %}
</div>
