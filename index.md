---
layout: default
title: Home
permalink: /
---

<h2>Latest</h2>

<ul class="post-list">
  {% assign latest_posts = site.posts | sort: "date" | reverse | slice: 0, 10 %}
  {% for post in latest_posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <small>
        {{ post.date | date: "%b %-d, %Y" }}
      </small>
    </li>
  {% endfor %}
</ul>

<h2>Categories</h2>

<ul class="category-menu">
  {% assign types = site.posts | map: "type" | uniq | compact %}
  {% for type in types %}
    <li>
      <a href="/{{ type }}/">{{ type | capitalize }}</a>
    </li>
  {% endfor %}
</ul>
