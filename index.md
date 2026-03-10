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
      <small>{{ post.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>

<h2>
  <a href="{{ '/categories/' | relative_url }}">Categories</a>
</h2>

<ul class="category-menu">
  <ul class="category-menu">
  {% for category in site.categories %}
    <li>
      <a href="/{{ category[0] }}/">
        {{ category[0] | capitalize }}
      </a>
    </li>
  {% endfor %}
</ul>
  {% for type in types %}
    <li>
      <a href="/{{ type }}/">{{ type | capitalize }}</a>
    </li>
  {% endfor %}
</ul>
