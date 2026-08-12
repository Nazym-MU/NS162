---
id: NZ-35
title: Derive the cotangent weights from the Dirichlet energy
category: learning
project: geometry-processing
milestone: a mesh is a sparse matrix to me
status: todo
estimate: 90
visibility: public
done_when: the cotan weight (cot alpha + cot beta)/2 is derived by taking the gradient of a piecewise-linear hat function over a triangle and integrating the Dirichlet energy, with the step showing where the cotangents come from geometrically, not quoted from the paper
blocks: [NZ-36]
created: 2026-08-12
---
The single most important matrix in the field, and the place where "why these weights"
is the actual question. Desbrun 1999 introduces it; the derivation is what makes the
rest of the project make sense.

This is the discretization argument the project exists for. Copying the formula here
would hollow out every later milestone.
