---
layout: post
title: 'Complex Analysis'
---
### Complex Power Series

A complex power series centered at a point $$z_0$$ has the form

$$ \sum_{n=0}^{\infty} a_n (z-z_0)^n \label{1}$$

where the coefficients $$a_n$$ are complex constants.

Every complex power series has radius of convergence $$R \ge 0$$ which specifies the largest circle centered at $$z_0,$$ $$\Vert z - z_0 \Vert = R$$ such that the series converges absolutely everywhere within the circle and diverges at every point outside the circle.

There are three cases of to consider
1. $$R=0,$$ in which case $$(1)$$ converges only at its center $$z=z_0$$
2. $$0 < R < \infty ,$$ in which case $$(1)$$ converges for all interior points $$\Vert z - z_0 \Vert < R$$ and diverges at every point $$\Vert z - z_0 \Vert > R$$
3. $$R= \infty ,$$ in which case $$(1)$$ converges for all $$z \in \mathbb{C}$$

**The Cauchy Hadamard Formula (1888)** \\
The radius of convergence $$R$$ of the complex power series $$(1)$$ is

$$ R := \frac{1}{\varlimsup_{n \rightarrow \infty} \Vert a_n \Vert^{\frac{1}{n}}}$$

- $$ \varlimsup_{n \rightarrow \infty} \Vert a_n \Vert^{\frac{1}{n}} = 0 \iff R = \infty$$
- $$ \varlimsup_{n \rightarrow \infty} \Vert a_n \Vert^{\frac{1}{n}} = \infty \iff R = 0$$

where $$\varlimsup_{n \rightarrow \infty} a_n$$ denotes the limit superior of the sequence $$a_n$$ as $$n \rightarrow \infty.$$ \\

***Example:*** Find the radius of converrgence of the power series $$ \sum_{n=0}^{\infty} (1+i)^n (z)^n$$ \\
We have coefficient $$a_n = (1+i)^n$$ \\
with modulus $$\Vert a_n \Vert = \Vert (1+i)^n \Vert = \Vert 1+i \Vert^n = \Vert \sqrt{2} \Vert^n = 2^{\frac{n}{2}}$$ \\
applying CHF $$R =  \lim_{n\to \infty} \frac{1}{\sqrt[n]{2^{\frac{n}{2}}}} = \frac{1}{\sqrt{2}}$$





<hr>

### Complex Integration

Consider the complex-valued function $$f(t) = u(t) + iv(t),$$ defined and piecewise-continous over the real interval $$(a,b).$$ We define the integral of $$f$$ over $$(a,b)$$ to be

$$
\LARGE
\int_{a}^b f(t)dt = \int_{a}^b u(t)dt + i \int_{a}^b v(t)dt
\label{1.0.1} \tag{}
$$

<hr>
$$\mathbf{Example}:$$ Calculate the integral $$\int_{0}^{\frac{\pi}{2}} e^{it}dt. \\$$

$$\mathit{Solution}$$: Using Euler's formula, $$e^{it} = cost + isint. \\$$

$$
\int_{0}^{\frac{\pi}{2}} e^{it}dt = \int_{0}^{\frac{\pi}{2}} costdt + i \int_{0}^{\frac{\pi}{2}} sint = sint\Big|_{0}^{\frac{\pi}{2}} - i cost\Big|_{0}^{\frac{\pi}{2}} = 1 + i.
$$
<hr>

A complex integral, also called a contour integral, is evaluated over a path in the complex plane.
Let $$\gamma: [a,b] \rightarrow \mathbb{C}$$ be a piecewise differentiable curve and $$f(z) = u(x,y) + iv(x,y)$$ a 
function of complex variable continous on the path $$\gamma([a,b]).$$ Then $$f(z(t))$$ is continous and we define 
the contour integral of $$f$$ over $$\gamma$$ as:

$$
\LARGE
\int_{\gamma} f(z)dz = \int_{a}^b f(z(t))z'(t)dt = \int_{\gamma} udx - vdy + i\int_{\gamma} vdx + udy.
\label{1.0.2} \tag{}
$$

The Estimation Lemma: Suppose $$\vert f(z) \vert \leq M$$ for all $$z$$ on some curve $$\gamma$$ with length $$\vert \gamma \vert$$

$$
\vert \int_{\gamma} f(z)dz \vert \leq M \vert \gamma \vert
$$