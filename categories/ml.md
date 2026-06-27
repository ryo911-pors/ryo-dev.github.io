---
layout: page
title: ML
permalink: /categories/ml/
---

Posts on machine learning — experiments, Kaggle, algorithms, and tooling.

{% assign posts = site.posts | where_exp: "post", "post.categories contains 'ML'" %}
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
