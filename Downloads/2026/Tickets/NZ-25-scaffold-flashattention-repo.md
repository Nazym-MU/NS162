---
id: NZ-25
title: Scaffold the FlashAttention repo with kernels/ and notebooks/
category: learning
project: flashattention
milestone: online softmax is correct
status: todo
estimate: 30
visibility: public
done_when: a repo exists with kernels/ and notebooks/, a notebook successfully imports a function from kernels/, and a naive attention reference implementation lives in kernels/ for later tests to compare against
blocks: [NZ-26]
created: 2026-08-12
---
Deliverable is a repo, not a single notebook. Getting the import boundary right up front
means every later test compares against one shared reference rather than a copy pasted
into each notebook.

The naive attention reference written here is what NZ-27 asserts against.
