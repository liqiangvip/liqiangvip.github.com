---
layout: page
title: Home
---
{% include JB/setup %}

{% assign last_post = site.posts.first %}

# {{ last_post.title }}
<hr>

{{ last_post.content }}

[Click to view the comments on this post]({{ last_post.url }})
<hr>
# Older Posts

<ul class="posts" style="margin-top:10px">
  {% for post in site.posts limit:10 offset:1 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
