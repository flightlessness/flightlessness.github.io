---
layout: default
title: Test
permalink: /testing/
---

<h1>Testing</h1>

<ul class="post-list">
  {% assign posts = site.posts | where: "type", "testing" | sort: "date" | reverse %}
  {% for post in posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <small>{{ post.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
