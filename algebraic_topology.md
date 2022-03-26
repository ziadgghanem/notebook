---
layout: post
title: 'Algebraic Topology'
---

## Concepts

Fundamental Group
Let $$X$$ be a topological space, we define a path in our space with a continous map $$\alpha: I \rightarrow X.$$

*In this post we will use $$I$$ to denote the unit interval $$[0,1].$$*

We will use the following composition operation on the space of paths $$P(X):=\{ \alpha: I \rightarrow X \}: \\$$ 
Consider the paths $$\alpha , \beta \in P(X)$$ with $$\alpha(0) = \beta(1) = p \in X.$$ 
We define a new path $$\alpha \circ \beta : I \rightarrow X$$ and call it the composition of $$\alpha$$ and $$\beta.$$

$$
\alpha \circ \beta = 
        \begin{cases} 
          \alpha(2t) & t \in [0, \frac{1}{2}] \\
          \beta(2t-1) & t \in [\frac{1}{2}, 1] 
       \end{cases}
$$

Terminology:
-   We say that two paths $$\alpha , \beta \in P(X)$$ are *homotopic* if there exists a continuous map $$h_t: I \rightarrow X, t \in I$$ with $$h_0 = \alpha$$ and $$h_1 = \beta.$$ In which case we write $$\alpha \simeq \beta.$$
-   A path $$\alpha: I \rightarrow X$$ whose initial and endpoints coincide in $$X$$ ( i.e. $$\alpha(0) = \alpha(1) = p$$) we call a loop based at $$p \in X$$.
-   We call a loop that can be contracted to a point (by which we mean the loop is homotopic to a point $$\alpha \simeq \cdot$$) *simple* otherwise it is called non-contractible. 
We are interested in using non-contractible loops to distinguish between topological spaces. Define the following set:

$$
\Large
G(X) := \{ \, \alpha: S^1 \rightarrow X \mid \alpha \nsim \cdot \, \}
$$

Note that this set is still too *fine* for our purposes, it differentiates between loops that we would rather identify, in particular it would be convenient to consider loops belonging to the same homotopy class as characterizing the same loop in our space. To this point we will assign the following equivalence relation to loops in $$G(X): \\$$ 

Let $$ \langle \alpha \rangle$$ denote the homotopy class of $$\alpha \in G(X)$$ where $$\beta \in \langle \alpha \rangle \iff \beta \simeq \alpha .$$

$$
\Large
\hat{G}(X) := \{ \, \langle \alpha \rangle \mid \alpha \in G(X) \, \}
$$
