---
layout: post
title: 'Algebraic Topology'
---

## Concepts

*Topological Equivalence:* Let $$X, Y$$ be topological spaces, we say that two sets $$X,Y$$ are homeomorphic if there exists a continuous bijection $$\phi : X \rightarrow Y.$$
- $$X \simeq Y \iff \exists_{\phi : X \rightarrow Y}$$ homeomorphism.

*Topological Invariant:* An algebraic object that is unchanged under homeomorphism. 
- e.g.: # of connected components, Euler characteristic, fundamental group.

*Topological Property:* A property that is unchanged under homeomorphism
- e.g.: compactness, connectedness, path connectedness, seperability.

<hr width="50%">

*Homotopic Maps:* 
Two maps $$f_0, f_1:X \rightarrow Y$$ are said to be homotopic if $$\exists$$ a map $$F:X \times I \rightarrow Y$$
such that $$F(\cdot, 0) = f_0$$ and $$F(\cdot, 1) = f_1$$ 

*Remark:* In this post we will use $$I$$ to denote the unit interval $$[0,1].$$

**Lemma:** Let $$C$$ be a convex space with $$f,g: X \rightarrow C$$ where $$X$$ is any topological space. Then $$f,g$$ are homotopic.

*Example:* Any two maps $$f,g: S^1 \rightarrow \mathbb{R}^2$$ are homotopic.

*Homotopic Equivalence:*
Two topological spaces $$X,Y$$ are said to be of the same homotopy class, $$X \sim Y,$$ if and only if there exist maps $$f:X \rightarrow Y$$ and $$g:Y \rightarrow X$$ such that
1. $$g \circ f \sim$$ $$\mathbb{1}_{X}$$
2. $$f \circ g \sim$$ $$\mathbb{1}_{Y}$$

*Remark:* In this post we will use $$\mathbb{1}_{X}$$ to denote the identity map on a space $$X.$$

*Example:* The disk is homotopically equivalent to a point
- $$D^2$$ $$\sim \cdot$$
*Proof:*
We must find maps $$f:X \rightarrow Y$$ and $$g:Y \rightarrow X$$ that satisfy $$g \circ f \sim$$ $$\mathbb{1}_{X}$$ and 
$$f \circ g \sim$$ $$\mathbb{1}_{Y}.$$
- Take $$f: D^2 \rightarrow \cdot$$ as $$f(x) = p$$ 
- Take $$g: \cdot \rightarrow D^2$$ as $$g(p) = 0)
- Then, $$f \circ g = \mathbb{1}_{p}$$ and, as $$D^2$$ is convex and $$g \circ f = 0 \sim \mathbb{1}_{X}$$

<hr>

## C.W. Complexes
### Notation
*n-disk:* The n-dimensional disk, a closed subset of $$R^n,$$ is defined
- $$D^n$$ $$:= \{ x \in \mathbb{R}^n : \vert x \vert \leq 1 \}$$

*open n-disk:* The interior of an n-disk is
- $$D^n$$ $$:= \{ x \in \mathbb{R}^n : \vert x \vert < 1 \}$$

*n-sphere:* The n-dimensional sphere is the boundary of an $$n+1$$ dimensional n-disk
- $$S^n$$ $$:= \{ x \in \mathbb{R}^n : \vert x \vert = 1 \}$$

<hr width="50%">

### Cell Decomposition
*n-cell:* The n-cell is any space homeomorphic to the open n-disk.

*cell-decomposition:* The cell-decomposition of topological space $$X$$ is the family $$\mathcal{E} := \{e_i \vert i \in I \}$$ where each $$e_i \subset X$$ is a cell residing in $$X$$ such that
- $$X = \sqcup_{i \in I} e_i \quad$$ that is, $$X$$ is the disjoint union of cells in $$E.$$

*n-skeleton:* The n-skeleton of $$X$$ is the subset $$\{e_i \vert i \in I$$  and $$dim(e_i) \leq n \}$$

*C.W. complex:* The pair $$(X,\mathcal{E})$$ consisting of topological space $$X$$ and cell decomposition $$E$$ is called a C.W. complex.

