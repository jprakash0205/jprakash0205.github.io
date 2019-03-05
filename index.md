---
layout: default
title:  "Posts"
---

## Articles

{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
      <p>{{ post.excerpt | strip_html | truncatewords:75 }}</p>
    {% endfor %}
  </ul>
{% endfor %}
