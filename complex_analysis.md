---
layout: post
title: 'Complex Analysis'
---

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