---
layout: project-custom
title: "Grape Harvest SLF Filtration System"
category: "Mechanical Design"
org: "MAE 2250 — Mechanical Design"
role: "Team: Trees of Doom (5 members)"
date_range: "Spring 2026"
tools:
  - "Fusion 360"
  - "3D Printing"
  - "Lathe & Mill"
tags:
  - "Mechanical Design"
  - "Prototyping"
  - "Fusion 360"
  - "Client Project"
description: >-
  A mechanical density-based filtration device to separate spotted lanternflies from
  harvested grapes — built for Cornell CALS, E&J Gallo Winery, and National Grape.
  Three prototype iterations converging on 64-second water retention and 8kg load capacity.
---

<!-- ── PROBLEM ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">The Problem</p>
  <h2 class="section-heading r">One bug can cost a 22-ton harvest</h2>
  <p class="problem-text r">
    Spotted lanternflies — an invasive pest — get swept up in mechanical grape harvesting along
    with the fruit. Federal regulation rejects entire 22-ton harvest batches if foreign matter
    exceeds <strong>just 0.1%</strong>, meaning as few as one or two insects per batch can trigger
    a full rejection. For New York vineyards already operating on tight margins, that's a significant
    and unpredictable revenue loss with no reliable mechanical solution on the market.
  </p>
  <div class="proj-img-wrap r">
    <img class="proj-img" src="/assets/images/slf-filtration/filtration-sequence.png" alt="Filtration sequence diagram" loading="lazy" />
    <p class="proj-img-caption">Filtration sequence — grapes (blue) sink, SLF (white) float, enabling physical separation</p>
  </div>
</section>

<!-- ── SOLUTION ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">The Solution</p>
  <h2 class="section-heading r">Rotating tri-sector cylinder — density separation, no power required</h2>
  <p class="problem-text r" style="margin-bottom: 1.75rem;">
    The core insight: <strong>grapes sink in water, spotted lanternflies float</strong>. Our device
    exploits this density difference using a rotating cylinder with three distinct base sections —
    solid, fine mesh, and fully open — each serving a different step in the separation sequence.
    A hand crank drives the rotation, keeping the device fully mechanical, food-safe, and buildable
    for roughly $140 in materials.
  </p>

  <div class="features-grid">
    <div class="feature-card r">
      <div class="feature-icon">⬇️</div>
      <p class="feature-name">1 — Pour</p>
      <p class="feature-desc">Harvested grapes enter the cylinder on the <strong>mesh base</strong>. Juice drains through automatically.</p>
    </div>
    <div class="feature-card r">
      <div class="feature-icon">💧</div>
      <p class="feature-name">2 — Float-Separate</p>
      <p class="feature-desc">Crank rotates base to <strong>solid section</strong>. Water floods in — SLF float to the surface, grapes sink.</p>
    </div>
    <div class="feature-card r">
      <div class="feature-icon">🔄</div>
      <p class="feature-name">3 — Drain</p>
      <p class="feature-desc">Rotate to <strong>mesh section</strong> — water drains through, leaving grapes on the base. SLF are skimmed off the surface.</p>
    </div>
    <div class="feature-card r">
      <div class="feature-icon">✅</div>
      <p class="feature-name">4 — Release</p>
      <p class="feature-desc">Rotate to <strong>open section</strong> — clean grapes fall through to collection. Cycle resets.</p>
    </div>
  </div>

  <div class="proj-img-wrap r" style="margin-top: 1.75rem;">
    <img class="proj-img" src="/assets/images/slf-filtration/base-sketch.png" alt="Annotated sketch of the tri-sector base" loading="lazy" />
    <p class="proj-img-caption">Base component — solid (left), mesh (center), open (right) tri-sector layout</p>
  </div>
  <div class="proj-img-wrap r">
    <img class="proj-img" src="/assets/images/slf-filtration/assembly-sketch.png" alt="Annotated sketch of full functional prototype" loading="lazy" />
    <p class="proj-img-caption">Full assembly — handle, shaft, bearing, rotating base, and housing</p>
  </div>
</section>

