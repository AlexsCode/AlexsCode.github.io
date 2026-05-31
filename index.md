---
layout: default
title: Home
---

# Hi, I'm Alex Tuddenham

**Embedded Systems Engineer** — I build firmware for microcontrollers, design IoT hardware, and write the low-level code that makes devices tick.

{% comment %}
  Uncomment and add a photo:
  Add your photo as assets/images/profile.jpg
  Then set logo: /assets/images/profile.jpg in _config.yml
{% endcomment %}

---

## What I Do

- **Embedded C/C++** — ESP32, ARM Cortex-M, bare-metal and RTOS
- **IoT Systems** — sensor networks, BLE, MQTT, LoRaWAN, edge computing
- **PCB & Hardware Design** — schematic capture, layout, prototyping
- **Test-Driven Development** for embedded — because bugs in firmware hurt more

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
