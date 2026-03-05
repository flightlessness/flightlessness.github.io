---
layout: default
title: Test
permalink: /test/
---

<h1>{{ page.title }}</h1>

{% assign category_name = page.title | downcase %}

{% assign posts = site.posts
  | where: "type", category_name
  | sort: "date"
  | reverse %}

{% if posts.size > 0 %}
  <ul class="post-list">
    {% for post in posts %}
      <li class="post-item">
        <a class="post-title" href="{{ post.url }}">
          {{ post.title }}
        </a>
        <small class="post-date">
          {{ post.date | date: "%b %-d, %Y" }}
        </small>
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p>No posts in this category yet.</p>
{% endif %}
