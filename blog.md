---
layout: page
title: Blog
---

<ul class="post-list">
{% for post in site.posts %}
  <li class="post-list-item">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
    {% if post.excerpt %}
    <p>{{ post.excerpt | strip_html | truncatewords: 40 }}</p>
    {% endif %}
    <a href="{{ post.url | relative_url }}" class="read-more">Read more →</a>
  </li>
{% endfor %}
</ul>
