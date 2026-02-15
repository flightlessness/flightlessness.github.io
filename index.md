---
layout: default
title: Home
permalink: /
---

<h1>Latest</h1>

<ul class="post-list">
  {% assign latest_posts = site.posts | sort: "date" | reverse | slice: 0, 10 %}
  {% for post in latest_posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <small>
        {{ post.date | date: "%b %-d, %Y" }}
        {% if post.type %}
          · <a href="/{{ post.type }}/">{{ post.type | capitalize }}</a>
        {% endif %}
      </small>
    </li>
  {% endfor %}
</ul>

<h2>Categories</h2>

<ul class="category-menu">
  <li><a href="/test/">Test</a></li>
  <li><a href="/hotel/">Hotel</a></li>
  <li><a href="/image/">Image</a></li>
</ul>

Welcome to my blog.

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}
