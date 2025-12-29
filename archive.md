---
layout: page
title: Archive
permalink: /archive/
---

## All Posts

<div class="archive-list">
{% for post in site.posts %}
  <article class="archive-item">
    <h3>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    <p class="post-meta">
      <time datetime="{{ post.date | date_to_xmlschema }}">
        {{ post.date | date: "%B %-d, %Y" }}
      </time>
      {% if post.categories.size > 0 %}
        • 
        {% for category in post.categories %}
          <span class="category">{{ category }}</span>
        {% endfor %}
      {% endif %}
    </p>
    <div class="post-excerpt">
      {{ post.excerpt }}
    </div>
  </article>
{% endfor %}
</div>

{% if site.posts.size == 0 %}
<p>No posts yet. Check back soon!</p>
{% endif %}
