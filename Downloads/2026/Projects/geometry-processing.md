---
type: project
slug: geometry-processing
title: Geometry Processing (Linear Algebra on Meshes)
---
# Geometry Processing (Linear Algebra on Meshes)

Implement the papers behind the Blender modifiers I already use. A mesh is an incidence
structure, operators on it are sparse matrices, and most features reduce to solving or
eigendecomposing one of them.

The field name is the thing that unlocks the literature: **geometry processing**.

The point is **not** the linear algebra. Quadratic forms, sparse Cholesky, SVD, and
symmetric eigenproblems are all familiar already. The actual content is the
**discretization**: why the cotangent weights are the right ones, what a mass matrix
means on a triangle mesh, and when a discrete operator silently fails to preserve a
continuous property. Go in for the discretization arguments, not for exotic algebra.

## Milestones (in order)

1. **a mesh is a sparse matrix to me** — I can build the incidence and cotan-Laplacian
   operators for a mesh by hand and say what each entry means.
2. **decimation works and matches Blender** — QEM simplification runs on a real mesh and
   its output is compared against Blender's Decimate on the same input.
3. **smoothing works and matches Blender** — cotan-Laplacian implicit fairing, compared
   against Blender's Laplacian Smooth.
4. **unwrapping works and matches Blender** — LSCM produces a UV atlas, compared against
   Blender's LSCM unwrap.
5. **deformation works and matches Blender** — ARAP deformation, compared against
   Blender's shape-key and UV tooling.
6. **the spectral payoff** — manifold harmonics: Laplacian eigenvectors as a Fourier
   basis on a surface. The reason to care about the operator, not just use it.

Only milestone 1 is active.

## Approach

Implement in Python with numpy/scipy, checking against libigl rather than calling it for
the core step. `igl.cotmatrix`, `igl.arap`, `igl.lscm` are one line each, which makes
libigl the ideal oracle and a poor teacher. Use it to verify, not to substitute.

Compare every result to Blender's output on the same mesh. That comparison is the whole
point: each milestone is a feature I already use, so a silent discretization error shows
up as a visible difference.

## Sequence and why this order

QEM first, then cotan smoothing, then LSCM, then ARAP. Together these cover quadratic
forms, sparse SPD solves, least squares, SVD, and eigenproblems, and each one is a
Blender feature with a paper behind it.

## Reading

Primary entry point, before any papers:

- Keenan Crane, *Discrete Differential Geometry: An Applied Introduction* (CMU 15-458).
  Free PDF notes, YouTube lectures, coding exercises. Built exactly around the
  mesh-as-sparse-matrix lens.
- *Polygon Mesh Processing* (Botsch, Kobbelt, Pauly, Alliez, Levy). The book equivalent.
  Shorter, more engineering-oriented, less proof-heavy.

Papers, roughly by value per page:

- Garland & Heckbert, *Surface Simplification Using Quadric Error Metrics* (1997). Read
  first. Each vertex carries a symmetric 4x4 $Q$; error of placing a vertex at $v$ is
  $v^T Q v$; collapsing an edge adds the $Q$s and minimizes a quadratic form via a 3x3
  solve. This is Blender's Decimate modifier.
- Desbrun et al., *Implicit Fairing of Irregular Meshes using Diffusion and Curvature
  Flow* (1999). Introduces the cotangent Laplacian; smoothing is solving
  $(I - \lambda L)x' = x$. The cotan Laplacian is the single most important matrix here.
- Sorkine et al., *Laplacian Surface Editing* (2004) and Sorkine, *Laplacian Mesh
  Processing* survey (2005). Differential coordinates, least-squares deformation, why
  $L^T L$ systems.
- Sorkine & Alexa, *As-Rigid-As-Possible Surface Modeling* (2007). Alternates a sparse
  linear solve with a per-vertex SVD for the closest rotation (orthogonal Procrustes).
- Levy et al., *Least Squares Conformal Maps* (2002). Blender's LSCM unwrap.
  Cauchy-Riemann discretized into an overdetermined sparse least-squares system. Pair
  with Mullen et al., *Spectral Conformal Parameterization* (2008), which recasts it as
  a generalized eigenvalue problem.
- Jacobson et al., *Bounded Biharmonic Weights for Real-Time Deformation* (2011). Rigging
  weights as a constrained QP with the bi-Laplacian. Explains automatic weights.
- Kavan et al., *Geometric Skinning with Approximate Dual Quaternion Blending* (2008).
  Blender's dual quaternion armature option; the rotation-representation side.
- Vallet & Levy, *Spectral Geometry Processing with Manifold Harmonics* (2008). The
  payoff paper if the linear algebra is the driver.
- Botsch & Sorkine, *On Linear Variational Surface Deformation Methods* (2008). Survey
  tying the deformation papers together; read after two or three of the above.

## Tools

- **libigl** — header-only C++ on Eigen with Python bindings. The tutorial is effectively
  a full course, one chapter per paper above. Use as oracle.
- **geometry-central** + **Polyscope** (Nick Sharp) — cleaner halfedge and vector field
  abstractions; Polyscope is the fastest way to look at what you computed.
- **ddg-exercises-js** — Crane's course skeletons with tests, in the browser.
- **gpytoolbox**, **trimesh** for Python experimentation; **Open3D** for scans and point
  clouds; **CGAL** for robustness and exact predicates.
- Blender's own source is readable here: `source/blender/geometry/`, plus decimate and
  laplacian-smooth in `blenkernel`, map directly onto the papers.

## Working preferences

- Derive results, do not assert them. If a formula appears, show where it comes from.
- Direct feedback. If an approach is wrong or a test is passing for the wrong reason, say
  so plainly.
- No em-dashes in prose.
