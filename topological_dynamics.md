---
layout: post
title: 'Topological Dynamics'
---

<blockquote>
        I have had my results for a long time: but I do not yet know how I am to arrive at them.
        <footer>Gauss</footer>
</blockquote>

1. [Introduction](#S1)
    1. [Linear Dynamical Systems](#S1s1)
2. [Appendix](#SA)


## Introduction <a name="S1"></a>

We consider the dynamical system

\begin{eqnarray}
\dot{x} = f(x); \quad x \in \RR^n \tag{1}
\end{eqnarray}
{: style="text-align: center"}

Our system is called *autonomous* as its dynamics, specified by the vector field $f: \RR^n \rightarrow \RR^n$, do not change over time. We will call $RR^n$ the **phase space**, and $x \in RR^n$ a **state vector** of $\tag{1}$. Furthermore, the position of a state vector $x$ at time $t$, denoted $x(t)$ will be called the **state** of our dynamical system.

The flow of system $\tag{1}$, is a map $\theta: \RR \times \RR^n \rightarrow \RR^n$ such that $\phi(t,x) \in \RR^n$ is the future state of the current state $x \in \RR^n$ after the passage of time $t \in \RR$. When conditions on the smoothness of $f(x)$ are given, at a minimum Lipschitz continuity, we are guaranteed the existence, uniqueness, and continuity of such a map. However, without additional assumptions on the boundedness of $f(x)$, the flow may become unbounded in finite time, in which case we will consider the so-called local flow $\theta: \Omega \rightarrow \RR^n$, where $\Omega$ is an open subset of $\RR \times \RR^n$ containing $\lbrace 0 \rbrace \times \RR^n$.

For $t \in \RR$, we use the notation $\phi_t: \RR^n \rightarrow \RR^n$ to denote the evolution of the phase space by time $t$, i.e. $\phi_t(x) = \phi(t,x)$. The family of diffeomorphisms $\lbrace \phi_t \rbrace_{t \in \RR}$ provide a rule...

The flow of an autonomous dynamical system, such as $\tag{1}$, will satisfy the Kolmogorov conditions
1. $\phi_0(x) = x$
2. $\phi_t (\phi_s (x)) = \phi_{t + s} (x)$

It will be useful to describe the Kolmogorov conditions in plain language. From the first condition, we might understand that, at any particular time $t$, the state of our dynamical system is fixed. Condition $2$ tell us that, if the phase space were allowed to evolve first time $s$ and then time $t$, the system would be in the same state as if the phase space were instead allowed to evolve time $s+t$.

For some current state, $x_0 \in \RR^n$ the solution $\phi(t,x_0)$ traces a curve in $\RR^n$ as $t \in RR$ is varied, called a trajectory of the system. Furthermore, $\forall_{x \in \RR^n}$ the vector $f(x)$ is tangent to the trajectory passing through $x$ and the time derivate of the flow evaluated at $t=0$ coincides with $f(x)$ 
- $\frac{d}{dt} \phi(t,x) \vert_{t = 0} = f(x)$

The flow of a dynamical system form a family of diffeomorphisms $G:=$

### Linear Dynamical Systems <a name="S1s1"></a>

A linear dynamical system has the form

\begin{eqnarray}
\dot{x} = Ax; \quad x \in \RR^n \tag{2}
\end{eqnarray}
{: style="text-align: center"}

Let us consider the planar dynamical system given by
- $\dot{x} = \begin{bmatrix} \alpha & -1\\1 & \alpha \end{bmatrix} x; \quad x \in \RR^2$


## Appendix <a name="SA"></a>
