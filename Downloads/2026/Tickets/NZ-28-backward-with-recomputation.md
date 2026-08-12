---
id: NZ-28
title: Derive the backward identity dS = P * (dP - D)
category: learning
project: flashattention
milestone: backward pass passes gradcheck
status: backlog
estimate: 90
visibility: public
done_when: dS = P * (dP - D) with D_i = rowsum(dO * O)_i is derived in full from the softmax Jacobian, including the step showing sum_k P_ik dP_ik = sum_k O_ik dO_ik, and checked numerically against a finite-difference dS on a small input
blocks: [NZ-32]
created: 2026-08-12
---
Derivation before code, and the reason the backward needs no N x N storage: D is a
single number per row.

The numeric finite-difference check is in `done_when` so the identity is confirmed
before it gets embedded in a tiled loop, where a sign error is much harder to localize.
