---
layout: post
title: 'Complex Analysis'
---

### Complex Integration

Consider the complex-valued function $$f(t) = u(t) + iv(t),$$ defined and piecewise-continous over the real interval $$(a,b).$$ We define the integral of $$f$$ over $$(a,b)$$ to be

$$
\LARGE
\int_{a}^b f(t)dt = \int_{a}^b u(t)dt + i \int_{a}^b v(t)dt
\label{1.0.1}
$$


$$\mathbf{Example}:$$ Calculate the integral $$\int_{0}^{\frac{\pi}{2}} e^{it}dt \\$$
$$\mathit{Solution}: Using Euler's formula, e^{it} = cost + isint. \\$$
$$
\int_{0}^{\frac{\pi}{2}} e^{it}dt = \int_{0}^{\frac{\pi}{2}} costdt + i \int_{0}^{\frac{\pi}{2}} sint = sint\Big|_{0}^{\frac{\pi}{2}} - i cost\Big|_{0}^{\frac{\pi}{2}} = 1 + i.
$$
