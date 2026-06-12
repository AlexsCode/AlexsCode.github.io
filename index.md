---
layout: default
title: Home
description: "Alex Tuddenham — Solution Architect & IoT Engineering Specialist. eSIM SGP.32 architecture, cellular IoT, embedded systems. GSMA eSIM work group member."
---

# Hi, I'm Alex Tuddenham

**Solution Architect – IoT Engineering Solutions** at CSL-Group. I architect and build eSIM orchestration systems, specialise in SGP.32, and help shape GSMA standards as a member of the eSIM work group.

---

## What I Do

- **eSIM & eUICC** — SGP.32 architecture, rSIM orchestration, GSMA standards. I also maintain [eUICC.tech](https://euicc.tech), a technical reference covering 12 GSMA eSIM specs.
- **Cellular & Modem** — 2G through 5G, chipset-level integration
- **Embedded Systems** — RTOS firmware, secure boot, hardware-in-the-loop testing
- **Architecture** — system design, CI/CD pipelines, test automation platforms

## Highlights

<div class="highlights-grid">

{% for project in site.portfolio limit:3 %}
  <div class="highlight-card">
    <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
    <p>{{ project.excerpt | strip_html | truncate: 120 }}</p>
    {% if project.tech %}
    <div class="project-tech">
      {% for t in project.tech limit:4 %}<span class="tech-tag">{{ t }}</span>{% endfor %}
    </div>
    {% endif %}
  </div>
{% endfor %}

</div>

[View all projects →](/portfolio/)

---

## Latest Writing

{% for post in site.posts limit:2 %}
- **[{{ post.title }}]({{ post.url | relative_url }})** — {{ post.date | date: "%b %d, %Y" }}
{% endfor %}

[Read the blog →](/posts/)
