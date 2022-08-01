---
layout: post
title: 'Brouwer Degree'
---

<div class="definition" markdown="1">

**Definition:** Admissiblity

Let $\Omega \subset \RR^n$ be an open bounded set and $f: \RR^n \rightarrow \RR^n$ a continuous map. The pair $(f, \Omega)$ is called admissible if 
> $\forall_{x \in \partial \Omega} f(x) \neq 0$

Equivalently, such an $f$ will be called $\Omega$-admissible
</div>

The theory of the Brouwer Degree is concerned with algebraically counting the solutions of the equation

\$$
\begin{eqnarray}
f(x) &= 0, \; x \in \Omega \end{equation} \tag{1} \label{1}
\end{eqnarray}
\$$
{: style="text-align: center"}

for admissible pairs $(f,\Omega)$. 


For a Euclidean space $\RR^n$ we denote by $\mathcal{M}(\RR^n)$ the set of all admissible pairs $(f, \Omega)$ in $\RR^n$ and, taking a union over all Euclidean spaces, we put 
> $\mathcal{M} := \bigcup_n \mathcal{M}(\RR^n)$ {: style="text-align: center"}

<div class="definition" markdown="1">

**Definition:** Local Brouwer Degree

The Local Brouwer degree is a function
> $deg: \mathcal{M} \rightarrow \mathbb{Z}$
satisfying the following three conditions
1. (Additivity): If $(f, \Omega) \in \mathcal{M}(\RR^n)$ with $(f^{-1}(0) \cap \Omega) \subset (\Omega_1 \cup \Omega_2) \subset \Omega$ for disjoint open subsets $\Omega_1, \Omega_2$ then
    - $deg(f, \Omega) = deg(f, \Omega_1) + deg(f, \Omega_2)$
2. (Homotopy): Given an $\Omega$-admissible homotopy, $h: [0,1] \times \RR^n \rightarrow \RR^n$, 
    - $deg(h_t, \Omega)$ is constant with respect to $t \in [0,1]$
3. (Normalization): Let $\Omega \subset \RR^n$ be open, bounded with $a \in \RR^n$, $a \notin \partial \Omega$ then
    - $deg(Id - a, \Omega) = \begin{cases} 0 & \text{if } a \notin \Omega \\ 1 & \text{if } a \in \Omega \end{cases}$
</div>

**Remark:** A homotopy, $h: [0,1] \times \RR^n \rightarrow \RR^n$, is said to be $\Omega$ admissible if $\forall_{x \in \partial \Omega,} \forall_{t \in [0,1]} h_t(x) \neq 0$, i.e. $h$ is an $\Omega$-admissible homotopy if $\forall_{t \in [0,1]} (h_t, \Omega) \in \mathcal{M}(\RR^n)$.

### Additional Properties of the Degree

<div class="proposition" markdown="1">

**Proposition:** Empty-set Lemma

$(f, \emptyset)$ is always an admissible pair for any $f: \RR^n \rightarrow \RR^n$ and
> $deg(f, \emptyset) = 0$


<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

Indeed, we have the following truisms 
1. $(f^{-1}(0) \cap \emptyset) \subset \emptyset \cup \emptyset$
2. $\emptyset \cup \emptyset = \emptyset$

So, by additivity of the degree

\begin{align}
deg(f, \emptyset) & = deg(f, \emptyset) + deg(f, \emptyset) \\
 & \rightarrow deg(f, \emptyset) = 0 \; \square
\end{align}

</details>
</div>

</div>

<div class="proposition" markdown="1">

**Proposition:** Existence Property

For $(f, \Omega) \in \mathcal{M}(\RR^n)$, if $deg(f, \Omega) \neq 0$ then $\exists_{x_0 \in \Omega}$ with $f(x_0) = 0$


<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

Consider the contrapositive of the proposition: 
> $\forall_{x \in \Omega} f(x) \neq 0 \; \implies \; deg(f, \Omega) = 0$

Suppose $f$ has no zeros in $\Omega$, i.e. suppose $f^{-1}(0) \cap \Omega = \emptyset$, and take $\Omega_1, \Omega_2 = \emptyset$ then
1. $f^{-1}(0) \cap \Omega \subset \Omega_1 \cup \Omega_2$
2. $\Omega_1 \cap \Omega_2 = \emptyset$

