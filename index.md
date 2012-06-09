---
layout: page
title: Origin World
---
{% include JB/setup %}

## My Blog Posts

<ul class="posts">
  {% for post in site.posts limit:10 offset:1 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
