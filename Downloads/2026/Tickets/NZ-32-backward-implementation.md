---
id: NZ-32
title: Implement the tiled backward pass with recomputation, verified by gradcheck
category: learning
project: flashattention
milestone: backward pass passes gradcheck
status: backlog
estimate: 90
visibility: public
done_when: torch.autograd.gradcheck passes on a small float64 input, S and P are recomputed inside the loop from Q, K, V and the saved logsumexp, and a peak-memory check confirms no N x N buffer is ever allocated
blocks: [NZ-29]
created: 2026-08-12
---
The hard ticket. Recompute S and P inside the loop rather than storing them, using the
identity derived in NZ-28.

Gradcheck alone would still pass if an N x N intermediate were quietly materialized, so
the memory assertion is part of `done_when` rather than assumed.

If gradcheck fails after two days, the bug is almost certainly in the NZ-26 rescaling.
Go back rather than grinding forward.