**Proposition:** A C.W. complex is a topological space $$X$$ and a sequence of n-skeletons such that
- $$\emptyset \subset X^0 \subset X^1 \subset \cdots \subset X^n \subset \cdots \subset X$$

**Proposition:** Let $$(X,\mathcal{E})$$ be a C.W. complex. The n-skeleton $$X^n$$ is obtained recursively from $$X^{n-1}$$ by attatching the boundaries of n-cells to the $$n-1$$ skeleton via maps $$\phi_i: \partial D^n_{i} \rightarrow X^{n-1}$$

### Excercises


### Fundamental Group \\
Let $$X$$ be a topological space, A path in $$X$$ is a continous map $$\alpha: I \rightarrow X.$$
Lets define a composition operation on the space of paths 
$$P(X):=\{ \alpha: I \rightarrow X \}$$ Consider the paths $$\alpha , \beta \in P(X)$$ with $$\alpha(0) = \beta(1) = p \in X.$$ 
We define a new path $$\alpha \circ \beta : I \rightarrow X$$ and call it the composition of $$\alpha$$ and $$\beta.$$

$$
\Large
\alpha \circ \beta = 
        \begin{cases} 
          \alpha(2t) & t \in [0, \frac{1}{2}] \\
          \beta(2t-1) & t \in [\frac{1}{2}, 1] 
       \end{cases}
$$

*Terminology:*
1.   We say that two paths $$\alpha , \beta \in P(X)$$ are *homotopic* if there exists a continuous map $$h_t: I \rightarrow X$$ with $$h_0 = \alpha$$ and $$h_1 = \beta.$$ In which case we write $$\alpha \simeq \beta.$$
2. Homotopy is an equivalence relation on $$P(X),$$ the equivalence classes are called homotopy classes, and composition of loops induces a multiplication of homotopy classes: $$<\alpha> \circ <\beta> = <\alpha \circ \beta>$$
3.  A path $$\alpha: I \rightarrow X$$ whose initial and endpoints coincide in $$X,$$ i.e. $$\alpha(0) = \alpha(1) = p$$, we call a loop based at $$p \in X$$.
4.  A loop that can be contracted to a point (by which we mean the loop is homotopic to a point $$\alpha \simeq \cdot$$) is called *simple* otherwise it is called non-contractible. 

We are interested in using loops to distinguish between topological spaces. 

**Theorem** \\
Let $$X$$ be a topological space. The set of loops in $$X$$ based at $$p$$ forms a group, $${\Large \pi}_1(X,p): = \{ <\alpha> \quad \Vert \quad \alpha(0)=\alpha(1), \, \alpha:I \rightarrow X \}$$ with multiplication $$<\alpha> \circ <\beta> = <\alpha \circ \beta>$$

***Proof*** \\
0. $${\Large \pi}_1(X,p),$$ is well defined. \\
For $$\alpha \simeq \alpha^{'}, \beta \simeq \beta^{'}$$ we have $$\alpha \circ \beta \simeq \alpha^{'} \circ \beta^{'}$$
1. *Associativity* $$(<\alpha> \circ <\beta>) \circ <\gamma> = <\alpha> \circ (<\beta> \circ <\gamma>)$$ \\
$$(\alpha \circ \beta) \circ \gamma = \alpha \circ (\beta \circ \gamma)$$
2. *Identity element* $$e:I \rightarrow X$$ such that $$e(t) \equiv p$$
3. *Inverse element* $$\alpha^{-1} = \alpha(1-t)$$ such that $$\alpha \circ \alpha^{-1} = \alpha^{-1} \circ \alpha \equiv p$$

**Definition** \\
We say that $$X$$ is simply connected if it is path connected and $$\Large{\pi}_1(X,p) = {0}$$

**Lemma** \\
$$X$$ is simply connected iff there exists a unique homotopy class of paths between any two paths in $$X$$.
 
<hr>

## Complete Classification of Surfaces

