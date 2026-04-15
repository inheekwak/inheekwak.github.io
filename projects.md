---
layout: default
title: Projects
permalink: /projects/
---

<div class="projects-grid">
  {% for p in site.projects %}
    {% include project-card.html project=p %}
  {% endfor %}
</div>
