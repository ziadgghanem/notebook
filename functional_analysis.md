---
layout: post
title: 'Functional Analysis'
---

# Basic Topology

## Normed Spaces, Metric Spaces, Topological Spaces

**Normed Space** \\
A vector space $$V$$ together with a function $$\Vert \cdot \Vert : V \rightarrow \mathbb{R}$$ satisfying:
$$\\ \forall v\in V, \forall r\in \mathbb{R}$$ we have 
1.  $$\Vert v \Vert \ge 0$$ and $$\Vert v \Vert = 0 \iff v = 0$$
2.  $$\Vert rV \Vert$$ $$=$$ $$\vert r \vert \Vert v \Vert$$
3.  $$\Vert u+v \Vert \le \Vert v \Vert + \Vert u \Vert$$
is called a normed space and the function $$\Vert \cdot \Vert$$ is called a norm on $$V.$$

**Metric Space** \\
*Remark:* Any normed space $$(V, \Vert \cdot \Vert)$$ is also a metric space $$(V,d)$$ where
$$d: VxV \rightarrow \mathbb{R}$$ satisfies the metric space properties:
$$\\ \forall u,v,w\in V$$ we have 
1.  $$d(u,v) \ge 0$$ and $$d(u,v) = 0 \iff u = v$$
2.  $$d(u,v)$$ $$=$$ $$d(v,u)$$
3.  $$d(u,v) \le d(u,w) + d(w,v)$$
indeed it is sufficient to take $$d(u,v) := \Vert u-v \Vert.$$

**Topological Space** \\
Furthermore, it is the case that any metric space $$(V,d)$$ is in addition a topological space $$(V, {\Large \tau})$$ where
$${\Large \tau}$$ is a collection of subsets of $$V,$$ called a topology on $$V,$$ satisfying:
1.  $$V, \emptyset \in {\Large \tau}$$ $$ $$
2.  $$\{ U_{\alpha} \}_{\alpha \in \Lambda} \subset {\Large {\Large \tau}} \rightarrow \bigcup_{\alpha \in \Lambda}U_{\alpha} \in {\Large \tau}$$ $$ $$
3.  $$\{ \, U_{\alpha_1}, U_{\alpha_2}, \ldots , U_{\alpha_n} \, \} \subset {\Large \tau} \rightarrow U_{\alpha_1} \bigcap U_{\alpha_2} \bigcap \cdots \bigcap U_{\alpha_n} \in {\Large \tau}$$ $$ $$

The sets $$U \in {\Large \tau}$$ are called open.

**Open Set** \\
We now recall the notion of the open subset of a normed space $$V.$$ 
A subset $$U \subset V$$ is said to be open if: 
- $$ \forall_{ u \in U} \exists_{\epsilon \geq 0} \forall_{ v \in V} \| u - v \| < \epsilon \Rightarrow	v \in U $$

Or equivalently,

- $$\forall_{ u \in U} \exists_{\epsilon \geq 0} B_{\epsilon}(u) \subset U $$ $$ $$

Where $$B_{\epsilon}(u) := \{v \in V: \| u - v \| < \epsilon\}$$ is the open ball of radius $$\epsilon$$ centered at $$u$$.

**Set Manipulation** \\
We will use $$A + B$$ to denote the algebraic sum of sets $$A,B \subset V$$  
- $$A + B := \{a + b: a \in A, b \in B\}$$ $$\\$$

$$x_0 + A$$ is for us algebraic sum of an element $$x_0 \in V$$ with the set $$A \subset V\textstyle$$
- $$x_0 \in V \qquad x_0 + A := \{x_0 + a: a \in A\}$$ 

And by $$rA$$ we mean the scalar multiplication of a set $$A \subset V$$ with the real number $$r \in \mathbb{R}$$
- $$r \in \mathbb{R} \qquad rA := \{ra: a \in A\}$$ $$$$

