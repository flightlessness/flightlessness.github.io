---
layout: default
title: Music
category: music
permalink: /music/
---

<h1>{{ page.title }}</h1>

{% assign posts = site.categories[page.category] %}

{% if posts and posts != empty %}
  {% assign posts = posts | sort: "date" | reverse %}
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
  <p>This category is ready. Posts will appear here soon.</p>
{% endif %}