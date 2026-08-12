---
id: NZ-27
title: Implement tiled forward attention with a running output accumulator
category: learning
project: flashattention
milestone: tiled forward attention matches naive
status: backlog
estimate: 90
visibility: public
done_when: an outer loop over Q blocks and inner loop over K/V blocks maintaining m, l, and a rescaled running output accumulator passes torch.allclose against the naive attention reference, for at least two block sizes that do not evenly divide the sequence length
blocks: [NZ-31]
created: 2026-08-12
---
Outer loop over Q blocks, inner loop over K/V blocks. The output accumulator gets
rescaled by the same factor derived in NZ-26.

Ragged block sizes are in `done_when` deliberately: a tiling bug that only shows up on
the last partial tile is easy to miss if N is always a multiple of the block size.
