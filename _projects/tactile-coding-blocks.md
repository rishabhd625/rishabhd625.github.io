---
layout: project-custom
title: "Tactile Coding Blocks"
category: "Assistive Technology"
org: "Cornell Assistive Technologies"
role: "Mechanical Engineering Member"
date_range: "August 2025 – Present"
award: "2nd Place — RESNA 2026 Student Design Challenge"
tools:
  - "Fusion 360"
  - "3D Printing"
  - "AMS Multi-Material"
  - "Braille / CAD"
tags:
  - "Assistive Tech"
  - "3D Printing"
  - "Fusion 360"
  - "Award Winner"
description: >-
  A library of 3D-printed tactile coding blocks with embedded braille, enabling visually
  impaired students to physically build code — at ~$15/block vs. $500+ market alternatives.
  2nd Place at the RESNA 2026 Student Design Challenge.
---

<!-- ── PROBLEM ──────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">The Problem</p>
  <h2 class="section-heading r">CS education has a blind spot</h2>
  <p class="problem-text r">
    Technical literacy is increasingly essential, but the tools for teaching CS to visually
    impaired students are either <strong>prohibitively expensive or simply don't exist</strong>.
    Sighted students get intuitive drag-and-drop environments like Scratch; blind and low-vision
    students have been largely locked out of that learning experience — not because the concepts
    are inaccessible, but because nobody has built the right physical interface for them.
  </p>
</section>

<!-- ── SOLUTION ──────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">The Solution</p>
  <h2 class="section-heading r">Physical blocks that make code tangible</h2>
  <p class="problem-text r">
    A library of <strong>3D-printed snap-together blocks</strong> embedded with Grade 1 Braille
    and contrasting colors, so blind and low-vision students can physically assemble programs
    the same way sighted students drag blocks in Scratch. Each block corresponds to a real
    function, variable, or event in actual block-based coding languages.
  </p>

  <div class="proj-img-wrap r" style="margin-top: 1.5rem;">
    <img class="proj-img" src="/assets/images/tactile-blocks/physical-tactilecodingblocks-kit.png" alt="Full tactile coding blocks kit" loading="lazy" />
    <p class="proj-img-caption">The full block library — 3D-printed, braille-embedded, snap-together coding blocks</p>
  </div>

  <div class="stat-compare r">
    <div>
      <p class="stat-compare-num">~$15</p>
      <p class="stat-compare-label">Our Cost Per Block</p>
      <p class="stat-compare-sub">FDM 3D printed, iteratively refined</p>
    </div>
    <p class="stat-compare-vs">vs.</p>
    <div>
      <p class="stat-compare-num muted">$500+</p>
      <p class="stat-compare-label">Market Alternatives</p>
      <p class="stat-compare-sub">When they exist at all</p>
    </div>
  </div>
</section>

<!-- ── PHASE 1: QUORUM ──────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Technical Progression</p>
  <div class="phase-header r">
    <span class="phase-num">Phase 1</span>
    <span class="phase-name">Quorum</span>
    <span class="phase-platform">— accessibility-focused block language</span>
  </div>
  <ul class="phase-bullets r">
    <li>Designed the <strong>game.game library block</strong>, incorporating Grade 1 Braille and dovetail connector extensions for snap-together modularity</li>
    <li>Iterated the block geometry for a cleaner aesthetic fit and improved the dovetail mechanism for better physical engagement between pieces</li>
    <li>Outlined the full library implementation system, including the <strong>"use Libraries" block</strong> and end cap design to terminate sequences cleanly</li>
    <li>Adapted a "sum" block into an "assignment" block, reworking the geometry to ensure clean fit with adjacent variable blocks</li>
  </ul>

  <div class="proj-img-wrap r">
    <img class="proj-img" src="/assets/images/tactile-blocks/handsketch-libraryassembly.png" alt="Hand sketch of use Libraries and game.game block concept" loading="lazy" />
    <p class="proj-img-caption">Early concept sketch — use Libraries / game.game block layout and connector system</p>
  </div>

  <div class="img-gallery r">
    <div class="img-slot has-img">
      <img src="/assets/images/tactile-blocks/game.game-block.png" alt="game.game library block" loading="lazy" />
      <p class="img-caption">game.game library block — braille + dovetail connectors</p>
    </div>
    <div class="img-slot has-img">
      <img src="/assets/images/tactile-blocks/sum-assignment-block.png" alt="sum to assignment block adaptation" loading="lazy" />
      <p class="img-caption">sum → assignment block — geometry rework for variable block fit</p>
    </div>
  </div>

  <div class="proj-img-wrap r" style="margin-top: 1rem;">
    <img class="proj-img" src="/assets/images/tactile-blocks/useLibraries-game.game-fullassembly.png" alt="use Libraries and game.game full assembly" loading="lazy" />
    <p class="proj-img-caption">use Libraries + game.game full assembly — complete sequence with end cap</p>
  </div>
