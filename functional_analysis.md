---
layout: post
title: 'Functional Analysis'
---

# Basic Topology

## Normed Spaces, Metric Spaces, Topological Spaces
A vector space $$V$$ together with a function $$\Vert \cdot \Vert : V \rightarrow \mathbb{R}$$ satisfying:
$$\\ \forall v\in V, \forall r\in \mathbb{R}$$ we have 
1.  $$\Vert v \Vert \ge 0$$ and $$\Vert v \Vert = 0 \iff v = 0$$
2.  $$\Vert rV \Vert$$ $$=$$ $$\vert r \vert \Vert v \Vert$$
3.  $$\Vert u+v \Vert \le \Vert v \Vert + \Vert u \Vert$$
is called a normed space and the function $$\Vert \cdot \Vert$$ is called a norm on $$V.$$

*Remark:* Any normed space $$(V, \Vert \cdot \Vert)$$ is also a metric space $$(V,d)$$ where
$$d: VxV \rightarrow \mathbb{R}$$ satisfies the metric space properties:
$$\\ \forall u,v,w\in V$$ we have 
1.  $$d(u,v) \ge 0$$ and $$d(u,v) = 0 \iff u = v$$
2.  $$d(u,v)$$ $$=$$ $$d(v,u)$$
3.  $$d(u,v) \le d(u,w) + d(w,v)$$
indeed it is sufficient to take $$d(u,v) := \Vert u-v \Vert.$$

Furthermore, it is the case that any metric space $$(V,d)$$ is in addition a topological space $$(V, {\Large \tau})$$ where
$${\Large \tau}$$ is a collection of subsets of $$V,$$ called a topology on $$V,$$ satisfying:
1.  $$V, \emptyset \in {\Large \tau}$$ $$ $$
2.  $$\{ U_{\alpha} \}_{\alpha \in \Lambda} \subset {\Large {\Large \tau}} \rightarrow \bigcup_{\alpha \in \Lambda}U_{\alpha} \in {\Large \tau}$$
3.  $$\{ \, U_{\alpha_1}, U_{\alpha_2}, \ldots , U_{\alpha_n} \, \} \subset {\Large \tau} \rightarrow U_{\alpha_1} \bigcap U_{\alpha_2} \bigcap \cdots \bigcap U_{\alpha_n} \in {\Large \tau}$$ 

The sets $$U \in {\Large \tau}$$ are called open.

We now recall the notion of an open subset of a normed space $$V.$$ A subset $$U \subset V$$ is said to be open if

$$
\begin{eqnarray*} 
\forall_{ u \in U} \exists_{\epsilon \geq 0} \forall_{ v \in V} \| u - v \| < \epsilon \Rightarrow	v \in U \\
\textstyle{or}, \textstyle{equivalently}, \forall_{ u \in U} \exists_{\epsilon \geq 0} B_{\epsilon}(u) \subset U.
\end{eqnarray*} 
$$
{: style="text-align: center"}

Where $$B_{\epsilon}(u) := \{v \in V: \| u - v \| < \epsilon\}$$ is the open ball of radius $$\epsilon$$ centered at $$u$$.

We will use $$A + B$$ to denote the algebraic sum of sets $$A,B \subset V \\$$  
$$x_0 + A$$ the algebraic sum of an element $$x_0 \in V$$ with the set $$A \subset V\textstyle \\$$
and $$rA$$ the scalar multiplication of a set $$A \subset V\textstyle{.}$$ with the real number $$r \in \mathbb{R}$$

1.  $$A + B := \{a + b: a \in A, b \in B\}$$
2.  $$x_0 \in V \qquad x_0 + A := \{x_0 + a: a \in A\}$$
3.  $$r \in \mathbb{R} \qquad rA := \{ra: a \in A\}$$

** Proposition 1.01 **
$$ 
\begin{eqnarray} 
\Large
B_{\epsilon}(x_0) = x_0 + B_{\epsilon}(0) = x_0 + \epsilon B_1(0) \tag{..1.01a} \label{1.01a} \\
\Large
B_{\epsilon}(x_0) + B_{\delta}(y_0) = (x_0+y_0) + (\epsilon + \delta)B_{1}(0) \tag{..1.01b} \label{1.01b}
\end{eqnarray} 
$$ 
{: style="text-align: center"}

*** Proof ***
1.0.1a: First, we note that any open (or closed) ball, $$B{r}(z)$$, is a convex set, i.e.: 
$$ \forall_{ t \in [0,1]} \forall_{ x,y \in B{r}(z)} tx + (1-t)y \in B{r}(z).$$

We recall that any normed space $$(V, \|\cdot\|) $$ is a metric space $$(V,d(\cdot,\cdot)),$$ with induced metric $$d(u,v) = \|u-v\|,$$ and any metric space is a topological space $$(V, \Tau) $$

** Proposition 1.02 **
Let $$(V, \|\cdot\|)$$ be a normed space with topology $${\Large {\Large \tau},$$ then
1. $$U \in \Tau \Rightarrow \forall_{ x_{0} \in V} x_{0} + U \in \Tau \tag{..1.02a} \label{1.02a}$$
2. $$U \in \Tau \Rightarrow \forall_{ r \neq 0} rU \in \Tau \tag{..1.02b} \label{1.02b}$$


*** Proof ***
1.0.2a:
Let $$U \in \Tau$$ then $$\forall_{ x \in U} \exists_{\epsilon > 0} B_{\epsilon}(x) \subset U$$
So, $$\forall_{ x_{0} \in V} x_0 + B_{\epsilon}(x) \subset x_0 + U $$
By $$\label{1.01a}$$ this is equivalent to $$ B_{\epsilon}(x+x_0) \subset x_0 + U \iff x_0 + U \in \Tau$$
More generally if $$A \in V$$ then 
$$A+U = \{a+x: a \in A, x \in U \} = \cup_{a \in A} a + U \in \Tau $$