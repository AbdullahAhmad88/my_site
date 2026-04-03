---
layout: default
title: Blog
---

# Blog

{% for post in site.posts %}
<div class="post-card">
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p>{{ post.date | date: "%B %d, %Y" }}</p>

  {% if post.image %}
    <img src="{{ post.image }}" alt="{{ post.title }}">
  {% endif %}

  <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
</div>
{% endfor %}
