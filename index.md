---
layout: default
title: "COM Anatomy — Series Index"
permalink: /com/
---

{% assign parts = site.com | sort: "order" %}
<ol>
{% for p in parts %}
  <li>
    <a href="{{ p.url }}">{{ p.title }}</a>
    {% if p.description %} — {{ p.description }}{% endif %}
  </li>
{% endfor %}
</ol>
