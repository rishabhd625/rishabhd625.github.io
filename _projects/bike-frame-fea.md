---
layout: project
title: "Bike Frame FEA Analysis & Optimization"
category: "Structural Analysis"
course: "MAE 3150 – Engineering Simulations & Design"
date_range: "April – May 2026"
tools:
  - "Fusion 360"
  - "Ansys Mechanical 2025 R2"
  - "Response Surface Optimization (MOGA)"
tags:
  - "FEA"
  - "Ansys"
  - "Fusion 360"
  - "Optimization"
description: >-
  Shell-theory FEA and MOGA-driven optimization of an aluminum bike-share frame.
  Achieved 42% material reduction while maintaining a factor of safety of 3.5.

problem: >-
  Bike-share programs must balance two competing demands: rider safety and operational cost.
  A frame that is over-engineered wastes material and raises the cost per unit; one that is
  under-designed risks failure under the highly variable loads of a shared-use environment.
  This project used finite element analysis to characterize the structural behavior of an
  aluminum alloy frame, then applied automated multi-objective optimization to find the
  minimum tube thickness that keeps the factor of safety comfortably above the target
  threshold — reducing material cost without compromising structural integrity.

steps:
  - number: "01"
    title: "Initial Analysis"
    description: >-
      Constructed 2D frame geometry in Fusion 360 using surface tools, then imported into
      Ansys Mechanical 2025 R2. Meshed at a 4mm element size with a shell-theory model
      (6 degrees of freedom per node). Boundary conditions: zero displacement at the
      handlebars and rear wheel contact point; 700N downward seat load and 150N pedal load.
      Material set to aluminum alloy at 2mm uniform thickness. Results showed maximum
      deformation of ~0.1mm near the seat and a factor of safety of 15 across most of
      the frame — confirming the baseline design is structurally over-engineered and a
      strong candidate for material reduction.

  - number: "02"
    title: "Design Modifications"
    description: >-
      Removed the top tube to cut material, added a battery weight load on the bottom tube
      to represent realistic e-bike loading conditions, and introduced a hole in the
      low-stress upper region of the bottom tube. Stress concentration increased slightly
      around the cutout but remained well within safe limits. This step demonstrated that
      stress-map-guided geometry decisions can meaningfully reduce mass without introducing
      structural risk, and established the modified geometry as the baseline for optimization.

  - number: "03"
    title: "Response Surface Optimization"
    description: >-
      Configured a parametric sweep of seat tube thickness from 1–2mm, then launched a
      Response Surface Optimization using the MOGA (Multi-Objective Genetic Algorithm) in
      Ansys Mechanical. Objective: minimize frame mass while maintaining FOS ≥ 3.5. After
      1,511 evaluations the algorithm converged on an optimal thickness of ~1.16mm. Maximum
      Von-Mises stress at the optimized geometry was ~64 MPa — well below aluminum's yield
      strength — confirming the result is both safe and material-efficient.

results:
  - stat: "42%"
    label: "Material Reduction"
    detail: "Lower tube material saved versus the original 2mm baseline design"
  - stat: "3.5×"
    label: "Factor of Safety"
    detail: "Maintained at or above the safety threshold after full optimization"
  - stat: "1,511"
    label: "MOGA Evaluations"
    detail: "Algorithm evaluations to converge on 1.16mm optimal seat tube thickness"

images:
  - label: "Initial Mesh (4mm elements)"
    src: /assets/images/bike-frame/mesh.png
  - label: "Von-Mises Stress Distribution"
    src: /assets/images/bike-frame/vonmises.png
  - label: "Deformation Contour"
    src: /assets/images/bike-frame/deformation.png
  - label: "Optimized Design"
    src: /assets/images/bike-frame/optimized.png
  - label: "MOGA Results Table"
    src: /assets/images/bike-frame/moga.png

learnings:
  - "Shell-theory FEA fundamentals and what 6-DOF node modeling means for thin-walled structures"
  - "Surface modeling in Fusion 360 — previously only worked with solid bodies"
  - "Parametric response surface optimization workflow end-to-end in Ansys Mechanical"
  - "Projecting sketches onto curved surfaces to create geometry cutouts in Fusion 360"
---
