---
layout: page
permalink: /blog/
title: Blog
description: Blog
tags:
---

<table width="100%" border="0">
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
