---
id: NZ-40
title: Compare QEM output against Blender's Decimate modifier
category: learning
project: geometry-processing
milestone: decimation works and matches Blender
status: backlog
estimate: 60
visibility: public
done_when: the same mesh is decimated to the same ratio by both implementations and compared by Hausdorff distance to the original, with any systematic difference traced to a specific choice (boundary handling, collapse validity, or the singular-quadric fallback) rather than left as noise
blocks: []
created: 2026-08-12
---
Closes milestone 2. Blender is the reference implementation, so a difference is
information about a choice one of us made.

Comparing to the *original* rather than to each other is deliberate: two decimators can
pick different edges and both be correct, so vertex-to-vertex comparison would fail for
the wrong reason. Distance to the source surface is the quality measure that matters.
