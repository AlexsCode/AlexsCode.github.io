---
layout: default
title: Blog
permalink: /posts/
---

# Blog

{% for post in site.posts %}
<div class="portfolio-entry">
  <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
  <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
  <p>{{ post.excerpt | strip_html | truncate: 200 }}</p>
</div>
<hr>
{% endfor %}

{% if site.posts.size == 0 %}
<p class="placeholder">
  No posts yet. Create markdown files in <code>_posts/</code> with dates and frontmatter.
</p>
{% endif %}
