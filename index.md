---
layout: home
title: Home
---

# Welcome to My Blog 👋

This is my personal tech blog where I share:

- 🔐 **Blockchain Security** - Wallets, smart contracts, cryptography
- 🤖 **AI & Automation** - Agent swarms, LLM applications
- 💻 **Engineering** - Tools, architecture, best practices

## Recent Posts

{% for post in site.posts limit:5 %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}

## About Me

Blockchain practitioner focused on security and user experience. Currently exploring AI-powered development workflows.

- GitHub: [@aigeneralstore](https://github.com/aigeneralstore)
