---
layout: default
date: 2020-10-01
permalink: /blog/
categories:
description: Blog
tags:
title: Blog
---

<table class="accounts" width="100%" border="0">
  {% for post in site.posts %}
  <tr>
    <td width="auto">
       <a href="{{ post.url | relative_url }}">
         {{ post.title }}
       </a>
    </td>
  </tr>
  {% endfor %}
</table>
