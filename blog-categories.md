---
layout: page
permalink: /blog/categories/
title: Categories
---

{% for category in site.categories %}
  {% capture category_name %}{{ category | first }}{% endcapture %}
  <div id="#{{ category_name | slugize }}">
    <h3>{{ category_name | capitalize }}</h3>
    <ul>
      {% for post in site.categories[category_name] %}
      <li>
        <a href="{{ post.url | downcase | relative_url }}">{{ post.title }}</a>
      </li>
      {% endfor %}
    </ul>
  </div>
{% endfor %}
