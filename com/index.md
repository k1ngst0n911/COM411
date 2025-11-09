---
layout: default
title: "COM411 - Series Index"
permalink: /com/
---

{% assign parts = site.com | sort: "order" %}
{% if parts.size == 0 %}
<p>No parts yet. Add files under <code>_com/</code> with front matter including <code>order:</code>.</p>
{% else %}
<ol>
{% for p in parts %}
  <li>
    <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
    {% if p.description %} — {{ p.description }}{% endif %}
  </li>
{% endfor %}
</ol>
{% endif %}
