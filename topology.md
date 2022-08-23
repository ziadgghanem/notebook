---
layout: post
title: 'Topology'
---

In this post we will make reference to an abstract topological space, $(M \tau)$, unless otherwise stated. 

<div class="definition" markdown="1">

**Definition:** Basis

We call a collection of open sets $\beta \subset \tau$ a *basis for the topology of $M$* if every open set can be represented as a union of elements from the basis, i.e. $\beta \subset \tau$ is a basis if $\forall_{U \in \tau}$ $\exists_{ \lbrace \Beta_{\lambda} \rbrace_{\lambda \in \Lambda} \subset \beta}$ with $U = \cup_{\lambda} \Beta_{\lambda}$
</div>

**Remark:** Elements of the basis are called *basic neighborhoods*

<div class="proposition" markdown="1">

**Theorem:** Necessary and Sufficient Conditions for Basis

A collection of open sets $\beta \subset \tau$ is a basis if and only if $\forall_{U \in \Tau}$ and $\forall_{x \in U}$, $\exists_{\Beta \in \beta}$ with $x \in \Beta$ and $\Beta \subset U$
</div>

<div class="definition" markdown="1">

**Definition:** Local Basis 

A local basis for a point $x \in M$ is a collection of open sets $\beta \subset \tau$ such that for any open neighborhood of $x$, $U \in \tau$, there exists a basic neighborhood $\Beta \in \beta$ with $x \in \Beta$ and $\Beta \subset U$
</div>

<div class="definition" markdown="1">

**Definition:** First Countability

A topological space $M$ is said to be first countable if every point has a countable local basis.
</div>

<div class="definition" markdown="1">

**Definition:** Seperability

A topological space $M$ is said to be seperable if it conntains a countable, dense subset $X \subset M$.
</div>

<div class="definition" markdown="1">

**Definition:** Second Countability

A topological space $M$ is said to be second countable if there exists a countable basis for the topology of $M$. 
</div>