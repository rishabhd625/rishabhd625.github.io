---
layout: project-custom
title: "Bike Frame FEA Analysis & Optimization"
category: "Structural Analysis"
org: "MAE 3150 — Engineering Simulations & Design"
role: "Individual Project"
date_range: "April – May 2026"
tools:
  - "Fusion 360"
  - "Ansys Mechanical 2025 R2"
  - "MOGA Optimization"
tags:
  - "FEA"
  - "Ansys"
  - "Fusion 360"
  - "Optimization"
description: >-
  Shell-theory FEA and MOGA-driven optimization of an aluminum bike-share frame.
  Achieved 42% material reduction while maintaining a factor of safety of 3.5.
---

<!-- ── PROBLEM ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Problem Statement</p>
  <h2 class="section-heading r">Over-engineered by default, optimized by analysis</h2>
  <p class="problem-text r">
    Bike-share programs must balance two competing demands: rider safety and operational cost.
    A frame that is over-engineered wastes material and raises the cost per unit; one that is
    under-designed risks failure under the highly variable loads of a shared-use environment.
    This project used finite element analysis to characterize the structural behavior of an
    aluminum alloy frame, then applied automated multi-objective optimization to find the
    <strong>minimum tube thickness that keeps the factor of safety comfortably above the target
    threshold</strong> — reducing material cost without compromising structural integrity.
  </p>
</section>

<!-- ── STEP 01 ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Process</p>
  <div class="phase-header r">
    <span class="phase-num">01</span>
    <span class="phase-name">Initial Analysis</span>
  </div>
  <p class="problem-text r" style="margin-bottom: 1.5rem;">
    Constructed 2D frame geometry in Fusion 360 using surface tools, then imported into
    Ansys Mechanical 2025 R2. Meshed at a <strong>4mm element size</strong> with a shell-theory
    model (6 degrees of freedom per node). Boundary conditions: zero displacement at the
    handlebars and rear wheel contact point; 700N downward seat load and 150N pedal load.
    Material set to aluminum alloy at 2mm uniform thickness.
  </p>

  <div class="proj-img-wrap r">
    <img class="proj-img" src="/assets/images/bike-frame/mesh.png" alt="Initial mesh at 4mm elements" loading="lazy" />
    <p class="proj-img-caption">Initial mesh — 4mm shell elements, 6 DOF per node</p>
  </div>

  <p class="problem-text r" style="margin-top: 1.25rem;">
    Results showed maximum deformation of <strong>~0.1mm near the seat</strong> and a factor of
    safety of 15 across most of the frame — confirming the baseline design is structurally
    over-engineered and a strong candidate for material reduction.
  </p>

  <div class="proj-img-wrap r" style="margin-top: 1.25rem;">
    <img class="proj-img" src="/assets/images/bike-frame/deformation.png" alt="Deformation contour" loading="lazy" />
    <p class="proj-img-caption">Deformation contour — peak ~0.1mm at seat, confirming baseline over-stiffness</p>
  </div>
</section>

<!-- ── STEP 02 ──────────────────────────────────── -->
<section class="proj-section">
  <div class="phase-header r">
    <span class="phase-num">02</span>
    <span class="phase-name">Design Modifications</span>
  </div>
  <p class="problem-text r" style="margin-bottom: 1.5rem;">
    Removed the top tube to cut material, added a battery weight load on the bottom tube to
    represent realistic e-bike loading conditions, and introduced a hole in the low-stress
    upper region of the bottom tube. Stress concentration increased slightly around the cutout
    but remained well within safe limits — demonstrating that <strong>stress-map-guided geometry
    decisions can meaningfully reduce mass</strong> without introducing structural risk.
  </p>

  <div class="proj-img-wrap r">
    <img class="proj-img" src="/assets/images/bike-frame/vonmises.png" alt="Von-Mises stress distribution" loading="lazy" />
    <p class="proj-img-caption">Von-Mises stress distribution — modified design with top tube removed and bottom tube cutout</p>
  </div>
