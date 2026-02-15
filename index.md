---
layout: default
title: Quiet Uptime
permalink: /
---

<div class="post">
  <header class="post-header">
    <h1 class="post-title">Quiet Uptime</h1>
    <p class="post-description">Short journals on memory, systems, and growth.</p>

    <p class="text-muted">
      <a href="/journal/">Journal</a>
      · <a href="/about/">About</a>
      · <a href="/feed.xml">RSS</a>
    </p>
  </header>

  <article>
    <h2>Recent</h2>
    <ul>
      {% assign recent = site.posts | where_exp: "p", "p.categories contains 'journal'" | slice: 0, 7 %}
      {% for post in recent %}
        <li>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <span class="text-muted">— {{ post.date | date: "%Y-%m-%d" }}</span>
        </li>
      {% endfor %}
    </ul>

    <p class="text-muted" style="margin-top: 1rem">
      Minimal by design. If it feels too quiet, that’s the point.
    </p>
  </article>
</div>
