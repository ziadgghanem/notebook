---
layout: post
title: 'Algebraic Topology'
---

## Concepts

Fundamental Group
Let $$X$$ be a topological space, we define a path in our space with a continous map $$\alpha: I \rightarrow X.$$
*In this post we will use $$I$$ to denote the unit interval $$[0,1].$$*

-   A path $$\alpha: I \rightarrow X$$ whose initial and endpoints coincide in $$X$$ ( i.e. $$\alpha(0) = \alpha(1) = p$$) we call a loop based at $$p \in X$$.
-   We call a loop that can be contracted to a point (denoted $$\alpha \sim \cdot$$) *simple* otherwise it is called non-contractible. 

We are interested in using non-contractible loops to distinguish between topological spaces. Define the following set:

$$
\LARGE
G(X) := \{ \, \alpha: S^1 \rightarrow X \mid \alpha \nsim \cdot \, \}
$$

Remark: this set is too fine for our purposes, instead we would like to assign an equivalence relation to loops in $$G(X).$$ Let $$ \< \alpha \>$$ denote the homotopy class of $$\alpha \in G(X)$$ where $$\beta \in \< \alpha \> \iff \beta \simeq \alpha .$$

$$
\LARGE
\hat{G}(X) := \{ \, \< \alpha \> \mid \alpha \in G(X) \, \}
$$