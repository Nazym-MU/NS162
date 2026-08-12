---
id: NZ-21
title: Write and launch a vector-add CUDA kernel, verified against CPU output
category: learning
project: cuda-from-scratch
milestone: first kernel runs
status: todo
estimate: 60
visibility: public
done_when: a CUDA kernel adds two arrays on the GPU and its output matches a CPU-computed reference exactly, on real hardware (not just compiled)
blocks: [NZ-22]
created: 2026-08-02
---
The canonical first kernel — proves toolchain, launch config, and memory transfer all
work before anything more interesting is attempted.