A surface is said to be closed if it is compact, connected, and has no boundary. 
A classification of the space of closed surfaces is a list of topologically distinct classes such that, given any closed surface $$S$$, one has exactly one class $$S$$ and for any other closed surface $$L$$ one has $$L \in <S>$$ if and only if $$L$$ is homeomorphic to $$S$$

**Classification Theorem** \\ 
Any closed surface is homeomorphic one of the following:
1. The sphere.
2. The sphere with a finite number of handles.
3. The shere with a finite number of disks removed and replaced with mobius strips.

How do we add a handle to the sphere? First we remove the interiors of a pair of disjoint discs, then we attach a cylinder by glueing its boundary circles to the boundary circles of the chosen discs. To add further handles we repeat this procedure with another pair of discs and cylinder.

**Lemma** \\
Every closed surface $$S$$ can be triangulated.

***Outline of Proof*** \\
Consider a closed surface $$S$$. As $$S$$ is closed, it must be compact and so it can be converred by a finite collection of closed discs whose union is $$S$$. Moreover we can find a finite cover such that the boundaries of any two discs
meet with an at most finite number of points and arcs. Such a cover can be partitioned into a finite number of disjoint *patches* each homeomorphic to the disc. Hence, each patch is triangulable and the triangulation of the partitioned cover returns a finite cover of disjoint triangles which covers our surface $$S$$.

A surface $$S$$ is said to be orientable if it has one of the following equivalent properties:
1. $$S$$ has two "sides" which can each be seperately colored. 
2. Any loop in the surface does not change direction.
3. $$S$$ does not contain a copy of the mobius strip.

**Lemma** \\
Any loop that changes direction is itself a copy of the mobius strip so we have, in fact, that A closed surface is non-orientable if and only if it contains a mobius strip.

**Definition** \\
Let $$S$$ be any triangulable surface. Let $$v$$ be the number of vertices, $$e$$ the number of edges and $$t$$ the number of triangles used in triangulation. Then the Euler Characteristic of $$S$$ is $$\chi(S) = v - e + t.$$

<hr>

**Definition (Triangulation):** \\
Let $$V:= \{ v_0,v_1, \ldots ,v_k \}$$ be points in $$\mathbb{R}^n.$$ We call the set
$$\Delta:= \{ \lambda_0 v_0 + \lambda_1 v_1 + \cdots + \lambda_k v_k \vert \quad \lambda_i \in \mathbb{R}, \sum_{i=0}^k \lambda_i = 1\}$$ 
the hyperplane spanned by $$V$$. \\
We say that the points $$\{ v_0,v_1, \ldots ,v_k \}$$ are in *general position* if any subset of them spans a strictly smaller subset. 

**Lemma** \\
A set $$V:= \{ v_0,v_1, \ldots ,v_k \}$$ is in general position if and only if the set of vectors $$\{ v_1 - v_0,v_2 - v_0, \ldots ,v_k - v_0 \}$$ is linearly independent. \\


- Given $$k+1$$ points $$V:= \{ v_0,v_1, \ldots ,v_k \}$$ in general position, we call the smallest convex set containing them a k-simplex with vertices $$\{ v_0,v_1, \ldots ,v_k \}.$$ By assigning an order to the vertices of our k-simplex we define an ordered k-simplex $$\[ v_0,v_1, \ldots ,v_k \]$$ \\

- If $$A,B$$ are simplexes and the vertices of B are some subset of the vertices of A then we say that B is a face of the simplex A. The subsimplex of an ordered simplex inherits an induced order from its supersimplex. \\

- *e.g.* Consider the ordered 2-simplex $$\sigma = \[ v_0, v_1, v_2 \].$$ We specify three 1-faces of $$\sigma$$

$$
x = \begin{cases}
[v_0, v_1] \\
[v_0, v_2]\\
[v_1, v_1]
\end{cases}
$$

**Definition (Simplicial Complex):** \\ A finite collection of simplexes in $$\mathbb{R}^n$$ is called a simplicial complex if whenever a ssimplex lies in the collection then so does each of its faces and whenever two simplexes of the collection intersect they do so in a common face. \\

We call a topological space *triangulable* if it is homeomorphic to a simplicial complex. \\




