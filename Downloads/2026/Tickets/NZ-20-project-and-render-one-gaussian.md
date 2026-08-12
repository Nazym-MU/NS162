---
id: NZ-20
title: Project one 3D Gaussian to a screen-space ellipse and render it
category: project
project: splat-rasterizer
milestone: one gaussian on screen
status: todo
estimate: 90
visibility: public
done_when: a single 3D Gaussian, given a camera, projects to a screen-space ellipse and renders as a recognizable blob at the right screen position
blocks: []
created: 2026-08-02
---
Brings together NZ-18 (rasterization), NZ-19 (covariance), and NZ-7 (the projection
Jacobian) into one working pipeline. This is the ticket where "one gaussian on screen"
actually becomes demoable.
