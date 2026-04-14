---
layout: default
title: Blog
permalink: /blog/
---

# Blog

<ul class="post-list" style="list-style: none; padding-left: 0;">
  {% for post in site.posts %}
    <li style="margin-bottom: 30px; border-bottom: 1px solid #eee; padding-bottom: 15px;">
      <span style="color: #888; font-size: 0.85rem;">{{ post.date | date: "%B %d, %Y" }}</span>
      <br>
      <a href="{{ post.url | relative_url }}" style="font-size: 1.25rem; font-weight: bold; text-decoration: none; color: #13294B;">
        {{ post.title }}
      </a>
      <p style="margin-top: 10px; color: #444;">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
    </li>
  {% endfor %}
</ul>

{% if site.posts.size == 0 %}
  <p>Coming soon! I'll be sharing my thoughts on AI, mental health, and my journey across the US.</p>
{% endif %}
