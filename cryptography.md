---
layout: page
title: 🔐 Cryptography
permalink: /cryptography/
---

# Cryptography

Exploring the mathematical foundations of secure communication and computation.

## Topics

- **MPC (Multi-Party Computation)** - Secure computation without revealing inputs
- **Zero-Knowledge Proofs** - Prove statements without revealing secrets
- **Threshold Signatures** - Distributed key generation and signing
- **Post-Quantum Cryptography** - Preparing for the quantum era

## Posts

{% assign posts = site.posts | where: "category", "cryptography" %}
{% for post in posts limit:10 %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}

{% if posts.size == 0 %}
*No posts yet. Coming soon!*
{% endif %}
