---
layout: default
title: Education
---

# Education

Here is my educational background:

{% for edu in site.education %}
  <div class="education">
    <h2>{{ edu.degree }}</h2>
    <p>{{ edu.institution }}, {{ edu.date }}</p>
    <p>{{ edu.description }}</p>
  </div>
{% endfor %}