So, by additivity of the degree

\begin{align}
deg(f, \Omega) & = deg(f, \Omega_1) + deg(f, \Omega_2) \\
 & = deg(f, \emptyset) + deg(f, \emptyset) = 0 \; \square
\end{align}

</details>
</div>

</div>

<div class="proposition" markdown="1">

**Proposition:** Excision Property

For $(f, \Omega) \in \mathcal{M}(\RR^n)$, if $(f^{(-1)}(0) \cap \Omega) \subset \Omega_1$, for $\Omega_1 \subset \Omega$ open then
> $deg(f, \Omega) = \deg(f, \Omega_1)$

<div class="proof" markdown="1">

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

Again, using additivity of the degree with $\Omega_2 = \empty$

\begin{align}
deg(f, \Omega) & = deg(f, \Omega_1) + deg(f, \emptyset) \\
 & = deg(f, \Omega_1) \; \square
\end{align}

</details>
</div>

</div>

**Remark:** If $\Omega \subset \Omega_0$ are two open, bounded sets with $\forall_{x \in \overline{\Omega} \setminus \Omega_0} f(x) \neq 0$ then
> $deg(f, \Omega) = \deg(f, \Omega_0)$

<div class="proposition" markdown="1">

**Proposition:** Rouche Property

Let $(f, \Omega) \in \mathcal{M}(\RR^n)$, and suppose $g: \RR^n \rightarrow \RR^n$ is a continuous function such that
> $\sup_{x \in \partial \Omega} \vert g(x) - f(x) \vert < \inf_{x \in \partial \Omega} \vert f(x) \vert$

then, 
> $deg(f, \Omega) = deg(g, \Omega)$

<div class="proof" markdown="1">

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

Recall, two maps connected by an $\Omega$-admissible homotopy share the same degree over $\Omega$.

Consider the linear homotopy $h_t : [0,1] \times \RR^n \rightarrow \RR^n$ defined by $h(t,x) = (1-t)f(x) + tg(x)$. We claim that $h_t$ is $\Omega$-admissible. 

Indeed, take $t \in [0,1]$ and $x \in \partial \Omega$ then

\begin{align}
\vert h(t,x) \vert & = \vert (1-t)f(x) + tg(x) \vert \\
 & = \vert f(x) - t(f(x) - g(x)) \vert \\
 & \geq \vert f(x) \vert - t \vert f(x) - g(x) \vert \\
 & \geq \vert f(x) \vert - \vert f(x) - g(x) \vert \\
 & \geq \inf_{x \in \partial \Omega} \vert f(x) \vert - \sup_{x \in \partial \Omega} \vert g(x) - f(x) \vert > 0 \; \square
\end{align}

</details>
</div>

</div>

<div class="proposition" markdown="1">

**Proposition:** Boundary Property

Let $(f, \Omega) \in \mathcal{M}(\RR^n)$ and suppose $g: \RR^n \rightarrow \RR^n$ is a continuous function such that
$\forall_{x \in \partial \Omega} \; f(x) = g(x)$ then $(g,\Omega)\in \mathcal{M}(\RR^n)$ and
> $deg(f, \Omega) = deg(g, \Omega)$

<div class="proof" markdown="1">

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

This is an immediate consequence of the Rouche property.

</details>
</div>

</div>

### Degree of Linear Isomorphisms

The general linear group, $GL(n,\RR):= \lbrace A: \RR^n \rightarrow \RR^n \; : \; A \text{is a linear isomorphism} \rbrace$, has two connected components

\begin{align}
GL(n, \RR) &= GL^{+}(n, \RR) \cup GL^{-}(n, \RR) \\
GL^{+}(n, \RR) &= \lbrace A \in GL(n, \RR) \; : \; det(A)>0 \rbrace  \\
GL^{-}(n, \RR) &= \lbrace A \in GL(n, \RR) \; : \; det(A)<0 \rbrace
\end{align}

<div class="proposition" markdown="1">

**Proposition:** Lemma 

$GL^{\pm}(n, \RR)$ are each open and connected in $L(n, \RR)$, the space of linear maps $\RR^n \rightarrow \RR^n$.

<div class="proof" markdown="1">

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

...

</details>
</div>

</div>