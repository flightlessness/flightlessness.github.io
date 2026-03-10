---
layout: default
title: Test
permalink: /test/

# SEO
description: Posts categorized under Test.
keywords: [test, experiments, drafts]
canonical_url: https://flightlessness.github.io/test/

# Display options
intro: Experimental posts and development notes.
cover_image: /assets/images/test-banner.jpg

# Behavior flags
show_date: true
show_post_count: true
hidden: false

# Navigation ordering
nav_order: 3

# Optional custom styling
body_class: category-test

# Future-proofing
paginate: 10
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
