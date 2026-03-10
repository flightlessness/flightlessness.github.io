---
layout: default
title: Music
permalink: /music/
---

<h1>{{ page.title }}</h1>

<h2>All Music Posts</h2>

<ul class="post-list">
  {% assign posts = site.categories.music | sort: "date" | reverse %}
  {% for post in posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <small>{{ post.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>

<h2>Subcategories</h2>

<ul>
  {% assign subcats = site.categories.music | map: "categories" | flatten | uniq %}
  {% for cat in subcats %}
    {% unless cat == "music" %}
      <li>
        <a href="/music/{{ cat }}/">{{ cat | capitalize }}</a>
      </li>
    {% endunless %}
  {% endfor %}
</ul>
