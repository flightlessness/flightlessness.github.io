---
layout: default
title: Archive
permalink: /archive/
---

<h1>Archive</h1>

{% assign posts = site.posts | sort: "date" | reverse %}

<ul class="post-list">
  {% for post in posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <small>{{ post.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
