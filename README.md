# alexscode.github.io

Personal CV + Portfolio site for Alex Tuddenham. Built with Jekyll, hosted on GitHub Pages.

## Structure

```
├── _config.yml          # Site config, theme, nav, collections
├── _data/               # Structured CV data (YAML)
│   ├── experience.yml   # Work history
│   ├── education.yml    # Education & certifications
│   ├── skills.yml       # Skills by category
│   └── social.yml       # Contact links
├── _layouts/            # Page layouts (default, cv, project, post)
├── _portfolio/          # Project pages (markdown with frontmatter)
├── _posts/              # Blog posts (YYYY-MM-DD-title.md)
├── assets/css/          # Custom styles
├── index.md             # Landing page
├── cv.md                # Auto-generates from _data/
├── about.md             # About me
├── portfolio.md         # Lists all _portfolio/ items
└── posts.md             # Lists all _posts/ items
```

## How to edit

**CV:** Edit `_data/experience.yml`, `_data/skills.yml`, `_data/education.yml`

**Portfolio:** Add `.md` files to `_portfolio/` with frontmatter:
```yaml
---
title: "Project Name"
subtitle: "One-liner"
tech: ["C++", "ESP32"]
links:
  - label: GitHub
    url: https://github.com/...
---
```

**Blog:** Add `.md` files to `_posts/` as `YYYY-MM-DD-slug.md`

**Profile photo:** Add `assets/images/profile.jpg` and set `logo: /assets/images/profile.jpg` in `_config.yml`

## Local development

```bash
bundle install
bundle exec jekyll serve
```

Site auto-builds on push to `main`. Live at [alexscode.github.io](https://alexscode.github.io).
