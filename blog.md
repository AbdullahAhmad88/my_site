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
    <img src="{{ post.image }}">
  {% endif %}

  <p>{{ post.excerpt }}</p>
</div>
{% endfor %}
