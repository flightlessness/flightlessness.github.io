---
layout: default
title: Categories
permalink: /categories/
---

<h1>Categories</h1>

<ul>
  {% for category in site.categories %}
    <li>
      <a href="/{{ category[0] }}/">
        {{ category[0] | capitalize }}
      </a>
    </li>
  {% endfor %}
</ul>
