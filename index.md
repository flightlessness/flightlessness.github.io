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
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>{{ post.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>

<h2>
  <a href="{{ '/books/' | relative_url }}">Bookshelf</a>
</h2>

<p>
  <a href="{{ '/books/' | relative_url }}">View my bookshelf →</a>
</p>

<h2>
  <a href="{{ '/categories/' | relative_url }}">Categories</a>
</h2>

<ul class="category-menu">
  {% for category in site.categories %}
    <li>
      <a href="{{ '/' | append: category[0] | append: '/' | relative_url }}">
        {{ category[0] | capitalize }}
      </a>
    </li>
  {% endfor %}
</ul>
