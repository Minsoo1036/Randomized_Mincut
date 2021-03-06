# Randomized_Mincut
Karges Algorithm and Karger-Stein Algorithm


I implement the algorithms in two ways corresponding to the contraction implementations.
One is implementing the contraction by sampling two nodes randomly.**(node-based)**
Another one is implementing the contraction by sampling one existing edge randomly and selecting the corresponding nodes.**(edge-based)**

Edge-based is the original version of Kargers Algorithm.
But it has the time complexity **O(VE)**, rather than **O(V^2)** which Node-based takes. and I also wonder whether there is a way to implement edge-based in **O(V^2)**.

Anyway, in the experiments, Edge-based shows more reasonable solution of mincut compared to Node-based.

Karger-Stein Algorithm also depends on the algorithm of contraction.
and it comes to be efficient algorithm when applied to boosting framework.

When the success probability of boosting is 1-1/n and it comes to be edge-based, Kargers Algorithm takes **O(V^3 E log(V) )** and Karger-Stein Algorithm takes **O(V^2 log(V)^3 ).**
Furthermore, the state-of-the-art deterministic min-cut algorithm (Stoer-Wagner) takes **O(VE+V^2 log(V) ).** So Karger-Stein Algorithm can obtain gain when the graph is dense.

The code is based on **R**.
