---
layout: default
title: Bookshelf
permalink: /books/
---

<div class="bookshelf">
  {% for book in site.books %}
  <a class="book-card" href="{{ book.url | relative_url }}">
    <img src="{{ book.cover | relative_url }}" alt="{{ book.title }}">
    <div class="book-title">{{ book.title }}</div>
    <div class="book-author">{{ book.author }}</div>
  </a>
  {% endfor %}
</div>
