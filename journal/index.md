---
layout: page
title: Journal
permalink: /journal/
nav: true
nav_order: 1
---

{% assign recent = site.posts | where_exp: "p", "p.categories contains 'journal'" %}

<ul>
{% for post in recent %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="text-muted">— {{ post.date | date: "%Y-%m-%d" }}</span>
  </li>
{% endfor %}
</ul>
