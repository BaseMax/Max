---
layout: page
permalink: /blog/
title: Blog
description: Blog
tags:
---

{% assign sorted = site.posts | sort: 'date' | reverse  %}
<ul>
	{% for post in sorted %}
	<li>
		<a href="{{ post.url | downcase | relative_url }}">
			{{ post.date | date: '%Y/%m/%d' }}: {{ post.title }}
		</a>
	</li>
	{% endfor %}
</ul>

<h2>Categories</h2>

{% for category in site.categories %}
  {% capture category_name %}{{ category | first }}{% endcapture %}
  <div id="#{{ category_name | slugize }}">
    <h3>{{ category_name | capitalize }}</h3>
    <ul>
      {% for post in site.categories[category_name] %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </li>
      {% endfor %}
    </ul>
  </div>
{% endfor %}
