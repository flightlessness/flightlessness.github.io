---
layout: default
title: Categories
permalink: /categories/
---

<h1>Categories</h1>

<ul>
  {% assign sorted_categories = site.categories | sort %}
  {% for category in sorted_categories %}
    {% assign name = category[0] %}
    {% assign posts = category[1] %}
    <li>
      <a href="/{{ name | uri_escape }}/">
        {{ name | capitalize }} ({{ posts | size }})
      </a>
    </li>
  {% endfor %}
</ul>