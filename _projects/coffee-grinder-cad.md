---
layout: project-custom
title: "Vintage Coffee Grinder Redesign"
category: "CAD & Mechanical Design"
org: "MAE 2250 — Introduction to Mechanical Design"
role: "Individual"
date_range: "Spring 2026"
tools:
  - "Fusion 360"
  - "McMaster-Carr"
tags:
  - "CAD"
  - "Component Selection"
  - "Fusion 360"
  - "3D Printing"
description: >-
  A fully constrained Fusion 360 assembly redesigning a 1930s Peugeot hand-crank
  coffee grinder using modern McMaster-Carr components — the assignment was about
  making sourcing and machining decisions that could actually be built.
---

<!-- ── THE ASSIGNMENT ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">The Assignment</p>
  <h2 class="section-heading r">A CAD and component-selection exercise — not a design showcase</h2>
  <p class="problem-text r">
    The goal was to redesign a 1930s Peugeot hand-crank coffee grinder using modern
    off-the-shelf components, verify the design with a fully constrained CAD assembly,
    and document every component with sourcing and machining requirements — the standard
    being a design that could actually be built. The interesting part wasn't modeling
    shapes. It was making every component decision work together under real fabrication
    and sourcing constraints.
  </p>

  <div class="proj-img-wrap r" style="margin-top: 1.75rem;">
    <img class="proj-img" src="/assets/images/coffee-grinder/sketch.png" alt="Annotated engineering sketch — body view and cross-section showing zone labels, shaft sizing logic, bearing positions, and dimension callouts" loading="lazy" />
    <p class="proj-img-caption">Engineering sketch developed before any CAD — body view (top) with labeled zones (miter gear area / burr area / collection area) and cross-section (bottom) showing shaft sizing logic, bearing placement, and dimension callouts for collection cup clearance</p>
  </div>
</section>

<!-- ── THE ENGINEERING CHALLENGE ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">The Engineering Challenge</p>
  <h2 class="section-heading r">Making every component decision work together</h2>
  <p class="problem-text r" style="margin-bottom: 1.75rem;">
    Three constraints shaped every decision in the project — and each one ruled out
    the easy path.
  </p>

  <div class="constraints-grid r">
    <div class="constraint-card">
      <div class="constraint-icon">🔩</div>
      <div>
        <p class="constraint-name">Mechanical fastening only</p>
        <p class="constraint-desc">No welding, gluing, or taping — every joint had to be threaded, bored, press-fit, or otherwise mechanically locked. Every connection required a deliberate fastening decision.</p>
      </div>
    </div>
    <div class="constraint-card">
      <div class="constraint-icon">📦</div>
      <div>
        <p class="constraint-name">At most 3 self-fabricated parts</p>
        <p class="constraint-desc">Everything else had to come from McMaster-Carr with a downloadable CAD file. The constraint forced sourcing decisions first, then design around what's available — not the other way around.</p>
      </div>
    </div>
    <div class="constraint-card">
      <div class="constraint-icon">⚙️</div>
      <div>
        <p class="constraint-name">Fully constrained assembly</p>
        <p class="constraint-desc">No part penetrations, nothing falling under gravity, and motion-linked: rotating the crank handle had to actually drive the burrs through the miter gears in the Fusion 360 assembly.</p>
      </div>
    </div>
  </div>
</section>

