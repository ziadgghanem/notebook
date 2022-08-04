---
previewWebRootPath: \coursebook
layout: post
title: 'Lebesgue Spaces'
---

## Jensen's Inequality and Convexity

In calculus we learn various equivalent definitions of convexity

Let $f:(a,b) \rightarrow \mathbb{R}$ be twice differentiable on $(a,b)$ then $f$ is said to be convex on this interval if its second derivative is nonegative, i.e. if $\forall_{x \in (a,b)}$
- $f''(x) \geq 0$ 

Assume that $f$ is atleast once differentiable on $(a,b)$ then $f$ is convex if its first derivative increases monotonically, i.e. if $\forall_{u,v \in (a,b)}$ 
- $u \leq v \; \implies \; f'(u) \leq f'(v)$

The definition of convexity we will use does not require any assumption of differentiability, however if $f$ is differentiable it will coincide with the above notions

For our purposes, a function $f:(a,b) \rightarrow \mathbb{R}$ is said to be convex if $\forall_{s,t,p \in (a,b)$
- $s < t < p \; \implies \; \frac{f(t) - f(s)}{t-s} \leq \frac{f(p) - f(t)}{p-t}$ 

<div class="proposition" markdown="1">

**Lemma:** First Jensen's Inequality 

A function $f:(a,b) \rightarrow \mathbb{R}$ is convex if and only if $\forall_{x,y \in (a,b)}$ and $\forall_{\lambda \in [0,1]}$
- $x \leq y \; \implies \; f(\lambda x + (1- \lambda) y) \leq \lambda f(x) + (1-\lambda)f(y)$ 
</div>

<div class="proposition" markdown="1">

**Proposition:** Continuity of convex functions

Let $f:(a,b) \rightarrow \mathbb{R}$ be convex, then it is continuous.


<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

Without loss of generality, assume $x \leq y$ such that $x,y \in [c,d] \subset (a,b)$, choose any $z \in [c,d]$ with $y \leq z$ then $(y - x) \leq (z - x) $, now put $\lambda = \frac{y - x}{z - x}$, clearly $0 \leq \lambda \leq 1$. Now, $(z - x) \lambda = y - x$ such that $y = \lambda z + (1- \lambda)x$ so by convexity of $f$
- $f(y) \leq \lambda f(z) + (1- \lambda)f(x) = f(x) + \lambda (f(z) - f(x)$


Finally note, a convex function is bounded on any closed set so let $\max_{x \in [c,d]} f(x) = M$ and $\min_{x \in [c,d]} f(x) = m$. 
</div>
</details>
</div>

**Question:** What if we replace the open interval $(a,b)$ with its closure? 
- A convex function, $f:[a,b] \rightarrow \mathbb{R}$, need not be continuous, indeed consider $\phi: [0,1] \rightarrow \mathbb{R}$

$$\phi(x) = \begin{cases} 0, \quad 0 \leq x < 1 \\ 1, \quad x = 1 \end{cases}$$

<div class="proposition" markdown="1">

**Lemma:** General Jensen's Inequality 

Assume $\Omega$ is a measure space with $\mu(\Omega) = 1$, $f: \Omega \rightarrow (a,b)$ Lebesgue integrable and $\phi: (a,b) \rightarrow \mathbb{R}$ convex then
- $\phi( \int\limits_{\Omega} f d \mu) \leq \int\limits_{\Omega} (\phi \circ f) d \mu$ 

</div>


<div class="proposition" markdown="1">

**Corollary 1:** 

Assume $\phi(x) = e^x$ then for $\mu(\Omega) = 1$ and $f: \Omega \rightarrow (a,b)$ Lebesgue integrable Jensen's inequality reads
- $e^{\int\limits_{\Omega} f d \mu} =  \int\limits_{\Omega} e^{f} d \mu$
</div>

<div class="proposition" markdown="1">

**Corollary 2:** 

Let $\Omega = \lbrace p_1, \ldots, p_n \rbrace$ with $\mu(p_i) = \frac{1}{n}$ and $f: \Omega \rightarrow (a,b)$ such that $f(p_i) = x_i$ then
- $e^{\frac{1}{n}(x_1 + \cdots + x_n)} \leq \frac{1}{n}(e(x_1) + \cdots + e(x_n))$


<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">

It follows from Jensen's inequality that,

\begin{align}
e( \int\limits_{\Omega} f d \mu) & = e(x_1 \frac{1}{n} + \cdots + x_n \frac{1}{n}) \\
 & = e(\frac{1}{n}(x_1 + \cdots + x_n)) \\
 & \leq \int\limits_{\Omega} (e \circ f) d \mu = \frac{1}{n} e(x_1) + \cdots + \frac{1}{n} e(x_n) \; \square
\end{align}
 
</div>
</details>
</div>


<div class="proposition" markdown="1">

**Corollary 3:** 

Again, let $\Omega = \lbrace p_1, \ldots, p_n \rbrace$ with $\mu(p_i) = \frac{1}{n}$ and $f: \Omega \rightarrow (a,b)$ such that $f(p_i) = x_i$, and put $y_i : = e^{x_i}$ then 
- $\sqrt[n]{y_1 \cdots y_n} \leq \frac{y_1 + \cdots + y_n}{n}$

Which is the classical inequality between geometric and arithmetic means.

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">
 
</div>
</details>
</div>

<div class="proposition" markdown="1">

**Corollary 4:** 

Assume $\Omega$ and $f: \Omega \rightarrow (a,b)$ are as in Cor. 2 and 3. Define a measure $\mu$ on $\Omega$ such that $\mu(p_i) = \alpha_i \geq 0$ such that $\sum_{i=1}^n \alpha_i = 1$, then
- $e^{\alpha_1 x_1 + \cdots + \alpha_n x_n} \leq \alpha_1 e^{x_1} + \cdots + \alpha_n e^{x_n}$

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">
 
</div>
</details>
</div>

<div class="definition" markdown="1">

**Definition:** Conjugacy

Given two real numbers, $p,q > 1$, we say that they are conjugate if $\frac{1}{p} + \frac{1}{q} = 1$ or equivalently if $pq = p+q$

</div>

**Remark:** Some immediate properties of conjugate numbers
1. For every $p \in [1, \infty]$ there exists a unique $q \in [1, \infty]$ conjugate to $p$. 
2. $2$ is the only number conjugate to itself.
3. If $p,q$ are conjugate and $p \rightarrow 1$ then $q \rightarrow \infty$

<div class="proposition" markdown="1">

**Theorem:** Holder's Inequality 

Let $(X, \Sigma_X, \mu)$ be a measaure space and $f,g: \rightarrow [0, \infty]$ two integrable functions. For any two conjugates $p,q$ the following inquality holds
- $\int\limits_X fg d \mu \leq (\int\limits_X f^p d \mu)^{\frac{1}{p}} (\int\limits_X g^q d \mu)^{\frac{1}{p}}$

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">
 
</div>
</details>
</div>


<div class="proposition" markdown="1">

**Theorem:** Minkowski's Inequality 

Let $(X, \Sigma_X, \mu)$ be a measaure space and $f,g: \rightarrow [0, \infty]$ two integrable functions. For any $p > 1$ the following inquality holds
- $(\int\limits_X (f + g)^p d \mu)^{\frac{1}{p}} \leq (\int\limits_X f^p d \mu)^{\frac{1}{p}} + (\int\limits_X g^p d \mu)^{\frac{1}{p}}$

<details>
<summary><i style="font-size:150%;">Proof</i></summary>

<div class="proof" markdown="1">
 
</div>
</details>
</div>


<div class="definition" markdown="1">

**Definition:** p-Norm

Given a measure space $(X, \Sigma_X, \mu)$ and a measurable function $f: X \rightarrow \RR$, we define the $p$-norm of $f$ as
- \Vert f \Vert_p := (\int\limits_X f^p d \mu)^{\frac{1}{p}}
</div>

<div class="definition" markdown="1">

**Definition:** Essentially Bounded

A measurable function $f: X \rightarrow \RR$ is called essentially bounded if $\exists_{M >0}$ such that $\vert f(x) \vert \leq M$ for almost all $x \in X$.
</div>


<div class="definition" markdown="1">

**Definition:** Essential Supremum

The essential supremum of a measurable function $f: X \rightarrow \RR$ is defined with respect to the collection $\mathcal{Z} : = \lbrace Z \subset X \; : \: \mu(Z) = 0 \rbrace$
- $ess sup(f):= \inf_{Z \in \mathcal{Z}} \sup_{x \in X \setminus Z} \vert f(x) \vert$
</div>

**Remark:** $\Vert f \Vert_{\infty} := ess sup(f)$ defines a norm up to the property
- $\Vert f \Vert_{\infty} = 0 \implies f \equiv 0$