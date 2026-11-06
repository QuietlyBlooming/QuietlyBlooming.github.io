---
layout: page
title: Travel
permalink: /travel/
---

<p class="category-intro">
Places I've been, moments I've collected, and stories from the road.
</p>

{% assign category_posts = site.categories.travel %}

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
No stories here yet. Perhaps the next journey will begin soon.
</p>

{% endif %}
