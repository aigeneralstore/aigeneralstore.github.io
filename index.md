---
layout: home
title: Home
---

## All Posts

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: "%Y-%m-%d" }} • {{ post.category }}
{% endfor %}

{% if site.posts.size == 0 %}
*No posts yet.*
{% endif %}
