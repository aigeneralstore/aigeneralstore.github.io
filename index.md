---
layout: home
title: Home
---

# Welcome 👋

I write about building secure, intelligent systems.

## All Posts

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: "%Y-%m-%d" }} • {{ post.category }}
{% endfor %}

{% if site.posts.size == 0 %}
*No posts yet.*
{% endif %}

---

**About** — Blockchain practitioner focused on security and user experience.

GitHub: [@aigeneralstore](https://github.com/aigeneralstore)
