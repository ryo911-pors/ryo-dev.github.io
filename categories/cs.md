---
layout: page
title: CS
permalink: /categories/cs/
---

Posts on computer science — systems, algorithms, engineering fundamentals.

{% assign posts = site.posts | where_exp: "post", "post.categories contains 'CS'" %}
{% if posts.size == 0 %}
*No posts yet.*
{% else %}
<ul>
{% for post in posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span style="color: #888; font-size: 0.85em;"> — {{ post.date | date: "%Y-%m-%d" }}</span>
  </li>
{% endfor %}
</ul>
{% endif %}
