---
layout: layouts/base.njk
title: CRMEF
---

<section class="section">
  <h2>Vue d’ensemble</h2>
  <div class="card">
    <p class="muted">
      Ici, je regroupe les modules suivis, productions, et traces d’apprentissage,
      organisés par semestre, puis par module.
    </p>
  </div>
</section>

<section class="section">
  <h2>Semestres</h2>
  <div class="grid grid-3">
    <a class="card" href="/semesters/semestre-1/">
      <div class="kicker">Semestre 1</div>
      <h3>Fondations</h3>
      <p class="muted">Planification, gestion, TICE, didactique…</p>
    </a>
    <a class="card" href="/semesters/semestre-2/">
      <div class="kicker">Semestre 2</div>
      <h3>Approfondissement</h3>
      <p class="muted">Consolidation, projets, évaluation avancée…</p>
    </a>
    <a class="card" href="/ressources/">
      <div class="kicker">Ressources</div>
      <h3>Supports & outils</h3>
      <p class="muted">PDF, modèles, grilles, diapos, liens.</p>
    </a>
  </div>
</section>

<section class="section">
  <h2>Modules (liste)</h2>
  <div class="grid">
    {% for m in collections.modules %}
      <a class="card" href="{{ m.url }}">
        <h3>{{ m.data.title }}</h3>
        <p class="muted">{{ m.data.excerpt }}</p>
      </a>
    {% endfor %}
  </div>
</section>