</section>

<!-- ── PHASE 2: MICRO:BIT ──────────────────────────────── -->
<section class="proj-section">
  <div class="phase-header r">
    <span class="phase-num">Phase 2</span>
    <span class="phase-name">Micro:bit / MakeCode</span>
    <span class="phase-platform">— after presenting Quorum work at competition</span>
  </div>
  <ul class="phase-bullets r" style="margin-bottom: 1.25rem;">
    <li>Recognized inconsistent tolerances across the team's growing block library — created a <strong>fully constrained parametric base sketch</strong> in Fusion 360 that became the standardized template for all future blocks</li>
  </ul>

  <div class="proj-img-wrap r">
    <img class="proj-img" src="/assets/images/tactile-blocks/constrainedsketch.png" alt="Fully constrained parametric base sketch" loading="lazy" />
    <p class="proj-img-caption">Constrained base sketch — parametric template that standardized tolerances across the entire library</p>
  </div>

  <ul class="phase-bullets r">
    <li>Designed the <strong>"play" block</strong> in both braille and non-braille versions based on direct feedback from the Micro:bit team and end users</li>
    <li>After user testing, reworked "play" into a <strong>"play tone" block</strong> — extending it to accept additional variables for note and beat</li>
    <li>Designed a set of modular <strong>Note Blocks</strong> (High C, Middle C, Middle D#, High E) that snap into the play tone block as interchangeable inputs</li>
  </ul>

  <div class="img-gallery r">
    <div class="img-slot has-img">
      <img src="/assets/images/tactile-blocks/playblock-braille.png" alt="play block with braille" loading="lazy" />
      <p class="img-caption">play block — braille version</p>
    </div>
    <div class="img-slot has-img">
      <img src="/assets/images/tactile-blocks/playblock-nobraille.png" alt="play block without braille" loading="lazy" />
      <p class="img-caption">play block — non-braille version</p>
    </div>
  </div>

  <div class="callout-box r">
    <p class="callout-eyebrow">Engineering Problem</p>
    <p class="callout-title">Print bed constraint → dovetail split-and-rejoin solution</p>
    <p class="callout-text">
      Extending the "play" block with additional variable slots pushed the part beyond the printer's build volume.
      Rather than simplify the design, I engineered a <strong>dovetail split joint</strong> that divides the block
      into two printable halves with carefully tuned tolerances — tight enough for a solid, seamless connection,
      loose enough for repeatable assembly without tools. The two halves rejoin with the same dovetail geometry
      used throughout the library, keeping the interface consistent for users.
    </p>
  </div>

  <div class="proj-img-wrap r">
    <img class="proj-img" src="/assets/images/tactile-blocks/playtoneblock-dovetailsplit.png" alt="play tone block with dovetail split joint" loading="lazy" />
    <p class="proj-img-caption">play tone block — dovetail split into two printable halves, with "for" and "beat" extension blocks</p>
  </div>

  <div class="proj-img-wrap r">
    <img class="proj-img" src="/assets/images/tactile-blocks/noteblocks.png" alt="Note blocks set" loading="lazy" />
    <p class="proj-img-caption">Note Blocks — High C, Middle C, Middle D#, High E; snap into play tone block as interchangeable inputs</p>
  </div>
</section>

<!-- ── PHASE 3: OCTOSTUDIO ──────────────────────────────── -->
<section class="proj-section">
  <div class="phase-header r">
    <span class="phase-num">Phase 3</span>
    <span class="phase-name">OctoStudio</span>
    <span class="phase-platform">— first production-finish prints</span>
  </div>
  <ul class="phase-bullets r">
    <li>Designed compact event-trigger blocks — <strong>"when"</strong> and <strong>"when I shake"</strong> — with embedded Braille and tactile icon cutouts (play button, shake icon, phone icon) for an additional block-coding platform</li>
    <li>These were produced in <strong>dual-color AMS filament</strong> (black/white) — the first blocks in the project to move from prototype gray to a production-style finish with visual contrast for low-vision users</li>
  </ul>

  <div class="img-gallery r">
    <div class="img-slot has-img">
      <img src="/assets/images/tactile-blocks/octostudios-playwhen-cad.png" alt="when block CAD render" loading="lazy" />
      <p class="img-caption">"when" block — CAD</p>
    </div>
    <div class="img-slot has-img">
      <img src="/assets/images/tactile-blocks/octostudios-playwhen-physical.png" alt="when block final print" loading="lazy" />
      <p class="img-caption">"when" block — final black/white print</p>
    </div>
    <div class="img-slot has-img">
      <img src="/assets/images/tactile-blocks/octostudios-whenIshake-cad.png" alt="when I shake block CAD render" loading="lazy" />
      <p class="img-caption">"when I shake" block — CAD</p>
    </div>
    <div class="img-slot has-img">
      <img src="/assets/images/tactile-blocks/octostudios-whenIshake-physical.png" alt="when I shake block final print" loading="lazy" />
      <p class="img-caption">"when I shake" block — final print</p>
    </div>
  </div>
</section>

<!-- ── AWARD ──────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Recognition</p>
  <h2 class="section-heading r">2nd Place — RESNA 2026 Student Design Challenge</h2>
  <p class="problem-text r">
    The team presented Tactile Coding Blocks at the <strong>RESNA 2026 Annual Conference</strong>
    in the Student Design Challenge — a national competition for student-built assistive technology.
    Out of teams from universities across the country, we placed <strong>2nd overall</strong>.
    The judges highlighted the project's low cost, real-world testability, and the directness
    of the solution to a gap in accessible CS education.
  </p>
  <div class="proj-img-wrap r" style="margin-top: 1.5rem; margin-bottom: 0;">
    <img class="proj-img" src="/assets/images/tactile-blocks/RESNA2026TeamPhoto.png" alt="RESNA 2026 team photo" loading="lazy" />
    <p class="proj-img-caption">RESNA 2026 Student Design Challenge — 2nd place, New York Metro</p>
  </div>
</section>

<!-- ── REFLECTION ──────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Reflection</p>
  <h2 class="section-heading r">What I took away</h2>
  <ul class="reflection-list">
    <li class="r">
      <span class="reflection-bullet"><svg width="10" height="10" viewBox="0 0 10 10" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><polyline points="2 5 4.2 7.2 8 3"/></svg></span>
      <span><strong>Standardization upfront saves enormous time downstream.</strong> Once the team locked in consistent tolerances and a shared base sketch, every block that followed got faster to design. The parametric template was the single highest-leverage thing I contributed.</span>
    </li>
    <li class="r">
      <span class="reflection-bullet"><svg width="10" height="10" viewBox="0 0 10 10" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><polyline points="2 5 4.2 7.2 8 3"/></svg></span>
      <span><strong>Team organization is a force multiplier.</strong> Centralizing CAD files and documenting dimension standards made it possible to hand off work cleanly — without it, each new block would have required rediscovering decisions already made.</span>
    </li>
    <li class="r">
      <span class="reflection-bullet"><svg width="10" height="10" viewBox="0 0 10 10" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><polyline points="2 5 4.2 7.2 8 3"/></svg></span>
      <span><strong>Front-load the fuzzy work.</strong> The projects that went smoothest were the ones where we did brainstorming and early prototyping before we thought we needed to. Constraints get clearer once you have something physical in your hands.</span>
    </li>
  </ul>
</section>

<!-- ── LINKS ──────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Links</p>
  <h2 class="section-heading r">Learn more</h2>
  <div class="proj-ext-links r">
    <a href="https://tactilecodingblocks.com/" target="_blank" rel="noopener" class="btn btn-accent">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
      Project Website
    </a>
    <a href="https://www.resna.org/Events/RESNA-2026-Conference-Information/New-York-Metro/2026-RESNA-Student-Design-Challenge-Winners-Finalists" target="_blank" rel="noopener" class="btn btn-ghost">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
      RESNA 2026 Winners
    </a>
  </div>
</section>

<!-- ── BACK BUTTON ──────────────────────────────── -->
<div class="proj-footer-nav r">
  <a href="/projects/" class="btn btn-ghost">
    <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><polyline points="15 18 9 12 15 6"/></svg>
    Back to Projects
  </a>
</div>
