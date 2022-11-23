<ul>
  {% for category in site.categories %}
    {% if post.title == "Technology" %}
      {% for post in category.last %}
        <li>
          <a href="{{ post.url | downcase | relative_url }}">
            {{ post.title }}
          </a>
        </li>
      {% endfor %}
    {% endif %}
  {% endfor %}
</ul>
