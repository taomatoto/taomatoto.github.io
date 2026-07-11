---
layout: works
title: works
permalink: /works/
description: Visual index of selected design engineering projects.
nav: true
nav_order: 1
---

{% assign works = site.projects | sort: "importance" %}

<section class="works-hero" aria-labelledby="works-title">
  <div class="works-hero__meta">
    <span>Selected works</span>
    <span>Design engineering / research systems</span>
  </div>
  <div class="works-hero__grid">
    <h1 id="works-title">Selected works.</h1>
    <p>
      A visual catalogue of prototypes, tools, and experiments across mobility,
      AI-assisted workflows, and human-machine interaction.
    </p>
  </div>
</section>

<section class="works-index" aria-label="Project index">
  {% for project in works %}
    {% include work-card.liquid project=project index=forloop.index %}
  {% endfor %}
</section>
