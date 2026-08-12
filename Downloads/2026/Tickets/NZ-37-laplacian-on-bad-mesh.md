---
id: NZ-37
title: Find where the cotan Laplacian breaks on obtuse and degenerate triangles
category: learning
project: geometry-processing
milestone: a mesh is a sparse matrix to me
status: todo
estimate: 60
visibility: public
done_when: a mesh with obtuse triangles is shown to produce negative cotan weights, the consequence for the maximum principle is stated concretely, and the difference between barycentric and Voronoi mass matrices on that mesh is measured rather than described
blocks: []
created: 2026-08-12
---
Closes milestone 1. This is the "when does a discrete operator silently fail to preserve
a continuous property" question, made concrete.

Negative weights are exactly the case where smoothing can move a vertex outside the
convex hull of its neighbours, which the continuous operator never does. Worth seeing
happen before trusting the operator in milestones 2 through 6.
