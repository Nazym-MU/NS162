---
type: project
slug: flashattention
title: FlashAttention From Scratch (FA1–FA4)
---
# FlashAttention From Scratch (FA1–FA4)

From-scratch study and reimplementation of the FlashAttention line of work, with a
written analysis of why each version exists.

This is a **GPU systems project, not an ML architecture project**. FlashAttention
computes exactly the same function as standard scaled dot-product attention; it is not
an approximation. Everything interesting is memory hierarchy, not modelling.

Deliverable is a repo, not a notebook: `kernels/` for real code, `notebooks/` for
exposition and tests that import from `kernels/`.

## Milestones (in order)

1. **online softmax is correct** — blockwise softmax with running max `m` and running
   normalizer `l` matches one-pass softmax, with the rescale factor derived rather than
   copied.
2. **tiled forward attention matches naive** — `torch.allclose` against naive attention,
   per-row logsumexp saved for the backward.
3. **backward pass passes gradcheck** — recomputation-based backward, nothing `N x N`
   ever stored, verified by `torch.autograd.gradcheck` in float64.
4. **IO cost is measured, not asserted** — HBM reads/writes counted as a function of
   block size and plotted against the `O(N^2 d^2 / M)` bound.
5. **FA1/FA2 run as Triton kernels** — real SRAM tiling on a rented/Colab GPU,
   reproducing FA1 and FA2 behaviour. Triton, not CUDA C++.
6. **FA3/FA4 written up** — roofline analysis only, no implementation. See hardware.

Milestones 1–4 are Phase 1 and run locally, ticketed as NZ-25 through NZ-33. Milestone 5
is Phase 2 and milestone 6 is Phase 3; both stay unticketed until Phase 1 lands, since
neither can start on this machine.

Only milestone 1 is active.

## Phase boundaries

- **Phase 1 (current): correctness in NumPy/PyTorch.** No kernels yet. Goal is to
  understand the algorithm well enough to write one. Expected to be *slower* than
  `F.scaled_dot_product_attention`. Do not benchmark this phase and do not treat its
  slowness as a bug.
- **Phase 2: Triton kernels.** Real SRAM tiling for FA1 and FA2.
- **Phase 3: analysis only.** FA3 (Hopper) and FA4 (Blackwell) get a roofline write-up.

## Hardware constraints

- Local machine is an M2 MacBook Air, 8 GB RAM. **No CUDA device.**
- Phase 1 runs locally; Phase 2 needs Colab or rented GPU time.
- Colab free tier is a T4 (Turing). Fine for FA1/FA2 Triton work.
- FA3 requires H100, FA4 requires B200. Neither is realistically available, hence
  Phase 3 being analysis only.

## Timebox

Phase 1 is three to four days. If milestone 3 still fails gradcheck after two days, the
bug is almost certainly in the milestone 1 rescaling, not in the backward. Go back
rather than grinding forward.

## Version summary (for the write-up)

- **FA1**: tiling + online softmax + backward recomputation. HBM traffic drops from
  `O(N^2)` to `~O(N^2 d^2 / M)`. FLOP count goes *up*; it wins because attention is
  memory bound.
- **FA2**: mostly scheduling, not new hardware. Fewer non-matmul FLOPs, added
  parallelism over the sequence dimension, repartitioned warp work (split Q instead of
  K/V) to remove a shared-memory sync.
- **FA3**: Hopper co-design. TMA, async WGMMA, warp specialization, ping-pong
  scheduling, FP8.
- **FA4**: Blackwell co-design. B200 roughly doubles tensor core throughput while shared
  memory bandwidth and exponential units barely scale, so non-MMA units became the
  bottleneck. Response: software-emulated exponentials, conditional softmax rescaling,
  tensor memory, 2-CTA MMA. Written entirely in CuTe-DSL (Python), not C++.

## Working preferences

- Derive results, do not assert them. If a formula appears, show where it comes from.
- Direct feedback. If an approach is wrong or a test is passing for the wrong reason,
  say so plainly.
- No em-dashes in prose.
