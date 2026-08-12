---
id: NZ-31
title: Save per-row logsumexp from the forward pass
category: learning
project: flashattention
milestone: tiled forward attention matches naive
status: backlog
estimate: 30
visibility: public
done_when: the tiled forward returns per-row logsumexp alongside the output, matching torch.logsumexp on the naive attention scores to float64 tolerance
blocks: [NZ-28]
created: 2026-08-12
---
Small ticket, but separated because it is the interface between forward and backward.

Not optional bookkeeping: NZ-28 recomputes S and P from this, and that is what avoids
ever materializing an N x N matrix.
