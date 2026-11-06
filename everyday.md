---
layout: page
title: Everyday
permalink: /everyday/
---

<p class="category-intro">
Little moments, ordinary days, and the beauty of everyday life.
</p>

{% assign category_posts = site.categories.everyday %}

{% if category_posts and category_posts.size > 0 %}

<ul class="post-list">
  {% for post in category_posts %}
    <li>
      <span class="post-meta">
        {{ post.date | date: "%B %-d, %Y" }}
      </span>

      <a class="post-link" href="{{ post.url | relative_url }}">
        {{ post.title | escape }}
      </a>

      <div class="post-excerpt">
        {{ post.excerpt | strip_html }}
      </div>
    </li>
  {% endfor %}
</ul>

{% else %}

<p class="category-empty">
A collection of little moments, coming soon.
</p>

{% endif %}
