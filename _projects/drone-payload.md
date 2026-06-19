---
layout: project-custom
title: "3D Printed Payload Drone"
category: "Aerial Robotics"
org: "Personal Project"
role: "Co-developer"
date_range: "May – August 2025"
tools:
  - "Mechanical"
  - "Electrical"
  - "Software"
tags:
  - "Drones"
  - "Embedded Systems"
  - "3D Printing"
  - "FEA"
description: >-
  A fully 3D-printed quadcopter designed and built from scratch to carry up to 1lb of payload.
  Custom airframe, hand-soldered electronics, and BetaFlight configuration — flight achieved.
---

<!-- ── OVERVIEW ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">The Project</p>
  <h2 class="section-heading r">Designed to carry — built from scratch</h2>
  <p class="problem-text r">
    Most consumer drones aren't designed with payload delivery in mind — their frames are
    optimized for low weight at the cost of structural margin, and swapping in a payload
    bay isn't straightforward. This project started from a blank CAD canvas: design and
    build a fully 3D-printed quadcopter, from airframe geometry to flight controller
    configuration, capable of carrying up to <strong>1lb of payload</strong>. Every component
    was either designed, sourced, assembled, or soldered by hand.
  </p>

  <div class="proj-img-wrap r" style="margin-top: 1.75rem;">
    <img class="proj-img" src="/assets/images/drone/DroneAssembled.jpg" alt="Fully assembled 3D printed quadcopter in grass" loading="lazy" />
    <p class="proj-img-caption">Finished quadcopter — fully 3D-printed frame, arms, cover, and payload bay</p>
  </div>
</section>

<!-- ── TOOLS BREAKDOWN ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Tools & Skills</p>
  <div class="role-grid">
    <div class="role-card r">
      <p class="role-name">Mechanical</p>
      <ul class="role-bullets">
        <li>Custom 3D-printed frame, arms, cover, payload bay</li>
        <li>DFM / DFA design principles</li>
        <li>Static FEA (arm + frame validation)</li>
        <li>Hand drill, screws, airframe assembly</li>
        <li>Propeller selection and fit</li>
      </ul>
    </div>
    <div class="role-card r">
      <p class="role-name">Electrical</p>
      <ul class="role-bullets">
        <li>TAKER G4 AIO flight controller</li>
        <li>SunnySky brushless DC motors</li>
        <li>ExpressLRS EP1 receiver + RC transmitter</li>
        <li>LiPo battery</li>
        <li>Hand PCB soldering</li>
        <li>Continuity & isolation testing</li>
      </ul>
    </div>
    <div class="role-card r">
      <p class="role-name">Software</p>
      <ul class="role-bullets">
        <li>BetaFlight Configurator</li>
        <li>Flight controller setup & tuning</li>
        <li>Bench testing protocol</li>
      </ul>
    </div>
  </div>
</section>

<!-- ── PHASE 01: DESIGN & CAD ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Process</p>
  <div class="phase-header r">
    <span class="phase-num">01</span>
    <span class="phase-name">Design & CAD</span>
  </div>
  <p class="problem-text r" style="margin-bottom: 1.25rem;">
    After research into existing payload drone designs, we designed the frame, arms,
    cover, and payload bay from scratch in CAD. The goal from the start was to make
    every printed part <strong>efficient to produce and assemble</strong> — applying DFM/DFA
    principles to minimize support structures, reduce print time, and keep hardware
    requirements simple (primarily screws).
  </p>
  <ul class="phase-bullets r">
    <li>Designed the frame for clean screw-together assembly with no bonding required</li>
    <li>Arms were designed as separate printed parts to allow replacement if damaged</li>
    <li>Payload bay integrated directly into the frame geometry rather than bolted on as an afterthought</li>
    <li>Ran <strong>static FEA on the arms and frame</strong> based on expected flight loads to validate structural integrity and determine factor of safety before committing to final prints</li>
  </ul>
</section>

<!-- ── PHASE 02: ELECTRICAL INTEGRATION ──────────────────────────────────── -->
<section class="proj-section">
  <div class="phase-header r">
    <span class="phase-num">02</span>
    <span class="phase-name">Electrical Integration</span>
  </div>
  <p class="problem-text r" style="margin-bottom: 1.25rem;">
    The <strong>TAKER G4 AIO board</strong> serves as the flight controller and ESC in one —
    it handles motor control, sensor fusion, and receiver communication on a single compact
    board. This kept the wiring manageable inside the frame. The rest of the electrical
    system: SunnySky brushless motors on each arm, an ExpressLRS EP1 receiver for RC link,
    and a LiPo battery.
  </p>
  <ul class="phase-bullets r">
    <li>Laid out the full circuit before touching a soldering iron — mapped every connection and confirmed pin assignments for the AIO board</li>
    <li>Performed precise PCB soldering by hand, working through motor pads, power leads, and receiver connections methodically</li>
    <li>After soldering, ran <strong>continuity and isolation testing</strong> on every connection before powering anything on — catching any bridged pads or incomplete joints cold</li>
  </ul>

  <div class="proj-img-wrap r" style="margin-top: 1.5rem;">
    <img class="proj-img" src="/assets/images/drone/FlightController.jpg" alt="TAKER G4 AIO flight controller with soldered connections" loading="lazy" />
    <p class="proj-img-caption">TAKER G4 AIO — hand-soldered motor leads, power connections, and ExpressLRS EP1 receiver wiring</p>
  </div>
</section>

<!-- ── PHASE 03: SOFTWARE & FLIGHT TESTING ──────────────────────────────────── -->
<section class="proj-section">
  <div class="phase-header r">
    <span class="phase-num">03</span>
    <span class="phase-name">Software & Flight Testing</span>
  </div>
  <p class="problem-text r" style="margin-bottom: 1.25rem;">
    With the airframe assembled and electronics validated, we used <strong>BetaFlight
    Configurator</strong> to set up and tune the flight controller — configuring motor
    direction, receiver protocol, PID parameters, and arming behavior. Before any flight
    attempt, we ran rigorous bench testing: motors spinning up correctly, receiver
    input registering as expected, failsafe behavior confirmed.
  </p>
  <ul class="phase-bullets r">
    <li>Configured BetaFlight for the TAKER G4 board: motor mapping, ESC protocol, RC link setup</li>
    <li>Tuned PID baseline and confirmed control surface response through stick input testing on the bench</li>
    <li>Verified failsafe behavior and arming/disarming sequence before moving to outdoor flight</li>
  </ul>

  <div class="callout-box r" style="margin-top: 1.5rem;">
    <p class="callout-eyebrow">Result</p>
    <p class="callout-title">Flight achieved — with room to grow</p>
    <p class="callout-text">
      The drone flew. That said, further simulation testing and software debugging would
      be needed to improve reliability for repeated or sustained flight. We hit the core
      engineering goal — a fully 3D-printed, hand-built quadcopter that leaves the ground —
      and identified clearly where the next iteration should focus.
    </p>
  </div>
</section>

<!-- ── BACK BUTTON ──────────────────────────────────── -->
<div class="proj-footer-nav r">
  <a href="/projects/" class="btn btn-ghost">
    <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><polyline points="15 18 9 12 15 6"/></svg>
    Back to Projects
  </a>
</div>
