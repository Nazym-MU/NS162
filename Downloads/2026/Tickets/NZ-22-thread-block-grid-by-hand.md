---
id: NZ-22
title: Work out a thread/block/grid indexing scheme by hand for a 2D problem
category: learning
project: cuda-from-scratch
milestone: first kernel runs
status: todo
estimate: 45
visibility: public
done_when: a 2D kernel (e.g. matrix element-wise op) correctly indexes every element exactly once, with the block/grid math written out by hand and matching the running result
blocks: []
created: 2026-08-02
---
Builds on NZ-21's 1D case. This is the ticket where thread indexing stops being magic.
