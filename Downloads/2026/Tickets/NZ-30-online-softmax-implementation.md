---
id: NZ-30
title: Implement blockwise online softmax and test against one-pass softmax
category: learning
project: flashattention
milestone: online softmax is correct
status: todo
estimate: 75
visibility: public
done_when: a blockwise softmax maintaining running max m and running normalizer l matches a one-pass softmax to float64 tolerance on random inputs, including an input with a large positive outlier that would overflow a naive exp
blocks: [NZ-27]
created: 2026-08-12
---
Online softmax alone, no attention yet. Uses the rescale factor derived in NZ-26.

The outlier case is the point of the running max: test it explicitly rather than only
on well-conditioned random inputs, or the test passes for the wrong reason.
