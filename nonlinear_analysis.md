---
layout: post
title: 'The Brouwer Degree'
---

<div class="definition" markdown="1">

**Definition:** Admissiblity

Let $\Omega \subset \RR^n$ be an open bounded set and $f: \RR^n \rightarrow \RR^n$ a continuous map. The pair $(f, \Omega)$ is called admissible if 
> $\forall_{x \in \partial \Omega} f(x) \neq 0$

Equivalently, such an $f$ will be called $\Omega$-admissible
</div>

The theory of the Brouwer Degree is concerned with algebraically counting the solutions of the equation

\begin{eqnarray}
f(x) &= 0, \; x \in \Omega
\end{eqnarray}
{: style="text-align: center"}

for admissible pairs $(f,\Omega)$. 


For a Euclidean space $\RR^n$ we denote by $\mathcal{M}(\RR^n)$ the set of all admissible pairs $(f, \Omega)$ in $\RR^n$ and, taking a union over all Euclidean spaces, we put 

\begin{eqnarray}
\mathcal{M} := \bigcup_n \mathcal{M}(\RR^n)
\end{eqnarray}
{: style="text-align: center"}

\begin{cases} 
0 & \text{if } a \notin \Omega \\ 1 & \text{if } a \in \Omega 
\end{cases}
{: style="text-align: center"}

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
    - $$deg(Id - a, \Omega) = \begin{cases} 0 & \text{if } a \notin \Omega \\ 1 & \text{if } a \in \Omega \end{cases}$$
</div>

**Remark:** A homotopy, $h: [0,1] \times \RR^n \rightarrow \RR^n$, is said to be $\Omega$-admissible if $\forall_{x \in \partial \Omega,} \forall_{t \in [0,1]} h_t(x) \neq 0$. <br/> 
i.e. $h$ is an $\Omega$-admissible homotopy if $\forall_{t \in [0,1]} (h_t, \Omega) \in \mathcal{M}(\RR^n)$.

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

</div>
</details>

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

</div>
</details>

</div>

<div class="proposition" markdown="1">

**Proposition:** Excision Property

For $(f, \Omega) \in \mathcal{M}(\RR^n)$, if $(f^{(-1)}(0) \cap \Omega) \subset \Omega_1$, for $\Omega_1 \subset \Omega$ open then
> $deg(f, \Omega) = \deg(f, \Omega_1)$


<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

Again, using additivity of the degree with $\Omega_2 = \empty$

\begin{align}
deg(f, \Omega) & = deg(f, \Omega_1) + deg(f, \emptyset) \\
 & = deg(f, \Omega_1) \; \square
\end{align}

</div>
</details>

</div>

**Remark:** If $\Omega \subset \Omega_0$ are two open, bounded sets with $\forall_{x \in \overline{\Omega} \setminus \Omega_0} f(x) \neq 0$ then
> $deg(f, \Omega) = \deg(f, \Omega_0)$

<div class="proposition" markdown="1">

**Proposition:** Rouche Property

Let $(f, \Omega) \in \mathcal{M}(\RR^n)$, and suppose $g: \RR^n \rightarrow \RR^n$ is a continuous function such that
> $\sup_{x \in \partial \Omega} \vert g(x) - f(x) \vert < \inf_{x \in \partial \Omega} \vert f(x) \vert$

then, 
> $deg(f, \Omega) = deg(g, \Omega)$


<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

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

</div>
</details>

</div>

<div class="proposition" markdown="1">

**Proposition:** Boundary Property

Let $(f, \Omega) \in \mathcal{M}(\RR^n)$ and suppose $g: \RR^n \rightarrow \RR^n$ is a continuous function such that
$\forall_{x \in \partial \Omega} \; f(x) = g(x)$ then $(g,\Omega)\in \mathcal{M}(\RR^n)$ and
> $deg(f, \Omega) = deg(g, \Omega)$


<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

This is an immediate consequence of the Rouche property.

</div>
</details>

</div>

### Degree of Linear Isomorphisms

The general linear group, $GL(n,\RR):= \lbrace A: \RR^n \rightarrow \RR^n \; : \; A \text{is a linear isomorphism} \rbrace$, has two connected components

\begin{align}
GL(n, \RR) &= GL^{+}(n, \RR) \cup GL^{-}(n, \RR) \\
GL^{+}(n, \RR) &= \lbrace A \in GL(n, \RR) \; : \; det(A)>0 \rbrace  \\
GL^{-}(n, \RR) &= \lbrace A \in GL(n, \RR) \; : \; det(A)<0 \rbrace
\end{align}

