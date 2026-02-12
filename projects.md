---
layout: default
title: Projects
---

# My Projects

Here are some of the projects I've worked on:

{% for project in site.projects %}
  <div class="project">
    <h2><a href="{{ project.url }}">{{ project.title }}</a></h2>
    <p>{{ project.description }}</p>
  </div>
{% endfor %}
