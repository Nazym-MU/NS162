---
id: NZ-29
title: Instrument the loops to count HBM reads and writes by block size
category: learning
project: flashattention
milestone: IO cost is measured, not asserted
status: backlog
estimate: 60
visibility: public
done_when: the forward and backward loops report counted HBM reads and writes as a function of block size, with the count derived from the loop structure and cross-checked by hand for one small configuration
blocks: [NZ-33]
created: 2026-08-12
---
Counting IO, not timing it. Phase 1 is expected to be slower than
`F.scaled_dot_product_attention`, so wall-clock here would measure nothing useful.

The hand check on one configuration is what makes the instrumentation trustworthy
before it is plotted.
