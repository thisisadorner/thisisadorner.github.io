---
layout: default
title: Home
---

# [YOUR HOMEPAGE HEADLINE]

[YOUR INTRODUCTION PARAGRAPH]

## Recent Posts

<ul class="post-list">
{% for post in site.posts limit:5 %}
  <li class="post-list-item">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
    <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    <a href="{{ post.url | relative_url }}" class="read-more">Read more →</a>
  </li>
{% endfor %}
</ul>

[View all posts →](/blog)

## Featured Projects

[YOUR PROJECTS SECTION]

[View all projects →](/projects)
