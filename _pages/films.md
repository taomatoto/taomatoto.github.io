---
layout: films
title: films
permalink: /films/
description: Film stills and visual fragments.
nav: true
nav_order: 2
---

<section class="films-hero" aria-labelledby="films-title">
  <h1 id="films-title">Films.</h1>
</section>

<section class="films-grid" aria-label="Film gallery">
  <article class="film-tile">
    <div class="film-tile__media">
      {% include figure.liquid loading="lazy" path="assets/img/films/R1-05041-0037.JPG" alt="Film still" class="film-tile__image" %}
    </div>
  </article>

  <article class="film-tile">
    <div class="film-tile__media">
      {% include figure.liquid loading="lazy" path="assets/img/films/R1-07211-0019.JPG" alt="Film still" class="film-tile__image" %}
    </div>
  </article>

  <article class="film-tile film-tile--wide">
    <div class="film-tile__media">
      {% include figure.liquid loading="lazy" path="assets/img/films/R1-07211-0029.JPG" alt="Film still" class="film-tile__image" %}
    </div>
  </article>
</section>
