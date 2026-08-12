---
id: NZ-34
title: Build the mesh incidence matrices from a loaded triangle mesh
category: learning
project: geometry-processing
milestone: a mesh is a sparse matrix to me
status: todo
estimate: 75
visibility: public
done_when: vertex-edge and edge-face incidence matrices are built as scipy sparse matrices for a loaded mesh, and d1 @ d0 is verified to be the zero matrix, which is the discrete statement that the boundary of a boundary is empty
blocks: [NZ-35]
created: 2026-08-12
---
Start from the incidence structure rather than the geometry, since every operator later
is assembled from these.

The `d1 @ d0 == 0` check is the ticket's real content: it is a property of the
discretization that holds exactly, so a nonzero result means the connectivity is wrong
before any geometry is involved.