<!-- ── COMPONENT DECISIONS ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Component Decisions</p>
  <h2 class="section-heading r">Five decisions worth explaining</h2>
  <p class="problem-text r" style="margin-bottom: 1.75rem;">
    The BOM has eleven component types. Most are straightforward sourcing calls.
    These five each required an engineering decision beyond just picking a part.
  </p>

  <div class="callout-box r">
    <p class="callout-eyebrow">Main Shaft — McMaster 1265K71</p>
    <p class="callout-title">Three machining operations on one off-the-shelf rod</p>
    <p class="callout-text">
      A standard steel shaft, cut to length — but both ends had to do different jobs.
      One end was <strong>milled to a hex profile</strong> to mate with the miter gear
      without slipping under torque. The other was <strong>threaded</strong> to accept
      a hex nut that holds the vertical shaft in place axially. That's three operations
      (cut, mill, thread) on a single McMaster rod — exactly the kind of decision the
      assignment was designed to surface.
    </p>
  </div>

  <div class="callout-box r">
    <p class="callout-eyebrow">Miter Gears — McMaster 2600N1</p>
    <p class="callout-title">The axis change — and a bore that needed adjusting</p>
    <p class="callout-text">
      The miter gears do the core mechanical work: converting <strong>horizontal crank
      rotation to vertical burr drive</strong> through a 90° axis change. The constraint
      was fit — the bores as-purchased were slightly too small for the shaft diameter.
      Rather than sourcing a custom gear, the fix was <strong>boring them out</strong> to
      the needed clearance, keeping everything within McMaster stock while solving the
      interference.
    </p>
  </div>

  <div class="callout-box r">
    <p class="callout-eyebrow">Crank Handle — McMaster 6547N15</p>
    <p class="callout-title">One M2 set screw turns a free-spinning handle into a locked drive input</p>
    <p class="callout-text">
      Without a positive mechanical stop, the handle would spin freely on the shaft
      under any load. The solution: <strong>bore the handle for shaft fit</strong>, then
      drill and tap a radial hole for an M2 set screw. One small threaded fastener
      locks rotation without modifying shaft geometry or adding external hardware —
      the simplest mechanically-sound fix available within the sourcing constraint.
    </p>
  </div>

  <div class="callout-box r">
    <p class="callout-eyebrow">Ball Bearings — McMaster 5972K93 (×3)</p>
    <p class="callout-title">Standard bearings, 3D-printed housing — tolerance is the design problem</p>
    <p class="callout-text">
      Three bearings support the two shafts, allowing free rotation while holding
      position. The constraint: the housing they seat in is <strong>3D printed</strong>,
      one of the three allowed self-fabricated parts. That meant designing the housing
      geometry in Fusion to accept the standard bearing ODs precisely, and
      <strong>tapping the housing directly</strong> for all threaded connections rather
      than using inserts. The CAD had to get the bore diameters right for the bearings
      to seat without play.
    </p>
  </div>

  <div class="callout-box r">
    <p class="callout-eyebrow">Conical Burrs — GrabCAD (reverse-engineered)</p>
    <p class="callout-title">The one allowed exception — and why it was justified</p>
    <p class="callout-text">
      Every other component came from McMaster. The burrs were the single exception:
      their conical grinding geometry isn't machinable with class shop resources, and
      no suitable off-the-shelf part exists on McMaster-Carr. The solution was a
      <strong>reverse-engineered CAD model from GrabCAD</strong> — acceptable per the
      assignment rules as the one permitted departure from the sourcing constraint.
      Using it required explicit justification in the documentation, not just plugging
      in a convenient model.
    </p>
  </div>

  <div class="proj-img-wrap r" style="margin-top: 2rem;">
    <img class="proj-img" src="/assets/images/coffee-grinder/cad-render.png" alt="Isometric CAD render of full assembled grinder — dark material on grid background, showing external housing with cutaway windows, crank handle on right, hex nut on top, miter gears and burrs visible through openings" loading="lazy" />
    <p class="proj-img-caption">Final CAD assembly — cutaway housing exposes the miter gear area, burr zone, and collection area. Hex nut on top shaft and crank handle on right.</p>
  </div>

  <div class="proj-img-wrap r" style="margin-top: 1.5rem;">
    <img class="proj-img" src="/assets/images/coffee-grinder/exploded-view.png" alt="Exploded view of all major components — hex nut and main shaft pulling up from housing, crank assembly pulling right, miter gears and conical burrs separated, mounting screws dropped below" loading="lazy" />
    <p class="proj-img-caption">Exploded view showing all 11 component types, sourced from McMaster-Carr and 3D printed, with machining operations including shaft shortening, hex milling, boring, and threading</p>
  </div>
</section>

<!-- ── FULLY CONSTRAINED ASSEMBLY ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Assembly</p>
  <h2 class="section-heading r">Fully constrained — and motion-linked</h2>
  <p class="problem-text r" style="margin-bottom: 1.75rem;">
    The final Fusion 360 assembly is fully constrained: no part penetrations, no
    components that fall under gravity without a mate, and the motion is live —
    rotating the crank handle drives the miter gears, which drive the burrs through
    the vertical shaft. The section view below shows the internal geometry that makes
    it work: shaft stack, miter gear mesh, bearing seats, and burr alignment, all
    verified in the assembly before any fabrication would begin.
  </p>

  <div class="proj-img-wrap r">
    <img class="proj-img" src="/assets/images/coffee-grinder/section-view.png" alt="Section view of CAD assembly showing internal shaft stack, miter gear mesh, bearing seats, and burr alignment" loading="lazy" />
    <p class="proj-img-caption">Fully constrained assembly — rotating the crank drives the miter gears, which drive the burrs through the vertical shaft.</p>
  </div>
</section>

<!-- ── BACK BUTTON ──────────────────────────────────── -->
<div class="proj-footer-nav r">
  <a href="/projects/" class="btn btn-ghost">
    <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><polyline points="15 18 9 12 15 6"/></svg>
    Back to Projects
  </a>
</div>
