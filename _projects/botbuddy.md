---
layout: project-custom
title: "BotBuddy: Remote-Controlled Robot with Live Video"
category: "Robotics / Software"
org: "Personal Project"
role: "Solo — Self-initiated"
date_range: "May – August 2025"
status: "V0 Complete"
tools:
  - "Hardware"
  - "Software"
  - "Systems"
  - "Mechanical"
tags:
  - "Robotics"
  - "Raspberry Pi"
  - "Python"
  - "Flask"
description: >-
  A mobile wheeled robot with a live camera feed and Flask-based remote control,
  accessible from anywhere via Ngrok tunneling. Built to stay connected from afar.
---

<!-- ── MOTIVATION ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">The Idea</p>
  <h2 class="section-heading r">A robot built to stay connected</h2>
  <p class="problem-text r">
    BotBuddy started from a personal motivation: I wanted a way to stay connected with
    loved ones from afar — not just over video call, but something more present and
    interactive. A robot that could move around, stream live video, and be driven
    remotely from anywhere felt like the right kind of project: real hardware, real
    software, and a reason to actually build it well.
  </p>

  <div class="proj-img-wrap r" style="margin-top: 1.75rem;">
    <img class="proj-img" src="/assets/images/botbuddy/BotBuddyV0Robot.png" alt="BotBuddy V0 rover — Raspberry Pi, motor driver, camera, wiring visible" loading="lazy" />
    <p class="proj-img-caption">BotBuddy V0 — Raspberry Pi 3 Model B, TB6612FNG motor driver, DC gear motors, and camera module</p>
  </div>
</section>

<!-- ── TOOLS BREAKDOWN ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">Tools & Skills</p>
  <div class="role-grid r" style="grid-template-columns: repeat(2, 1fr);">
    <div class="role-card r">
      <p class="role-name">Hardware</p>
      <ul class="role-bullets">
        <li>Raspberry Pi 3 Model B</li>
        <li>TB6612FNG dual motor driver</li>
        <li>DC gear motors</li>
        <li>GPIO interfacing</li>
        <li>4×AA battery pack + USB power bank</li>
      </ul>
    </div>
    <div class="role-card r">
      <p class="role-name">Software</p>
      <ul class="role-bullets">
        <li>Python (backend logic)</li>
        <li>Flask (web server + control interface)</li>
        <li>HTML (control page)</li>
        <li>Ngrok (secure web tunneling)</li>
      </ul>
    </div>
    <div class="role-card r">
      <p class="role-name">Systems</p>
      <ul class="role-bullets">
        <li>Live video streaming</li>
        <li>Web-based remote control</li>
        <li>Remote access over public URL</li>
      </ul>
    </div>
    <div class="role-card r">
      <p class="role-name">Mechanical & Prototyping</p>
      <ul class="role-bullets">
        <li>Breadboarding + wiring</li>
        <li>3D printing <span style="color:var(--muted);font-style:italic;">(V1 planned)</span></li>
        <li>Soldering <span style="color:var(--muted);font-style:italic;">(V1 planned)</span></li>
      </ul>
    </div>
  </div>
</section>

<!-- ── HOW V0 WORKS ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">How V0 Works</p>
  <div class="phase-header r">
    <span class="phase-num">Hardware</span>
    <span class="phase-name">The physical system</span>
  </div>
  <p class="problem-text r" style="margin-bottom: 1.25rem;">
    The robot is built around a <strong>Raspberry Pi 3 Model B</strong>, which handles all
    compute — running the Flask server, processing movement commands, and streaming camera
    output. Motor control runs through a <strong>TB6612FNG dual motor driver</strong>, wired
    to the Pi's GPIO pins and driving two DC gear motors. Power is intentionally split:
    a 4×AA battery pack runs the motors to keep their current draw off the Pi's supply,
    while a USB power bank runs the Pi and camera separately.
  </p>
  <ul class="phase-bullets r">
    <li>GPIO pins control the motor driver inputs (direction + PWM speed)</li>
    <li>Camera module connects directly to the Pi's CSI port for low-latency video capture</li>
    <li>Split power supply prevents motor noise from affecting the Pi</li>
  </ul>
</section>

<section class="proj-section">
  <div class="phase-header r">
    <span class="phase-num">Software</span>
    <span class="phase-name">Control & streaming</span>
  </div>
  <p class="problem-text r" style="margin-bottom: 1.25rem;">
    The control interface is a <strong>Flask web app hosted on the Pi itself</strong>. A simple
    HTML page lets users send movement commands — forward, back, left, right — handled in
    real time by a Python backend that translates each command into GPIO signals to the
    motor driver. The camera feed streams live through the same interface.
  </p>
  <ul class="phase-bullets r" style="margin-bottom: 1.5rem;">
    <li>Flask routes map directly to motor control functions in Python</li>
    <li>Live video streamed via MJPEG — no external service, runs entirely on the Pi</li>
    <li><strong>Ngrok tunneling</strong> exposes the Flask app via a secure public URL, enabling control from any network — not just the same Wi-Fi</li>
  </ul>

  <div class="proj-img-wrap r">
    <img class="proj-img" src="/assets/images/botbuddy/BotBuddyWebInterface.png" alt="BotBuddy web control interface showing live video feed and arrow key controls" loading="lazy" />
    <p class="proj-img-caption">Flask control interface — live camera feed with on-screen movement controls, accessible via Ngrok public URL</p>
  </div>
</section>

<!-- ── CURRENT STATE ──────────────────────────────────── -->
<section class="proj-section">
  <div class="callout-box r">
    <p class="callout-eyebrow">Current State — V0</p>
    <p class="callout-title">Proof of concept: it works, tape and all</p>
    <p class="callout-text">
      BotBuddy V0 is physically held together with tape and breadboards. That's intentional
      for a proof of concept — the goal was to validate the full stack (hardware, control
      software, remote access, live video) before investing in a polished form factor.
      V0 does exactly that: the concept is validated and the foundation is solid.
    </p>
  </div>
</section>

<!-- ── NEXT STEPS ──────────────────────────────────── -->
<section class="proj-section">
  <p class="section-eyebrow r">What's Next</p>
  <h2 class="section-heading r">V1 — making it real</h2>
  <ol class="next-steps-list r">
    <li>
      <span class="step-bullet">1</span>
      <span>Design and <strong>3D print a custom chassis</strong> — replace the current placeholder structure with a purpose-built frame sized for the electronics and payload bay</span>
    </li>
    <li>
      <span class="step-bullet">2</span>
      <span><strong>Replace temporary wiring with soldered connections</strong> — move off the breadboard and make the electronics robust enough for actual use</span>
    </li>
    <li>
      <span class="step-bullet">3</span>
      <span>Add <strong>microphone or text-to-speech capabilities</strong> for basic two-way interaction — the feature that makes it genuinely useful for the original goal</span>
    </li>
  </ol>
</section>

<!-- ── CLOSING ──────────────────────────────────── -->
<section class="proj-section">
  <p class="problem-text r" style="color: var(--muted); font-style: italic;">
    This project has been a fun and hands-on way to apply both hardware and software skills —
    and I'm excited to keep building on it.
  </p>
</section>

<!-- ── BACK BUTTON ──────────────────────────────────── -->
<div class="proj-footer-nav r">
  <a href="/projects/" class="btn btn-ghost">
    <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><polyline points="15 18 9 12 15 6"/></svg>
    Back to Projects
  </a>
</div>
