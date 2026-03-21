---
layout: default
title: Classical Music
permalink: /music/classical/
---

<h1>{{ page.title }}</h1>

{% assign posts = site.categories.classical %}

{% if posts and posts != empty %}
  {% assign posts = posts | sort: "date" | reverse %}
  <ul class="post-list">
    {% for post in posts %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <small>{{ post.date | date: "%b %-d, %Y" }}</small>
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p>No classical music posts yet.</p>
{% endif %}
