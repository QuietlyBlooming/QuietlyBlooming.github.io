---
layout: page
title: Thoughts
permalink: /thoughts/
---

<p class="category-intro">
Notes on life, personal reflections, and thoughts that come and go.
</p>

{% assign category_posts = site.categories.thoughts %}

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
Some thoughts are still finding their words.
</p>

{% endif %}
