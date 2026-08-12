---
id: NZ-38
title: Derive the quadric error metric and the optimal contraction point
category: learning
project: geometry-processing
milestone: decimation works and matches Blender
status: backlog
estimate: 75
visibility: public
done_when: the 4x4 quadric Q is derived as the sum of outer products of plane equations so that v^T Q v is the sum of squared distances to those planes, and the 3x3 system for the optimal contraction position is obtained by setting the gradient to zero, including what to do when that system is singular
blocks: [NZ-39]
created: 2026-08-12
---
Garland & Heckbert 1997. The whole method is one quadratic form, so the derivation is
short and worth doing properly.

The singular case is in `done_when` because it is not an edge case: it happens on flat
and symmetric regions, which real meshes are full of. A fallback to the edge midpoint
must be a decision, not a crash.
