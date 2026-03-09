---
layout: default
title: Archive
permalink: /archive/
---

<h1>Archive</h1>

<ul class="post-list">
  {% for post in site.posts | sort: "date" | reverse %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <small>{{ post.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
