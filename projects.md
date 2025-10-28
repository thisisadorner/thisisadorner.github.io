---
layout: page
title: Projects
---

[YOUR PROJECTS INTRO]

<div class="project-list">
{% for project in site.projects %}
  <div class="project-card">
    <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
    <div class="project-meta">
      <strong>Status:</strong> {{ project.status }} | 
      <strong>Tech:</strong> {{ project.tech }}
    </div>
    <div class="project-description">
      {{ project.excerpt }}
    </div>
    <a href="{{ project.url | relative_url }}" class="read-more">View project →</a>
  </div>
{% endfor %}
</div>
