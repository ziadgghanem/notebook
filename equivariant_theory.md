---
layout: post
title: 'Equivariant Algebra'
---

## Conjugacy

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

A subgroup H is said to be normal in $G$, denoted $H \nrml G$, if and only if $\forall_{g \in G} gHg^{-1} = H$
</div>

In the context of the conjugacy relation we propose the following lemma.

<div class="proposition" markdown="1">

**Lemma:** 

$H \nrml G$ if and only if $H \sim K \implies K = G$
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

A normal subgroup, $H \nrml G$, is the union of its conjugacy classes.

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

$C_{G}(H) \nrml N_{G}(H)$

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

Let $x \in C_{G}(H)$ and $y \in N_{G}(H)$. We will show that $yxy^{-1} \in C_{G}(H)$.

Choose $h \in H$, then $y^{-1}hy \in H$ such that $x^{-1}(y^{-1}hy)x = y^{-1}hy$. Hence,
 
$$
\begin{align}
(yxy^{-1}) h (yxy^{-1})^{-1} & = yx (y^{-1} hy)x^{-1} y^{-1} \\
 & = yy^{-1} h y y^{-1} = h
\end{align}
$$

i.e. $yxy^{-1} \in C_{G}(H)$

</div>
</details>
</div>

</div>