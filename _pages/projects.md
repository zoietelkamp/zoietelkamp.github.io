---
layout: page
title: research
permalink: /projects/
nav: true
nav_order: 3
display_categories:
  - slug: environment
    label: "Core and Environment scale (~10,000 au – 1 pc)"
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
    font-size: clamp(2.5rem, 3.25vw, 2.25rem);
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
    font-size: 1.8rem;
    text-align: left;
  }

  .project-content::after {
    content: "";
    display: table;
    clear: both;
  }

  .project-figure-right {
    float: right;
    max-width: 55%;
    margin: 0.25rem 0 1rem 1.5rem;
  }

  .project-figure-right img {
    max-width: 100%;
    height: auto;
  }

  .project-figure-right .caption {
    margin-top: 0.4rem;
    margin-bottom: 0.5rem;
    font-size: 0.8rem;
    line-height: 1.3;
  }

  .project-figure-center {
    text-align: center;
    margin: 1.5rem 0;
  }

  .project-figure-center img {
    max-width: 100%;
    height: auto;
  }

  .project-figure-center .caption {
    max-width: 850px;
    margin: 0.5rem auto 0;
  }

  .dissertation-intro {
    font-size: 1.05rem;
    line-height: 1.6;
    max-width: 55rem;
    margin: -1.5rem 0 3rem;
  }
</style>

<div class="projects">
  <h1 class="dissertation-title">A multi-scale investigation of star formation across the mass spectrum</h1>

 <p class="dissertation-intro"> 
 Star formation is a complex, multi-scale process traditionally studied in two regimes: low-mass and massive stars, divided at approximately 8 solar masses. Although massive stars only comprise ~1% of the stellar population, their high-energy output and collapse into supernovae have a profound impact on galactic ecosystems. Yet, due to their extreme nature and rarity, a key question remains: do the observed differences between massive and low-mass stars reflect fundamentally distinct formation mechanisms, or is massive star formation simply a scaled-up version of the low-mass star formation process? My research uses data from telescope facilities spanning infrared (IR) to millimeter wavelengths to study star formation across a range of physical scales, working towards a more unified picture of star formation across the mass spectrum.

 </p>

  <!-- <p class="dissertation-intro">The link between the formation mechanisms of low-mass and high-mass stars (with a threshold at 8 M$_\odot$) is still debated. Low-mass stars are much more abundant and can be found in a diverse range of star-forming environments, from isolated dark globules to dense clusters (Beuther et al. 2025). In contrast, high-mass stars only make up about 1% of the stellar population (Rosen et al. 2020) and are typically located in more distant and extreme environments. As a result, high-mass protostars are more difficult to observe, and there is still no consensus on whether they form through similar processes as their low-mass counterparts, or if they require special conditions to form. In order to elucidate the link between low- and high-mass star formation, we need to examine both regimes at a range of scales --- from the inner ~10-100s of au where disks emerge, to the ~1,000-100,000 au where we find the core and clump. Using a range of instruments spanning micron to millimeter wavelengths, we can search for links between properties of disk-protostar systems, the chemistry that develops around them, and the environment in which they form. With this information, we can build a more unified picture of star formation across the mass spectrum.</p> -->

  <!-- <p class="dissertation-intro">Massive stars (which are heavier than eight suns) critically impact galaxy environments and evolution, but the standard framework for star formation breaks down in this mass regime. My dissertation synthesizes observations from major telescope facilities in a multi-scale comparative study of low-mass and massive star formation, working toward a more unified picture across the mass spectrum.</p> -->

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
      {% if project.paper or project.press %}
      <p>
        {% if project.paper %}
        <a href="{{ project.paper }}"><i class="fa-solid fa-file-lines"></i> Published Paper</a>
        {% endif %}
        {% if project.paper and project.press %}
        <span class="mx-2">&middot;</span>
        {% endif %}
        {% if project.press %}
        <a href="{{ project.press }}"><i class="fa-solid fa-newspaper"></i> {{ project.press_label | default: "Press" }}</a>
        {% endif %}
      </p>
      {% endif %}
      <div class="project-content">
        {% if project.summary %}
          {{ project.summary }}
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
