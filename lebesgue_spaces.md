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

**Corollary:** 

Assume $\phi(x) = e^x$ then for $\mu(\Omega) = 1$ and $f: \Omega \rightarrow (a,b)$ Lebesgue integrable Jensen's inequality reads
- $e^{\int\limits_{\Omega} f d \mu} =  \int\limits_{\Omega} e^{f} d \mu$
</div>

<div class="proposition" markdown="1">

**Corollary:** 

Let $\Omega = \lbrace p_1, \ldots, p_n \rbrace$ with $\mu(p_i) = \frac{1}{n}$ and $f: \Omega \rightarrow (a,b)$ such that $f(p_i) = x_i$ then it follows from Jensen's inequality that
- $\phi( \int\limits_{\Omega} f d \mu) = \phi(x_1 \frac{1}{n} + \cdots + x_n \frac{1}{n}) = \phi(\frac{1}{n}(x_1 + \cdots + x_n))$
- $ \leq \int\limits_{\Omega} (\phi \circ f) d \mu = \frac{1}{n} \phi(x_1) + \cdots + \frac{1}{n} \phi(x_n)$
</div>