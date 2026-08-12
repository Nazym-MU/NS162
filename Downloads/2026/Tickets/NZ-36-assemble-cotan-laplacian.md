---
id: NZ-36
title: Assemble the cotan Laplacian and mass matrix, verified against libigl
category: learning
project: geometry-processing
milestone: a mesh is a sparse matrix to me
status: todo
estimate: 75
visibility: public
done_when: hand-assembled L and M match igl.cotmatrix and igl.massmatrix to numerical tolerance, L is verified symmetric with rows summing to zero, and L applied to a constant function returns zero on interior vertices
blocks: [NZ-37]
created: 2026-08-12
---
libigl is the oracle here, not the implementation. Matching it is necessary but not
sufficient, hence the structural checks alongside.

Rows summing to zero and annihilating constants are the discrete versions of the
Laplacian killing constant functions. A weight sign error can still match libigl on one
mesh while breaking these, so both are in `done_when`.
