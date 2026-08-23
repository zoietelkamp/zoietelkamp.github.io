---
layout: page
title: research
permalink: /projects/
nav: true
nav_order: 3
display_categories:
  - slug: environment
    label: "Environment (~10,000 au – 1 pc)"
  - slug: innermost
    label: "Innermost (disk) scale (~10–100 au)"
  - slug: intermediate
    label: "Intermediate (outflow) scale (~1,000 au – 0.1 pc)"
---

<!-- pages/projects.md -->
<style>
  .post-header {
    display: none;
  }

  .dissertation-title {
    font-size: clamp(1.75rem, 4vw, 2.75rem);
    font-weight: 700;
    line-height: 1.3;
    text-align: left;
    color: #281a36;
    margin: 1rem 0 3rem;
  }

  .project-title a {
    color: #281a36;
  }

  .projects h2.category {
    color: #ABABAB;
    font-size: 1.5rem;
    text-align: left;
  }

  .project-content::after {
    content: "";
    display: table;
    clear: both;
  }

  .project-figure-right {
    float: right;
    margin: 0.25rem 0 1rem 1.5rem;
  }
</style>

<div class="projects">
  <h1 class="dissertation-title">A multi-scale investigation of star formation across the mass spectrum...</h1>

  {% for cat in page.display_categories %}
  {% assign sorted_projects = site.projects | where: "category", cat.slug | sort: "importance" %}
  {% if sorted_projects.size > 0 %}
  <section class="project-category mb-5">
    <a id="{{ cat.slug }}" href=".#{{ cat.slug }}">
      <h2 class="category">{{ cat.label }}</h2>
    </a>
    {% for project in sorted_projects %}
    <div class="project-entry mt-3 mb-4 pb-4 border-bottom" id="{{ project.title | slugify }}">
      <h3 class="project-title">
        <a href="#{{ project.title | slugify }}">{{ project.title }}</a>
      </h3>
      {% if project.description %}
      <p class="project-description text-muted">{{ project.description }}</p>
      {% endif %}
      {% if project.github %}
      <p>
        <a href="{{ project.github }}"><i class="fa-brands fa-github"></i> Code Repository</a>
      </p>
      {% endif %}
      {% if project.paper %}
      <p>
        <a href="{{ project.paper }}"><i class="fa-solid fa-file-lines"></i> Published Paper</a>
      </p>
      {% endif %}
      <div class="project-content">
        {% if project.summary %}
          {{ project.summary }}
          <p><a href="{{ project.url | relative_url }}">Full writeup &rarr;</a></p>
        {% else %}
          {{ project.content }}
        {% endif %}
      </div>
    </div>
    {% endfor %}
  </section>
  {% endif %}
  {% endfor %}
</div>
