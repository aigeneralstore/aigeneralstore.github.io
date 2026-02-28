---
layout: page
title: "🤖 AI Agents"
permalink: /ai-agents/
---

# AI Agents

Building autonomous systems that can think, plan, and execute.

## Topics

- **Agent Architecture** - Orchestration, memory, and tool use
- **Code Agents** - Automating development workflows
- **Multi-Agent Systems** - Coordination and swarm intelligence
- **LLM Engineering** - Prompting, RAG, and fine-tuning

## Posts

{% assign posts = site.posts | where: "category", "ai-agents" %}
{% for post in posts limit:10 %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}

{% if posts.size == 0 %}
*No posts yet. Coming soon!*
{% endif %}
