---
layout: default
title: Projects
---

<h1>Projects</h1>

<ul class="projects">
{% for project in site.projects %}
  <li><a href="{{ project.url | relative_url }}">{{ project.title }}</a></li>
{% endfor %}
</ul>
