<ul>
  {% for category in site.categories %}
    {% capture category_name %}{{ category | first }}{% endcapture %}
    {% if category_name == "Life" %}
      {% assign sorted = site.categories[category_name] | sort: 'date' | reverse  %}
      {% for post in sorted %}
        <li>
          <a href="{{ post.url | downcase | relative_url }}">
            {{ post.date | date: '%Y/%m/%d' }}: <b>{{ post.title }}</b>
          </a>
        </li>
      {% endfor %}
    {% endif %}
  {% endfor %}
</ul>
