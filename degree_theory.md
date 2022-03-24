---
layout: post
title: 'Planar Degree Theory'
---

### Degree Theory in $$\mathbb{R}^1$$


Recall the <a href="https://en.wikipedia.org/wiki/Intermediate_value_theorem">$$\underline{Intermediate Value Theorem}:$$</a> If $$ f:[a,b] \rightarrow \mathbb{R} $$ is continous with $$ f(a)f(b) \neq 0 $$
then $$\exists c \in (a,b)$$ such that $$f(c) = 0.$$

Take $$\Omega \subset \mathbb{R},$$ a bounded open set. For simplicity, suppose $$\Omega$$ can be 
constructed as the finite, disjoint union of open intervals. Take also $$f: \overline{\Omega} \rightarrow \mathbb{R}$$
a map without zeros on the boundary of $$\Omega$$, i.e. such that $$\forall t \in \partial \Omega \; f(t) \neq 0.$$
We call the pair $$(f, \Omega)$$ admissible and denote by $$M(\mathbb{R})$$ the collection of all such admissible pairs.

A degree on the set $$M(\mathbb{R})$$ is a map $$\operatorname{deg}: M(\mathbb{R}) \rightarrow \mathbb{Z}$$ satisfying:

$$(1) \mathbf{Additivity}:$$ Given admissible pair $$(f,\Omega)\inM(\mathbb{R})$$ with $$\Omega_1,\Omega_2 \subset \Omega$$ such that $$\Omega_1 \cap \Omega_2 = \emptyset$$ and $$f^{-1}(0) \subset \Omega_1 \cup \Omega_2$$ then 
$$\\ \operatorname{deg}(f, \Omega) = \operatorname{deg}(f, \Omega_1) + \operatorname{deg}(f, \Omega_2)$$

$$(2) \mathbf{Homotopy}:$$ Let $$h_t: \overline{\Omega} \rightarrow \mathbb{R}$$ be continous in both variables
$$t\in \[0,1\]$$ and $$x \in \Omega$$ such that the family, $$(h_t, \Omega),$$ is admissible $$\forall t.$$ Then $$h_t$$
is called an $$\Omega$$-admissible homotopy between $$h_0$$ and $$h_1.$$

$$deg(h_t, \Omega)$$ is constant, that is, the degree is independent of the parameter $$t.$$