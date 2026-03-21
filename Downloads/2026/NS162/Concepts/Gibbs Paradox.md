Removing and replacing a barrier between two gas halves should conserve entropy — resolves an apparent violation of the 2nd law via indistinguishability.
## Same Gas
**Before barrier removal:** $S = 2Nk_B \ln V$
**After removal (naive):** $S = 2Nk_B \ln(2V) = 2Nk_B \ln V + 2Nk_B \ln 2$ ← entropy increased?
**Fix:** particles are indistinguishable, so microstates $= V^N / N!$
$$S = 2k_B \ln \frac{V^N}{N!} = 2Nk_B \ln V - 2Nk_B \ln N - 2Nk_B$$
**After removal (corrected):**
$$S = k_B \ln \frac{(2V)^{2N}}{(2N)!} = 2Nk_B \ln V - 2Nk_B \ln N - 2Nk_B$$
Same — no entropy change.
## Two Different Gases
Now the two sides have distinguishable particles (blue vs red). Mixing increases entropy:
$$\Delta S = 2Nk_B \ln 2$$
Replacing the barrier leaves $N/2$ blue and $N/2$ red on each side — not the original state. The number of ways to arrange this mixed partition adds back:
$$\Delta S = 2Nk_B \ln 2$$
So entropy stays elevated — consistent with the 2nd law.
**Key point:** entropy change from mixing depends on whether the particles are distinguishable. Same gas → no entropy of mixing. Different gases → $\Delta S = 2Nk_B \ln 2$.