**Proposition 1.01**
$$\\$$
1. $$ B_{\epsilon}(x_0) = x_0 + B_{\epsilon}(0) = x_0 + \epsilon B_1(0) $$ $$ \tag{..1.01a} \label{1.01a} $$
2. $$ B_{\epsilon}(x_0) + B_{\delta}(y_0) = (x_0+y_0) + (\epsilon + \delta)B_{1}(0) $$   $$ \tag{..1.01b} \label{1.01b} $$

***Proof 1.01b***
$$\\$$
$$(\rightarrow)$$ Suppose $$x \in B_{\epsilon}(0) \iff \Vert x \Vert < \epsilon$$ and $$y \in B_{\delta}(0) \Vert y \Vert < \delta$$
then $$\Vert x + y \Vert < \Vert x \Vert + \Vert y \Vert < \epsilon + \delta$$ such that $$x+y \in B_{\epsilon + \delta}(0) \\$$
$$(\leftarrow)$$ Take $$z \in B_{\epsilon + \delta}(0) \iff \Vert z \Vert < \epsilon + \delta$$ Now choose $$x = \frac{\epsilon}{\epsilon + \delta} z$$ and $$y = \frac{\delta}{\epsilon + \delta} z$$ such that $$\Vert x \Vert < \epsilon \iff x \in B_{\epsilon}(0),$$ $$\Vert y \Vert < \delta \iff y \in B_{\delta}(0),$$ and $$z = x+y \in B_{\epsilon}(0) + B_{\delta}(0)$$

<hr>

**Proposition 1.02**
$$\\$$
Let $$(V, \|\cdot\|)$$ be a normed space with topology $${\Large \tau},$$ then
1. The following functions are continous: $$\tag{..1.02a} \label{1.02a}$$
    1. $$ + : V \times V \rightarrow V $$ $$$$
    2. $$ \cdot : R \times V \rightarrow V $$ $$$$
    3. $$ \Vert \cdot \Vert : V \rightarrow R $$ $$$$
2. $$U \in {\Large \tau} \Rightarrow \forall_{ x_{0} \in V} x_{0} + U \in {\Large \tau}$$ $$\tag{..1.02b} \label{1.02b}$$
3. $$U \in {\Large \tau} \Rightarrow \forall_{ r \neq 0} rU \in {\Large \tau}$$ $$\tag{..1.02c} \label{1.02c}$$


***Proof 1.0.2b:***
$$\\$$
Let $$U \in {\Large \tau}$$ then $$\forall_{ x \in U} \exists_{\epsilon > 0} B_{\epsilon}(x) \subset U$$
So, $$\forall_{ x_{0} \in V} x_0 + B_{\epsilon}(x) \subset x_0 + U $$
By (1.01a) this is equivalent to $$ B_{\epsilon}(x+x_0) \subset x_0 + U \iff x_0 + U \in {\Large \tau}$$
More generally if $$A \in V$$ then 
$$A+U = \{a+x: a \in A, x \in U \} = \cup_{a \in A} a + U \in {\Large \tau} $$

**Equivalence of Norms** \\
Let $$\Vert \cdot \Vert_{1}: V \rightarrow \mathbb{R}$$ $$\Vert \cdot \Vert_{2}: V \rightarrow \mathbb{R}$$ \\
be two norms on vector space $$V.$$ We say that $$\Vert \cdot \Vert_{1}$$ and $$\Vert \cdot \Vert_{2}$$ are equivalent 
when their associated topologies, $${\Large \tau}_{1}$$ and  $${\Large \tau}_{2}$$ respectively, coincide. \\
In the case that $${\Large \tau}_{1} \subset {\Large \tau}_{2}$$ $${\Large \tau}_{1}$$ is said to be weaker thant $${\Large \tau}_{2}$$
and furthermore $$\Vert \cdot \Vert_{1}$$ is said to be weaker than $$\Vert \cdot \Vert_{2}$$

**Theorem 1.03** \\
Given two norms $$\Vert \cdot \Vert_{1}, \Vert \cdot \Vert_{2}$$ on a vector space $$V$$ \\
$${\Large \tau}_{1} \subset {\Large \tau}_{2} \iff \exists_{c > 0} \forall_{x \in V} \Vert \cdot \Vert_{1} \leq c\Vert \cdot \Vert_{2}$$ 