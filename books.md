---
layout: default
title: Bookshelf
permalink: /books/
---

<section class="books-page">
  <h1>Bookshelf</h1>
  <p>Books I have read, collected, or want to remember.</p>

  <div class="bookshelf">
    {% for book in site.books %}
      <a class="book-card" href="{{ book.url | relative_url }}">
        <img src="{{ book.cover | relative_url }}" alt="{{ book.title }}">
        <h2>{{ book.title }}</h2>
        {% if book.author %}
          <p>{{ book.author }}</p>
        {% endif %}
      </a>
    {% endfor %}
  </div>
</section>
