---
layout: page
permalink: /blog/
title: Blog
description: Blog
tags:
---

<ul>
  {% for post in site.posts %}
  <li>
    <a href="{{ post.url | downcase | relative_url }}">
      {{ post.title }}
    </a>
  </li>
  {% endfor %}
</ul>
