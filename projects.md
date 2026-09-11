---
layout: page
title: Projects
description: >
  Selected software, teaching, coordination, and AI-assisted prototype work.
---

<p class="profile-lead">A mix of software, product/process work, and teaching projects. I keep the descriptions deliberately concrete: what the work involved, what was delivered, and what I learned from it.</p>

{% assign projects = site.projects | sort: 'date' | reverse %}
<div class="card-grid">
{% for project in projects %}
  <article class="portfolio-card">
    <div class="card-meta">{{ project.project_type | default: "Project" }} · {{ project.date | date: "%Y" }}</div>
    <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
    <p>{{ project.description }}</p>
  </article>
{% endfor %}
</div>
