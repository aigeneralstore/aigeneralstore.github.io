---
layout: page
title: ⛓️ Blockchain
permalink: /blockchain/
---

# Blockchain

Building the future of decentralized systems.

## Topics

- **Wallet Security** - Key management, signing, and user experience
- **Smart Contracts** - Solidity, audits, and best practices
- **Multi-Chain** - Ethereum, Solana, Bitcoin, and beyond
- **Enterprise Solutions** - Custody, compliance, and infrastructure

## Posts

{% assign posts = site.posts | where: "category", "blockchain" %}
{% for post in posts limit:10 %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}

{% if posts.size == 0 %}
*No posts yet. Coming soon!*
{% endif %}