<!-- ── DESIGN ITERATION ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Design Iteration</p>
  <h2 class="section-heading r">Three prototypes, three problems solved</h2>
  <p class="problem-text r" style="margin-bottom: 2rem;">
    Each version was built to a specific hypothesis, tested against three repeatable
    mechanical tests — rotation smoothness, water retention time, and max supported weight —
    then iterated based on what failed.
  </p>

  <div class="proto-list">

    <div class="proto-card r">
      <div class="proto-header">
        <span class="proto-num">P1</span>
        <div>
          <p class="proto-name">Prototype 1 — Proof of Concept</p>
          <p class="proto-change">Basic tri-base, no sealing</p>
        </div>
      </div>
      <p class="proto-desc">Established that the rotation mechanism worked and the tri-sector concept was physically feasible. The failure was immediate and clear: without any sealing, water drained in seconds.</p>
      <div class="proto-stats">
        <div class="proto-stat">
          <p class="proto-stat-num">~10s</p>
          <p class="proto-stat-label">Water Retention</p>
        </div>
        <div class="proto-stat proto-stat-dim">
          <p class="proto-stat-num">2kg</p>
          <p class="proto-stat-label">Max Load</p>
        </div>
      </div>
    </div>

    <div class="proto-card r">
      <div class="proto-header">
        <span class="proto-num">P2</span>
        <div>
          <p class="proto-name">Prototype 2 — Sealing Added</p>
          <p class="proto-change">O-ring + rubber divider flaps</p>
        </div>
      </div>
      <p class="proto-desc">Added an O-ring around the base perimeter and rubber divider flaps between sectors. Water retention jumped dramatically. The remaining constraint: the base was only press-fit to the shaft, limiting how much weight it could support before deflecting.</p>
      <div class="proto-stats">
        <div class="proto-stat">
          <p class="proto-stat-num">52s</p>
          <p class="proto-stat-label">Water Retention</p>
        </div>
        <div class="proto-stat proto-stat-dim">
          <p class="proto-stat-num">2kg</p>
          <p class="proto-stat-label">Max Load</p>
        </div>
      </div>
      <div class="proj-img-wrap r" style="margin-top: 1rem; margin-bottom: 0;">
        <img class="proj-img" src="/assets/images/slf-filtration/prototype-improvements.png" alt="O-ring, rubber flaps, and base support improvements" loading="lazy" />
        <p class="proj-img-caption">Sealing additions — O-ring groove, rubber divider flaps between sectors</p>
      </div>
    </div>

    <div class="proto-card r">
      <div class="proto-header">
        <span class="proto-num">P3</span>
        <div>
          <p class="proto-name">Final Prototype — Structural Support</p>
          <p class="proto-change">Bearing + shaft collar beneath base</p>
        </div>
      </div>
      <p class="proto-desc">Added a sealed food-safe bearing and shaft collar directly beneath the rotating base. This distributed the load properly and eliminated the deflection issue. Water retention improved further, and max supported weight jumped 4× over earlier versions.</p>
      <div class="proto-stats">
        <div class="proto-stat">
          <p class="proto-stat-num">64s</p>
          <p class="proto-stat-label">Water Retention</p>
        </div>
        <div class="proto-stat">
          <p class="proto-stat-num">8kg</p>
          <p class="proto-stat-label">Max Load</p>
        </div>
      </div>
      <div class="proj-img-wrap r" style="margin-top: 1rem; margin-bottom: 0;">
        <img class="proj-img" src="/assets/images/slf-filtration/final-prototype.png" alt="Final physical prototype" loading="lazy" />
        <p class="proj-img-caption">Final prototype — bearing support, full sealing, functional rotation</p>
      </div>
    </div>

  </div>

  <div class="proj-img-wrap r" style="margin-top: 2rem;">
    <img class="proj-img" src="/assets/images/slf-filtration/cad-assembly.png" alt="Full CAD assembly cross-section" loading="lazy" />
    <p class="proj-img-caption">CAD assembly cross-section — shaft, bearing, hex press-fit, tri-sector base, housing</p>
  </div>
  <div class="proj-img-wrap r">
    <img class="proj-img" src="/assets/images/slf-filtration/water-retention-test.png" alt="Water retention test setup" loading="lazy" />
    <p class="proj-img-caption">Water retention test — timed seal performance across prototype versions</p>
  </div>
</section>

<!-- ── REFLECTION ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Reflection</p>
  <h2 class="section-heading r">What I took away</h2>
  <ul class="reflection-list">
    <li class="r">
      <span class="reflection-bullet"><svg width="10" height="10" viewBox="0 0 10 10" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><polyline points="2 5 4.2 7.2 8 3"/></svg></span>
      <span>The project validated that <strong>density-based separation is a genuinely promising approach</strong> to a real agricultural problem. The physics work — and the iterative prototyping process of identifying a failure mode, designing a fix, and re-testing was exactly how that gets confirmed.</span>
    </li>
    <li class="r">
      <span class="reflection-bullet"><svg width="10" height="10" viewBox="0 0 10 10" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><polyline points="2 5 4.2 7.2 8 3"/></svg></span>
      <span>Working directly with outside clients — Cornell CALS, Gallo, National Grape — meant the constraints were real: <strong>no electrical power, low cost, simple enough to use in the field</strong>. Designing within those boundaries from day one shaped every decision.</span>
    </li>
    <li class="r">
      <span class="reflection-bullet"><svg width="10" height="10" viewBox="0 0 10 10" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><polyline points="2 5 4.2 7.2 8 3"/></svg></span>
      <span>The jump from P2 to P3 — where adding proper bearing support <strong>quadrupled load capacity without touching the sealing system</strong> — was a clean lesson in structural isolation: fixing one subsystem can have outsized effects if you've correctly diagnosed where the constraint actually lives.</span>
    </li>
  </ul>
</section>

<!-- ── BACK BUTTON ──────────────────────────────────── -->
<div class="proj-footer-nav r">
  <a href="/projects/" class="btn btn-ghost">
    <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><polyline points="15 18 9 12 15 6"/></svg>
    Back to Projects
  </a>
</div>
