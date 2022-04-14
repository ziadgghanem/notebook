---
layout: post
title: 'Complex Analysis'
---
### Complex Polynomials
A complex polynomial has the form:
- $$P(z)$$ $$= a_n z^n + \cdots + a_0 = \sum_{k=0}^{n} a_k z^k$$
- where $$a_k$$ are complex numbers, not identically zero and z is a complex variable.

**Terminology** \\
Let $$P(z) = a_n z^n + \cdots + a_0$$ be a complex polynomial.
1. If $$a_n \neq 0,$$ $$P$$ is said to be of *degree* $$n$$.
2. The *roots* of $$P$$ are points on the complex plane $$\lambda \in \mathbb{C}$$ where $$P(\lambda) = 0.$$

**Ring of Polynomials** \\
Recall: A *ring* is an commutative group equipped with a second operation, multiplication, that is associative, distributes over addition.
- An *integral domain* is a nonzero commutative ring with multiplicative identity, $$\mathbb{1}$$, in which the product of any two nonzero elements is nonzerro
- A *unique factorization domain* is a commutative ring in which every nonzero element can be exprressed as the product of prime elements, uniquely and up to the order of the units.

**Properties (Degree of a Polynomial)** \\
Let $$P,Q$$ be complex polynomials.
1. $$deg(P+Q)$$ $$\leq max \{ deg(P),deg(Q) \}$$
2. $$deg(cP)$$ $$= deg(P), \quad c \in \mathbb{C}$$
3. $$deg(P \cdot Q)$$ $$= deg(P) + deg(Q)$$ where $$\cdot$$ denotes elementwise multiplication of maps. 
4. $$deg(P \circ Q)$$ $$= deg(P) + deg(Q)$$ where $$\circ$$ denotes the composition of maps. 

**Theorem (Euclidean Theorem)** \\
Given complex polynomials $$P,Q \neq 0$$ there exists a unique pair of polynomials $$R,S$$ such that
- $$P = R \cdot Q + S$$ with $$deg(S) < deg(Q)$$

**Theorem (Bezout Lemma)** \\
Let $$z_0$$ be a root of the complex polynomial $$P,$$ then $$(z-z_0)$$ divides $$P.$$

***Proof***
- Take $$P = R \cdot Q + S$$ with $$Q = z-z_0.$$ such that $$deg(Q) = 1$$ 
- Then by $$deg(S) < deg(Q),$$ it must be the case that $$deg(S) = 0$$ i.e. $$S$$ is a constant polynomial.
- As $$z_0$$ is a root of both $$P$$ and $$z-z_0$$ we have:
- $$P(z_0) = R(z_0)(z_0 - z_0) + S$$ $$\rightarrow S = 0$$
- Hence $$P = R \cdot (z-z_0)$$

**Example** \\
Prove that all roots of $$P(z) = z^3 + 3z + 5$$ have modulus strictly bigger than one. \\
***Solution*** \\
Suppose not, assume that $$P(z)$$ has root $$z_0$$ with $$\vert z_0 \vert < 1$$
- Then $$P(z_0) = z_{0}^3 + 3z_0 + 5 = 0 \rightarrow 5 = -z_{0}^3 - 3z_0$$
- Taking modulus of both sides and applying reverse triangle inequality, $$5 = \vert -z_{0}^3 - 3z_0 \vert \leq \vert -z_{0}^3 \vert + \vert 3z_0 \vert \leq 1 + 3 = 4$$ contradiction.

**Definition** \\
For polynomial $$P(z) = a_0 + a_1 z + \cdots + a_n z^n$$ we define the linear operator
- $$ D[P(z)] =$$ $$P'(z) = a_1 + 2a_2 z + \cdots + n a_n z^{n-1}$$

**Theorem (Gauss-Lucas)** \\
Let $$P$$ be any complex polynomial, the roots of its derivative $$P'$$ must lie within the convex hull of the roots of $$P$$.

**Example** \\
Show that if all the zeros of polynomial $$P(z)$$ have positive real parts, then so do the zeross of its derivative.
 ***Solution*** \\
Let $$P(z)$$ be a polynomial of degree $$n$$ with zeros at $$z_k, k = 1:n$$ such that $$Re(z_k) > 0, \forall k$$
- We express our polynomial as $$P(z) = a(z-z_1)(z-z_2) \cdots (z-z_n)$$ and employ logarithmic differentiation:
- Take the natural logarithm of both sides of our expression: $$ln(P(z)) = ln(a(z-z_1)(z-z_2) \cdots (z-z_n))$$ $$ = ln(a) + ln(z-z_1) + \cdots ln(z-z_n)$$ 
- Take the derivative: $$\frac{P'(z)}{P(z)} = \frac{1}{z-z_1} + \cdots  \frac{1}{z-z_n}$$
- Consider $$z \in \mathbb{C}$$ with $$Re(z) \leq 0 $$ then as $$Re(z_k) > 0$$ we have $$Re(z-z_k) < 0 \rightarrow Re(\frac{1}{z-z_k}
), \forall k$$
- Hence, for any $$z \in \mathbb{C}$$ with $$Re(z) \leq 0 $$ we have $$Re(\frac{P'(z)}{P(z)}) < 0$$ in particular $$P'(z) \neq 0$$

 




<hr>

### Complex Power Series

A complex power series centered at a point $$z_0$$ has the form

$$ \sum_{n=0}^{\infty} a_n (z-z_0)^n \label{1}$$

where the coefficients $$a_n$$ are complex constants.

Every complex power series has radius of convergence $$R \ge 0$$ which specifies the largest circle centered at $$z_0,$$ $$\vert z - z_0 \vert = R$$ such that the series converges absolutely everywhere within the circle and diverges at every point outside the circle.

There are three cases of to consider
1. $$R=0,$$ in which case $$(1)$$ converges only at its center $$z=z_0$$
2. $$0 < R < \infty ,$$ in which case $$(1)$$ converges for all interior points $$\vert z - z_0 \vert < R$$ and diverges at every point $$\vert z - z_0 \vert > R$$
3. $$R= \infty ,$$ in which case $$(1)$$ converges for all $$z \in \mathbb{C}$$

**The Cauchy Hadamard Formula (1888)** \\
The radius of convergence $$R$$ of the complex power series $$\sum_{n=0}^{\infty} a_n (z-z_0)^n$$ is
- $$ R := \frac{1}{\varlimsup_{n \rightarrow \infty} \vert a_n \vert^{\frac{1}{n}}}$$
- $$ R = 
\begin{cases}
\varlimsup_{n \rightarrow \infty} \Vert a_n \Vert^{\frac{1}{n}} = 0 \\
\varlimsup_{n \rightarrow \infty} \Vert a_n \Vert^{\frac{1}{n}} = \infty
\end{cases}
$$

Where $$\varlimsup_{n \rightarrow \infty} a_n$$ denotes the limit superior of the sequence $$a_n$$ as $$n \rightarrow \infty.$$ 

***Example:*** Find the radius of converrgence of the power series $$ \sum_{n=0}^{\infty} (1+i)^n (z)^n$$ \\
*Solution:* \\
We have $$a_n = (1+i)^n$$ with modulus $$\vert a_n \vert = \vert (1+i)^n \vert = \vert 1+i \vert^n = \vert \sqrt{2} \vert^n = 2^{\frac{n}{2}}$$ applying the formula:
- $$R =  \lim_{n\to \infty} \frac{1}{\sqrt[n]{2^{\frac{n}{2}}}} = \frac{1}{\sqrt{2}}$$





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