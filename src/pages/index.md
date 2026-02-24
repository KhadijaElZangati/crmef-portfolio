---
layout: layouts/base.njk
title: Accueil
---

<section class="hero">
  <div class="kicker">Portfolio CRMEF</div>
  <h1>{{ site.tagline }}</h1>
  <p>
    Une vitrine claire et professionnelle de mon parcours : modules, productions,
    stages (MSP), ressources, articles et réflexions pédagogiques.
  </p>
  <div class="btns">
    <a class="btn btn--primary" href="{{ site.cta.primaryUrl }}">{{ site.cta.primaryLabel }}</a>
    <a class="btn" href="{{ site.cta.secondaryUrl }}">{{ site.cta.secondaryLabel }}</a>
  </div>
</section>

<section class="section">
  <h2>Navigation rapide</h2>
  <div class="grid grid-3">
    <a class="card" href="/profil/">
      <div class="kicker">Profil</div>
      <h3>Identité professionnelle</h3>
      <p class="muted">Compétences, CV, certifications, objectifs.</p>
    </a>
    <a class="card" href="/crmef/">
      <div class="kicker">CRMEF</div>
      <h3>Modules & productions</h3>
      <p class="muted">Semestres, modules, travaux et traces.</p>
    </a>
    <a class="card" href="/msp/">
      <div class="kicker">MSP</div>
      <h3>Pratique sur le terrain</h3>
      <p class="muted">Séances, fiches, observations, retours.</p>
    </a>
  </div>
</section>

<section class="section">
  <h2>Derniers articles</h2>
  <div class="grid">
    {% for post in collections.posts | slice(0,3) %}
  <a class="card" href="{{ post.url }}">
    {% if post.date %}
      <div class="kicker">{{ post.date }}</div>
    {% endif %}
    <h3>{{ post.data.title }}</h3>
    <p class="muted">{{ post.data.excerpt }}</p>
  </a>
{% endfor %}
  </div>
</section>
