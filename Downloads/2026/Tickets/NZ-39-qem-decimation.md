---
id: NZ-39
title: Implement QEM edge-collapse decimation with a priority queue
category: learning
project: geometry-processing
milestone: decimation works and matches Blender
status: backlog
estimate: 90
visibility: public
done_when: a mesh decimates to a target triangle count with quadrics accumulated on collapse and the queue updated lazily, and the result is a valid manifold with no degenerate or flipped triangles, checked rather than eyeballed
blocks: [NZ-40]
created: 2026-08-12
---
The afternoon implementation the brief promises, once NZ-38 has the math settled.

Manifold validity is in `done_when` because a decimator that produces a plausible
silhouette while quietly creating non-manifold edges or flipped normals looks correct in
a render and breaks everything downstream. Collapses that would flip a triangle need
rejecting.