<div class="proposition" markdown="1">

**Lemma:**  

$GL^{\pm}(n, \RR)$ are each open and connected in $L(n, \RR)$, the space of linear maps $\RR^n \rightarrow \RR^n$.


<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

...

</div>
</details>

</div>

<div class="proposition" markdown="1">

**Propostion:** Degree of Linear Isomorphism

For $A \in GL^{+}(n, \RR)$ and $\Omega \subset \RR^n$ open, bounded 

\begin{equation*}
deg(A,\Omega) = \begin{cases}
1 &\text{if } 0 \in \Omega\\
0 &\text{if } 0 \notin \Omega
\end{cases}
\end{equation*}

For $A \in GL^{-}(n, \RR)$ and $\Omega \subset \RR^n$ open, bounded 

\begin{equation*}
deg(A,\Omega) = \begin{cases}
-1 &\text{if } 0 \in \Omega\\
0 &\text{if } 0 \notin \Omega
\end{cases}
\end{equation*}


<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

...

</div>
</details>

</div>

## Some Fundamental Facts from Analysis

<div class="proposition" markdown="1">

**Theorem:**  Weierstrass

Let $K \subset \RR^n$ be a compact set and $f : \RR^n \rightarrow \RR^n$ a continuous map, then
- $\forall_{\epsilon>0} \exists_{f_0 : \RR^n \rightarrow \RR^n}$ such that $f_0 \in C^{\infty}$ and $\sup_{x \in K} \vert f(x) - f_0(x) \vert < \epsilon$
</div>

<div class="definition" markdown="1">

**Definition:**  Support

The support of a function $f : \RR^n \rightarrow \RR$ is defined
- $supp f := \lbrace x \in \RR^n \; : \; f(x) \neq 0 \rbrace$
</div>

<div class="proposition" markdown="1">

**Theorem:**  Tietze-Dugunji Extension

Let $(X,d)$ be a metric space, $A \subset X$ a closed subset, $\EE$ a normed space and $f: A \rightarrow \EE$ a continuous map. Then there exists a continuous map $\tilde{f}: X \rightarrow \EE$ such that 
1. $f(x) = \tilde{f}$ for all $x \in A$
2. $\tilde(f)(X) \subset \overline{conv(f(A))}$
</div>

**Remark:** The notion of an admissible pair $(f, \Omega)$ can be extended to include maps $f: \overline{\Omega} \rightarrow \RR^n$ with $\forall_{x \in \partial \Omega} f(x) \neq 0$. Furthermore, if $\tilde{f}$ is a continuous extension of $f$ then
- $deg(f, \Omega) = deg(\tilde{f}, \Omega)$

<div class="definition" markdown="1">

**Definition:**  Regular/Critical points and values

Let $f : \RR^n \rightarrow \RR^n$ be a $C^{\infty}$ map, and $K \subset \RR^n$ a compact set
- We say that $x_0 \in \RR^n$ is a regular point of $f$ if and only if $Df(x_0): \RR^n \rightarrow \RR^n$ is an isomorphism. 
    - Otherwise, $x_0$ is said to be critical.
- We say that $y_0 \in \RR^n$ is a critical value of $f_{\vert_K}$ if there exists a critical point $x_0 \in K$ such that $f(x_0) = y_0$
    - Otherwise, $y_0$ is said to be regular.
</div>

<div class="proposition" markdown="1">

**Theorem:**  Inverse Function Theorem

For $f : \RR^n \rightarrow \RR^m$ a $C^{\infty}$ map, if $x_0 \in \RR^n$ is a regular value of $f$, then $f$ is injective in a neighborhood of $f$


**Theorem:**  Lemma

For $f : \RR^n \rightarrow \RR^m$ a $C^{\infty}$ map, $x_0 \in \RR^n$ is a regular point of $f$ if and only if $Df(x_0) : \RR^n \rightarrow \RR^m$ is surjective, otherwise it is called critical. 
</div>

<div class="proposition" markdown="1">

**Theorem:**  Sard's Lemma

Let $K \subset \RR^n$ be a compact set, and $f : \RR^n \rightarrow \RR^m$ a $C^{\infty}$ map. Then, the set of all regular values of $f_{\vert_K}$ is open and dense in $\RR^m$

</div>