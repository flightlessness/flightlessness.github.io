---
layout: default
title: Categories
permalink: /categories/
---

<h1>Categories</h1>

<ul>
  {% assign types = site.posts | map: "type" | uniq | compact %}
  {% for type in types %}
    <li>
      <a href="/{{ type }}/">{{ type | capitalize }}</a>
    </li>
  {% endfor %}
</ul>
