---
layout: films
title: films
permalink: /films/
description: Film stills, sketches, visual notes, and fragments from everyday observation.
nav: true
nav_order: 2
---

<section class="films-hero" aria-labelledby="films-title">
  <div class="films-hero__meta">
    <span>Visual gallery</span>
    <span>Films / sketches / field notes</span>
  </div>
  <div class="films-hero__grid">
    <h1 id="films-title">Films and sketches.</h1>
    <p>
      A visual shelf for moving-image fragments, rough drawings, spatial notes,
      and small observations that sit beside the research work.
    </p>
  </div>
</section>

<section class="films-grid" aria-label="Film and sketch gallery">
  <article class="film-tile film-tile--wide">
    <div class="film-tile__media">
      <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/video/pexels-engin-akyurt-6069112-960x540-30fps.mp4' | relative_url }}" type="video/mp4">
      </video>
    </div>
    <div class="film-tile__body">
      <span>00 / moving note</span>
      <h2>motion study</h2>
      <p>Video placeholder for short film fragments and atmosphere studies.</p>
    </div>
  </article>

  <article class="film-tile">
    <div class="film-tile__media">
      {% include figure.liquid loading="lazy" path="assets/img/8.jpg" alt="Film still placeholder" class="film-tile__image" %}
    </div>
    <div class="film-tile__body">
      <span>01 / still</span>
      <h2>street frame</h2>
      <p>Use this slot for a composed still or location observation.</p>
    </div>
  </article>

  <article class="film-tile">
    <div class="film-tile__media">
      {% include figure.liquid loading="lazy" path="assets/img/10.jpg" alt="Sketch placeholder" class="film-tile__image" %}
    </div>
    <div class="film-tile__body">
      <span>02 / sketch</span>
      <h2>interface sketch</h2>
      <p>Loose drawing, storyboard, prototype note, or visual experiment.</p>
    </div>
  </article>

  <article class="film-tile">
    <div class="film-tile__media">
      {% include figure.liquid loading="lazy" path="assets/img/11.jpg" alt="Visual note placeholder" class="film-tile__image" %}
    </div>
    <div class="film-tile__body">
      <span>03 / note</span>
      <h2>material detail</h2>
      <p>A small visual note from objects, streets, screens, or machines.</p>
    </div>
  </article>

  <article class="film-tile film-tile--tall">
    <div class="film-tile__media">
      {% include figure.liquid loading="lazy" path="assets/img/2.jpg" alt="Vertical frame placeholder" class="film-tile__image" %}
    </div>
    <div class="film-tile__body">
      <span>04 / vertical</span>
      <h2>portrait frame</h2>
      <p>A taller slot for phone footage, vertical sketches, or scanned notes.</p>
    </div>
  </article>

  <article class="film-tile">
    <div class="film-tile__media">
      {% include figure.liquid loading="lazy" path="assets/img/5.jpg" alt="Film frame placeholder" class="film-tile__image" %}
    </div>
    <div class="film-tile__body">
      <span>05 / fragment</span>
      <h2>field fragment</h2>
      <p>Short visual fragments that may become larger project material later.</p>
    </div>
  </article>
</section>
