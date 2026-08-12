---
id: NZ-26
title: Derive the online softmax rescale factor by hand
category: learning
project: flashattention
milestone: online softmax is correct
status: todo
estimate: 45
visibility: public
done_when: the rescale factor exp(m_old - m_new) is written out with the step showing why a running normalizer computed under an old max must be corrected when the max updates, not asserted from the paper
blocks: [NZ-30]
created: 2026-08-12
---
Derivation before code. This is the load-bearing piece of the whole project: if the
rescaling is wrong, it surfaces as a mysterious backward failure three tickets later.

Per the project timebox, if the backward (NZ-31/NZ-32) fails gradcheck for two days,
come back to this ticket rather than grinding forward.
