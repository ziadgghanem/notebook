---
layout: post
title: 'Equivariant Marginalia'
---

1. [Conjugacy](#S1)
2. [$G$-Actions / $G$-Spaces](#S2)
    1. [Some Notations, Definitions, Properties](#S2s1)

## Conjugacy <a name="S1"></a>

In this section, let $G$ be any group.

<div class="definition" markdown="1">

**Definition:** Conjugacy of Subgroups

Two subgroups, $H \leq G$ and $K \leq G$, are said to be conjugate, denoted $H \sim K$ if and only if $\exists_{g \in G}$ such that $gHg^{-1} = K$
</div>

We denote by $(H)$ the conjugacy class of $H \leq G$

\begin{eqnarray}
(H) &:= \lbrace K \leq G \; : \; H \sim K \rbrace
\end{eqnarray}
{: style="text-align: center"}

Notice that conjugacy is an equivalence relation on the space of subgroups of $G$. We put

\begin{eqnarray}
\Phi(G) &:= \lbrace (H) \; : \; H \leq G \rbrace
\end{eqnarray}
{: style="text-align: center"}

<div class="definition" markdown="1">

**Definition:** Normality

A subgroup H is said to be normal in $G$, denoted $H \mathrel{\unlhd} G$, if and only if $\forall_{g \in G} gHg^{-1} = H$
</div>

In the context of the conjugacy relation we propose the following lemma.

<div class="proposition" markdown="1">

**Lemma:** 

$H \mathrel{\unlhd} G$ if and only if $H \sim K \implies K = G$
</div>

We might also consider the conjugacy of group elements. Denote the conjugacy of $h \in G$ with

\begin{eqnarray}
Cl_{G}(h) &:= \lbrace ghg^{-1} \; : \; g \in G \rbrace
\end{eqnarray}
{: style="text-align: center"}

Recall, the center of $G$ is the set

\begin{eqnarray}
Z(G) &:= \lbrace h \in G \; : \; gh=hg \; \forall_{g \in G} \rbrace
\end{eqnarray}
{: style="text-align: center"}

<div class="proposition" markdown="1">

**Lemma:** 

$Cl_{G}(h) = \lbrace h \rbrace$ if and only if $h \in Z(g)$
</div>

**Remark:** If $G$ is abelian, then $G = Z(G)$ such that $Cl_{G}(g) = \lbrace g \rbrace$ $\forall_{g \in G}$

<div class="proposition" markdown="1">

**Proposition:** 

A normal subgroup, $H \mathrel{\unlhd} G$, is the union of its conjugacy classes.

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

Take $h \in H$. As $H$ is normal
- $\for_{g \in G} ghg^{-1} \in H$

hence, $Cl_{G}(h) \subset H$. The other inclusion is immediate.

</div>
</details>
</div>

Let $H \leq G$, the centralizer of $H$ is the subgroup

\begin{eqnarray}
C_{G}(H) &:= \lbrace g \in G \; : \; ghg^{-1} = h \; \forall_{h \in H} \rbrace
\end{eqnarray}
{: style="text-align: center"}

Likewise, the centralizer of a group element $h \in G$ is the subgroup

\begin{eqnarray}
C_{G}(h) &:= \lbrace g \in G \; : \; ghg^{-1} = h \rbrace
\end{eqnarray}
{: style="text-align: center"}

Finally, we introduce the normalizer of $H \leq G$, which is the subgroup

\begin{eqnarray}
N_{G}(H) &:= \lbrace g \in G \; : \; gHg^{-1} = H \rbrace
\end{eqnarray}
{: style="text-align: center"}

<div class="proposition" markdown="1">

**Lemma:** 

$C_{G}(H) \mathrel{\unlhd} N_{G}(H)$

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

Let $x \in C_{G}(H)$ and $y \in N_{G}(H)$. We will show that $yxy^{-1} \in C_{G}(H)$.

Choose $h \in H$, then $y^{-1}hy \in H$ such that $x^{-1}(y^{-1}hy)x = y^{-1}hy$. \\
Hence,

{\Large
$$
\begin{align}
(yxy^{-1}) h (yxy^{-1})^{-1} & = yx (y^{-1} hy)x^{-1} y^{-1} \\
 & = yy^{-1} h y y^{-1} = h
\end{align}
$$
}%


i.e. $yxy^{-1} \in C_{G}(H)$

</div>
</details>
</div>

## $G$-Actions / $G$-Spaces <a name="S2"></a>

Throughout this section, we let $G$ denote a compact Lie group with identity $e \in G$.

<div class="definition" markdown="1">

**Definition:** $G$-Action

Let $X$ be a topological space, a continuous map $G \times X \rightarrow X$ defined by 
- $(g,x) \rightarrow gx$

is called a $G$-action if it satisfies the following conditions
1. $h(gx) = (hg)x, \; \forall_{h,g \in G} \forall{x \in X}$
2. $ex = x, \; \forall_{x \in X}$
</div>

If $X$ is, in addition, a Hausdorff space, then $X$ is said to be a **$G$-space**.

For a $G$-space $X$ and for any $g \in G$, define the map $T_g: X \rightarrow X$ by

\begin{eqnarray}
T_g(x) = gx
\end{eqnarray}
{: style="text-align: center"}

<div class="proposition" markdown="1">

**Lemma:** 

$T: G \rightarrow \text{Homeo}(X)$

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

Take $g \in G$, $T_g$ is a continuous map, by the continuity of the group action on $X$, with continuous inverse $(T_g)^{-1} = T_{g^{-1}}$. Indeed, by conditions $(1)$ and $(2)$ of the group action:

\begin{eqnarray}
T_g \circ T_{g^{-1}}(x) = T_{g g^{-1}}(x) = T_{e}(x) = x
\end{eqnarray}
{: style="text-align: center"}

</div>
</details>
</div>

Similarly, for any $x \in X$, we define the **continuous** map $J_x: G \rightarrow X$ by 

\begin{eqnarray}
J_x(g) = gx
\end{eqnarray}
{: style="text-align: center"}

### Some Notations, Definitions, Properties <a name="S2s1"></a>

In this section, we let $X$ denote a $G$-space.

<div class="definition" markdown="1">

**Definition:** Isotropy Group (Stabilizer)

We define the isotropy group of $x \in X$, $G_x$, as the set of elements in $G$ which fix $x$, i.e.

\begin{eqnarray}
G_x := \lbrace g \in G \; : \; gx = x \rbrace 
\end{eqnarray}
{: style="text-align: center"}
</div>

A $G$-action on $X$ is called free if

\begin{eqnarray}
\forall_{x \in X} G_x = \lbrace {e} \rbrace
\end{eqnarray}
{: style="text-align: center"}

it is called semi-free if

\begin{eqnarray}
\forall_{x \in X} G_x = \lbrace {e} \rbrace \lor G_x = G
\end{eqnarray}
{: style="text-align: center"}

And, it is called faithful if

\begin{eqnarray}
\forall_{g \in G} \exists_{x \in X} gx \neq x
\end{eqnarray}
{: style="text-align: center"}

<div class="proposition" markdown="1">

**Lemma:** 

A $G$-action on $X$ is faithful if and only if

\begin{eqnarray}
\bigcap_{x \in X} G_x = \lbrace e \rbrace
\end{eqnarray}
{: style="text-align: center"}
</div>

<div class="proposition" markdown="1">

**Lemma:** 

$G_x$ is a closed subgroup of $G$

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

That $G_x \mathrel{\unlhd} G$ is clear. We will prove that $G_x$ is, in addition, closed. Indeed, put

$$
{\Large
\begin{align}
G_x & := \lbrace g \in G \; : \; gx = x \rbrace \\
 & = \lbrace g \in G \; : \; J_x(g) = x \rbrace \\
 & = J_x^{-1}(x)
\end{align}
}%
$$

As the continuous pre-image of a closed set, $G_x$ is therefore closed.
</div>
</details>
</div>

For a given $x \in X$, we call the conjugacy class, $(G_x)$, the orbit type of $x$.

<div class="definition" markdown="1">

**Definition:** Orbit

The orbit of $x \in X$ is defined as

\begin{eqnarray}
G(x) := \lbrace gx  \; : \; g \in G \rbrace 
\end{eqnarray}
{: style="text-align: center"}
</div>

<div class="proposition" markdown="1">

**Lemma:** 

$G(x) \subset X$ is compact. 

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

Indeed, take $x \in X$, then the orbit can be equivalently defined as the range of the action-map $J_x: G \rightarrow X$

\begin{eqnarray}
G(x) = J_x(G)
\end{eqnarray}
{: style="text-align: center"}

Therefore, $G(x)$ is compact as the continuous image of a compact space.

</div>
</details>
</div>


<div class="proposition" markdown="1">

**Lemma:** 

The isotropy group of elements in the same orbit, $x,gx \in X$ are conjugate by the element $g \in G$, i.e.

\begin{eqnarray}
G_{gx} := g G_x g^{-1}
\end{eqnarray}
{: style="text-align: center"}

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

$$
{\Large
\begin{align}
G_{gx} & := \lbrace h \in G \; : \; h(gx) = gx \rbrace \\
 & = \lbrace h \in G \; : \; g^{-1}h(gx) = g^{-1}gx \rbrace \\
 & = \lbrace h \in G \; : \; g^{-1}hg \in G_x \rbrace \\
 & = \lbrace h \in G \; : \; h \in g G_x g^{-1} \rbrace \\
 & = g G_x g^{-1}
\end{align}
}%

$$

</div>
</details>
</div>

<div class="proposition" markdown="1">

**Lemma:** 

The set of orbits $\lbrace G(x) \; : \; x \in X \rbrace$ is a partition on $X$.
</div>

Let $A \subset X$, we will use the following notation for $g \in G$:

\begin{eqnarray}
gA := \lbrace gx \; : \; x \in A \rbrace = $T_g(A)$
\end{eqnarray}
{: style="text-align: center"}

and for $H \mathrel{\unlhd} G$ we put

\begin{eqnarray}
HA := \bigcup_{g \in H} gA
\end{eqnarray}
{: style="text-align: center"}

A set $A \subset X$ is called $G$-invariant if $$

\begin{eqnarray}
GA = A
\end{eqnarray}
{: style="text-align: center"}

and $A$ is said to be $H$-invariant for $H \leq G$ if

\begin{eqnarray}
HA = A
\end{eqnarray}
{: style="text-align: center"}

<div class="proposition" markdown="1">

**Proposition:** 

Let $S \subset X$ and $H \subset G$, then
1. If $S$ is open, so is $HS$
2. If $H$ is closed and $S$ compact, $HS$ is compact
3. If $S$, $H$ are both closed, so is $HS$
</div>

<hr>

We denote by, $\Phi(G)$, the set of all conjugacy classes of subgroups in $G$

\begin{eqnarray}
\Phi(G) = \lbrace (H) \; H \leq G \rbrace
\end{eqnarray}
{: style="text-align: center"}