Entropy has units of bits
$$H = \sum_{i=1}^n p_i \cdot \text{number of bounces}_i$$
$$\text{number of bounces}=\log_2 (\text{number of outcomes})$$
$$\text{number of outcomes} = \frac{1}{p}$$
Therefore, $$H = \sum_{i=1}^n p_i \cdot \log_2(\frac{1}{p_i}) =  -\sum_{i=1}^n p_i \cdot \log_2(p_i)$$
Entropy is maximum when all outcomes are equally likely.
Huffman encoding

4 axioms for $H(\vec p)$ that takes a vector of probabilities and spits out uncertainty:
1. Continuity (if I only change the probabilities a little, the information of the process should change only a little).
2. Symmetry (if I reorder the list of probabilities I gave you, you should get the same answer).
3. Condition of Maximum Information: $H(\vec p)$ is at its maximum value when all the $p_i$ are equal.
4. Coarse-Graining. $$H(X) = H(X') + p_{bc}H(G)$$where $H(G)$ is the uncertainty of the choice between the group G containing b and c. 

Quantifying coding failure using KL-divergence:$$KL(p|q)=\sum_{i=1}^Nq(x_i)\log_2\frac{q(x_i)}{p(x_i)}$$where $p(x)$ is the distribution you trained on, and $q(x)$ is the observed distribution.
Conditional entropy of $X$ given $Y$: $$H(X|Y) =\sum_{j \in M} H(X|y_j)P(y_j)$$