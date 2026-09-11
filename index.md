---
layout: page
title: "👋"
description: >
  Andrii Novikov — software engineering, AI experiments, teaching, and practical project notes.
---

<p class="eyebrow">Software engineering · AI · teaching</p>
<p class="profile-lead"><strong>Hi, I’m Andrii.</strong> I’m a software engineer and educator based in Goslar, Germany. I like projects where code, product thinking, and clear teaching meet.</p>

<p>This site is a compact record of things I build, teach, and investigate — from software and CRM/project coordination to AI-assisted prototypes and notes on frontier models.</p>

<div class="quick-facts">
  <div class="fact-card"><strong>Software</strong><span>Engineering, maintenance, practical prototypes</span></div>
  <div class="fact-card"><strong>Products</strong><span>Coordination, stakeholders, process design</span></div>
  <div class="fact-card"><strong>Teaching</strong><span>Learning tasks, instruction, mentoring</span></div>
</div>

## Latest posts

<div class="card-grid">
{% for post in site.posts limit: 4 %}
  <article class="post-card">
    <div class="card-meta">{{ post.date | date: "%b %d, %Y" }}</div>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p>{{ post.description }}</p>
  </article>
{% endfor %}
</div>

<a class="section-link" href="{{ '/blog/' | relative_url }}">See all posts →</a>

## Featured projects

{% assign selected_projects = site.projects | sort: 'date' | reverse %}
<div class="card-grid">
{% for project in selected_projects limit: 4 %}
  <article class="portfolio-card">
    <div class="card-meta">{{ project.project_type | default: "Project" }} · {{ project.date | date: "%Y" }}</div>
    <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
    <p>{{ project.description }}</p>
  </article>
{% endfor %}
</div>

<a class="section-link" href="{{ '/projects/' | relative_url }}">View projects →</a>

## Currently

I’m especially interested in how capable AI systems change the way small teams prototype software, document technical work, and move between research, implementation, and teaching. The goal is not to remove engineering judgment — it is to spend more of it on the decisions that matter.
