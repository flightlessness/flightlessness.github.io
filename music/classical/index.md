---
layout: default
title: Classical Music
permalink: /music/classical/
---

<h1>{{ page.title }}</h1>

<ul class="post-list">
  {% assign posts = site.categories.classical | sort: "date" | reverse %}
  {% for post in posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <small>{{ post.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
