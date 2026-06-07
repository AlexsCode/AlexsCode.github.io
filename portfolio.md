---
layout: default
title: Portfolio
description: "Projects by Alex Tuddenham — mobile network latency monitor, ISO 7816 SIM card reader, car parking sensor HUD, and confidential alarm communicator."
permalink: /portfolio/
---

# Portfolio

{% for project in site.portfolio %}
<div class="portfolio-entry">
  <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
  {% if project.period %}
    <span class="cv-period">{{ project.period }}</span>
  {% endif %}
  {% if project.subtitle %}
    <p class="subtitle">{{ project.subtitle }}</p>
  {% endif %}
  <p>{{ project.excerpt | strip_html | truncate: 200 }}</p>
  {% if project.tech %}
  <div class="project-tech">
    {% for t in project.tech %}<span class="tech-tag">{{ t }}</span>{% endfor %}
  </div>
  {% endif %}
</div>
<hr>
{% endfor %}

{% if site.portfolio.size == 0 %}
<p class="placeholder">
  No projects yet. Create markdown files in <code>_portfolio/</code> to add projects.
</p>
{% endif %}
