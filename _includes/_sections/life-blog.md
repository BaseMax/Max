<ul>
  {% for category in site.categories %}
    {{ category.title }}
    {% if category.title == "Technology" %}
      {% assign sorted = category.last | sort: 'date' | reverse  %}
      {% for post in sorted %}
        <li>
          <a href="{{ post.url | downcase | relative_url }}">
            {{ post.title }}
          </a>
        </li>
      {% endfor %}
    {% endif %}
  {% endfor %}
</ul>