</section>

<!-- ── STEP 03 ──────────────────────────────────── -->
<section class="proj-section">
  <div class="phase-header r">
    <span class="phase-num">03</span>
    <span class="phase-name">Response Surface Optimization</span>
  </div>
  <p class="problem-text r" style="margin-bottom: 1.5rem;">
    Configured a parametric sweep of seat tube thickness from 1–2mm, then launched a
    Response Surface Optimization using the <strong>MOGA (Multi-Objective Genetic Algorithm)</strong>
    in Ansys Mechanical. Objective: minimize frame mass while maintaining FOS ≥ 3.5. After
    1,511 evaluations the algorithm converged on an optimal thickness of <strong>~1.16mm</strong>.
    Maximum Von-Mises stress at the optimized geometry was ~64 MPa — well below aluminum's yield
    strength — confirming the result is both safe and material-efficient.
  </p>

  <div class="img-gallery r">
    <div class="img-slot has-img">
      <img src="/assets/images/bike-frame/moga.png" alt="MOGA results table" loading="lazy" />
      <p class="img-caption">MOGA results — 1,511 evaluations converging on 1.16mm optimal thickness</p>
    </div>
    <div class="img-slot has-img">
      <img src="/assets/images/bike-frame/optimized.png" alt="Optimized frame design" loading="lazy" />
      <p class="img-caption">Optimized design — 42% material reduction, FOS maintained at 3.5×</p>
    </div>
  </div>
</section>

<!-- ── RESULTS ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Outcomes</p>
  <h2 class="section-heading r">Key Results</h2>
  <div class="results-grid">
    <div class="result-card r">
      <p class="result-stat">42%</p>
      <p class="result-label">Material Reduction</p>
      <p class="result-detail">Lower tube material saved versus the original 2mm baseline design</p>
    </div>
    <div class="result-card r">
      <p class="result-stat">3.5×</p>
      <p class="result-label">Factor of Safety</p>
      <p class="result-detail">Maintained at or above the safety threshold after full optimization</p>
    </div>
    <div class="result-card r">
      <p class="result-stat">1,511</p>
      <p class="result-label">MOGA Evaluations</p>
      <p class="result-detail">Algorithm evaluations to converge on 1.16mm optimal seat tube thickness</p>
    </div>
  </div>
</section>

<!-- ── LEARNINGS ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Takeaways</p>
  <h2 class="section-heading r">What I learned</h2>
  <ul class="reflection-list">
    <li class="r">
      <span class="reflection-bullet"><svg width="10" height="10" viewBox="0 0 10 10" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><polyline points="2 5 4.2 7.2 8 3"/></svg></span>
      <span><strong>Shell-theory FEA fundamentals</strong> — what 6-DOF node modeling means for thin-walled structures, and where it's appropriate versus solid elements</span>
    </li>
    <li class="r">
      <span class="reflection-bullet"><svg width="10" height="10" viewBox="0 0 10 10" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><polyline points="2 5 4.2 7.2 8 3"/></svg></span>
      <span><strong>Surface modeling in Fusion 360</strong> — previously only worked with solid bodies; surface tools are essential for shell FEA geometry prep</span>
    </li>
    <li class="r">
      <span class="reflection-bullet"><svg width="10" height="10" viewBox="0 0 10 10" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><polyline points="2 5 4.2 7.2 8 3"/></svg></span>
      <span><strong>Parametric response surface optimization</strong> — the full MOGA workflow end-to-end in Ansys Mechanical, from parameter bounds to candidate selection</span>
    </li>
    <li class="r">
      <span class="reflection-bullet"><svg width="10" height="10" viewBox="0 0 10 10" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><polyline points="2 5 4.2 7.2 8 3"/></svg></span>
      <span><strong>Projecting sketches onto curved surfaces</strong> to create geometry cutouts in Fusion 360 — a workflow I'll use regularly for complex part features</span>
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
