---
layout: works
title: works
permalink: /works/
description: Visual index of selected design engineering projects.
nav: true
nav_order: 1
---

{% assign works = site.projects | where: "featured", true | sort: "importance" %}

<section class="works-hero" aria-labelledby="works-title">
  <div class="works-hero__meta">
    <span>Selected works</span>
    <span>Design engineering</span>
  </div>
  <h1 id="works-title">Projects</h1>
</section>

<section class="works-index" aria-label="Project index">
  {% for project in works %}
    {% include work-card.liquid project=project index=forloop.index %}
  {% endfor %}
</section>
