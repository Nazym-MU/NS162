---
id: NZ-33
title: Plot measured HBM traffic against the O(N^2 d^2 / M) bound
category: learning
project: flashattention
milestone: IO cost is measured, not asserted
status: backlog
estimate: 60
visibility: public
done_when: measured HBM traffic is plotted against the O(N^2 d^2 / M) bound across block sizes, with any departure from the bound's shape explained rather than noted
blocks: []
created: 2026-08-12
---
Closes Phase 1. The explanation matters more than the plot: the bound is asymptotic and
ignores constants, so the measured curve is not expected to lie on top of it.

This is what sets up the Phase 3 roofline analysis, where the same accounting argument
makes the FA3/FA4 write-up quantitative rather than descriptive.
