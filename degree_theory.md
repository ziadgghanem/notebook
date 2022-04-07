---
layout: post
title: 'Planar Degree Theory'
---

### Degree Theory in $$\mathbb{R}^1$$


Recall the <a href="https://en.wikipedia.org/wiki/Intermediate_value_theorem">Intermediate Value Theorem:</a> If $$ f:[a,b] \rightarrow \mathbb{R} $$ is continous with $$ f(a)f(b) \neq 0 $$
then $$\exists c \in (a,b)$$ such that $$f(c) = 0.$$

Take $$\Omega \subset \mathbb{R},$$ a bounded open set. For simplicity, suppose $$\Omega$$ can be 
constructed as the finite, disjoint union of open intervals. Take also $$f: \overline{\Omega} \rightarrow \mathbb{R}$$
a map without zeros on the boundary of $$\Omega$$, i.e. such that $$\forall t \in \partial \Omega \; f(t) \neq 0.$$
We call the pair $$(f, \Omega)$$ admissible and denote by $$M(\mathbb{R})$$ the collection of all such admissible pairs.

A degree on the set $$M(\mathbb{R})$$ is a map $$\operatorname{deg}: M(\mathbb{R}) \rightarrow \mathbb{Z}$$ satisfying:

$$(1) \; \mathbf{Additivity}:$$ Given admissible pair $$(f,\Omega)\in M(\mathbb{R})$$ with $$\Omega_1,\Omega_2 \subset \Omega$$ such that $$\Omega_1 \cap \Omega_2 = \emptyset$$ and $$f^{-1}(0) \subset \Omega_1 \cup \Omega_2$$ then 
$$\\ \operatorname{deg}(f, \Omega) = \operatorname{deg}(f, \Omega_1) + \operatorname{deg}(f, \Omega_2)$$

$$(2) \; \mathbf{Homotopy}:$$ Let $$h_t: \overline{\Omega} \rightarrow \mathbb{R}$$ be continous in both variables
$$t\in [0,1]$$ and $$x \in \Omega$$ such that the family, $$(h_t, \Omega),$$ is admissible $$\forall t.$$ Then $$h_t$$
is called an $$\Omega$$-admissible homotopy between $$h_0$$ and $$h_1.$$

For any $$\Omega$$-admissible homotopy, $$(h_t, \Omega),$$ deg(h_t, \Omega)$$ is constant, that is, the degree is independent of the parameter $$t.$$

$$(3) \; \mathbf{Normalization}:$$ For all admissible pairs, $$(f, \Omega),$$ with $$\Omega$$ an open, bounded set and $$f(t) = t - t_0$$
we have 

<hr>

### algebras and the existence of bounded/periodic solutions to dynamical systems 

Definitionss: Let $$V$$ be a vector space over a field $$K$$ (either $$\mathbb{R}$$ or $$\mathbb{C}$$). We equip $$V$$ with an additional operation $$*: V \times V \rightarrow V$$ satisfying the properties: $$\forall a,b,c \in V \, \forall \alpha, \beta \in K$$
1. (Right Distributivity) $$(\alpha a + \beta b) * c = \alpha(a*c) + \beta(b*c)$$
2. (Left Distributivity) $$c * (\alpha a + \beta b) = \alpha(c*a) + \beta(c*b)$$
Then we say that $$V$$ is an algebra over the field $$K$$ or we may call $$V$$ a $$K$$-algebra and write $$(V, *)$$. 

An Algebra is a vectorr space with an additional operator that is bilinear.

We will consider three classes of algebras, $$(A, *)$$ is called:
1. Commutative if $$a*b = b*a \quad \forall a,b \in A$$
2. Associative if $$(a*b)*c = a*(b*c) \quad \forall a,b,c \in A$$
3. Unital if $$\exists e \in A$$ st $$\forall a \in A a*e=e*a=a$$

For our purposes, an algebra satisfying atleast one of the above properties will be considered *reasonable*.

***Examples***
1. $$(\mathbb{C}, \cdot)$$ The complex numbers with standard complex multiplication is *commutative,* *associative* and *unital*
2. $$(\bar{\mathbb{C}}, *)$$ The complex numbers with the following multiplication: $$\forall z_1, z_2 \in \mathbb{C} \quad z_1 * z_2 = \bar{z_1} * \bar{z_2}$$ is *commutative,* *associative* but *not unital*
3. $$(\mathbb{R} \widehat{\bigoplus} \mathbb{R}, *)$$ with the following multiplication: $$ \forall u = (u_1, u_2) v = (v_1, v_2) \quad u*v = (u_1v_1, u_2,v_2)$$ is *commutative,* *associative* and *unital*
4. $$(M(n,K), \cdot)$$ The group of $$n \cross n$$ matrices with entries from field $$K$$ with the usual matrix multiplication. is *associative,* *unital* but *not commutative*
5. $$((C[a,b], K),*)$$ The space of functions continous over the interval $$[a,b] \subset K$$ with the usual function multiplication $$f*g = f(x) \cdot g(x) \, \forall x \in [a,b]$$ is *commutative,* *associative* and *unital*

**Terminology: Finite Dimensional Algebras** 

If the underlying vector space $$A$$ is finite-dimensional then we say $$(A,*)$$ is a finite dimensional algebra.

Given an $$n-$$ dimensional vector space $$A$$ one might want to define a multiplication $$*$$ on this space to construct an algebra $$(A,*).$$ This can be achieved as follows:
1. Take a basis $$\{e_1, \ldots , \e_n \}$$
2. Fix $$i,j$$ from $$1:n$$ and put $$e_j * e_i := \sum_{k=1}^n \alpha_{i \, j}^{k} e_{k} = \alpha_{i \, j}^{1} e_{1} + \cdots + \alpha_{i \, j}^{n} e_{n}$$ where $$\alpha_{i \, j}^{k}$$$ are chosen from our field.
3. In general we will need to specify $$n^3$$ coefficients $$\alpha_{i \, j}^{k} \in K$$ in order to define a particular multiplication over $$A$$.
4. Suppose we wanted to define a *commutative* multiplication, then $$\forall i,j,k \alpha_{i \, j}^{k}= \alpha_{j \, i}^{k}$$

***Example*** 

Take $$\mathbb{C}$$ and define the usual complex multiplication $$*$$ using the above strategy. 

We have the standard basis $$e_1 = (1,0), e_2 = (0,1)$$. As complex multiplication is *commutative* it is sufficient to define three products: 
1. $$e_1 * e_1 = \alpha_{11}e_1 + \alpha_{12}e_2 = e_1$$ i.e. $$(1,0)*(1,0) = (1,0) $$ or $$1 \cdot 1 = 1$$
2. $$e_1 * e_2 = \alpha_{21}e_1 + \alpha_{22}e_2 = e_2$$ i.e. $$(1,0)*(0,1) = (0,1) $$ or $$1 \cdot i = i$$
3. $$e_2 * e_2 = \alpha_{31}e_1 + \alpha_{32}e_2 = -e_1$$  i.e. $$(0,1)*(0,1) = (0,1) $$ or $$i \cdot i = -1$$

So for $$x = (x_1, x_2), y = (y_1, y_2) \in \mathbb{C}$$ we have

$$ (x_1, x_2)*(y_1, y_2) = (\alpha_{11}x_1y_1 + \alpha_{31}x_2y_2, \alpha_{22}x_1y_2 + \alpha_{22}x_2y_2) = (x_1y_1 - x_2y_2, x_1y_2 + x_2y_2)$$

**Definition: Left Multiplication Matrix, norm, trace** 

Given an algebra $$(A,*)$$ take a fixed element $$x \in A.$$ We define 
1. The so-called *left multiplication matrix* $$J_A(x): A \rightarrow A$$ is $$ J_A(x) \cdot y := x * y$$
2. The norm of A $$ \gamma_2 := \det J_A(x)$$
3. The trace of A $$\gamma_1 := \operatorname{Tr} J_A(x)$$

***Example*** 

Take $$(\mathbb{C}, \cdot)$$ the complex numbers with their usual multiplication. Choose $$z_1 = (x_1,y_1), z_2 = (x_2,y_2)$$ we have $$z_1 \cdot z_2 = (x_1 x_2 - y_1 y_2, x_1 y_2 + x_2 y_1)$$ the right multiplication matrix is

$$ \Large J_A(z_1) =  \begin{pmatrix}x_1 & -y_1\\\ y_1 & x_1\end{pmatrix}$$

$$  \Large J_A(z_1)z_2 = \begin{pmatrix}x_1 & -y_1\\\ y_1 & x_1\end{pmatrix} \begin{pmatrix}x_2 \\\ y_2 \end{pmatrix} = \begin{pmatrix}x_1 x_2 - y_1 y_2 \\\ x_1 y_2 + x_2 y_1 \end{pmatrix}$$

With determinant $$\det J_A(x) = x_1^2 + y_1^2 = \lVert z_1 {\rVert}_{2}^2$$


**Theorem (Cayley-Hamilton):** 

Let $$(A,*)$$ be a $$2-$$dimensional algebra, then $$ \forall x,y \in A x*(x*y) = \gamma_{1}(x) (x*y) - \gamma_{2}(x) y$$ \\

**Corollary**

If in addition $$(A,*)$$ is commutative, we have $$x*(x*x) = x^3 = \gamma_{1}(x) x^2 - \gamma_{2}(x) x$$ 

***Proof***

Recall that for any $$n \times n$$ matrix $$A$$ with characteristic polynomial $$P( \lambda ) = a_0 + a_1 \lambda + \cdots + a_n \lambda^n$$
then $$P(A) =  a_0 + a_1 A + \cdots + a_n A^n = 0$$ i.e. in general, any square matrix $$A$$ annihilates its own characteristic polynomial. We will show this is the case for $$n=2$$ \\
Take $$A =  \begin{pmatrix}a & b\\\ c & d\end{pmatrix}$$ it is well known that the characteristic polynomial of a $$2x2$$ matrix is given by $$ P( \lambda ) = \lambda^2 -  \operatorname{Tr}(A) \lambda + \det(A) \cdot Id_{2 \times 2}$$ where $$\det(A) = (ad - bc)$$ and $$\operatorname{Tr}(A) = a + d$$ \\
So $$P(A) = A^2 - \operatorname{Tr}(A) A + \det(A) \cdot Id_{2 \times 2}
 \begin{pmatrix}a & b\\\ c & d\end{pmatrix} \begin{pmatrix}a & b\\\ c & d\end{pmatrix} 
 - (a+d) \begin{pmatrix}a & b\\\ c & d\end{pmatrix}
 + \begin{pmatrix}ad - bc & 0\\\ 0 & ad - bc\end{pmatrix} 
 = \begin{pmatrix}a^2 + bc - a^2 - ad + ad - bc & ab + bd - ab - db\\\ ca + dc - ac + dc & cb + d^2 - ad - d^2 + ad -bc\end{pmatrix}
 = \begin{pmatrix}0 & 0\\\ 0 & 0\end{pmatrix} $$




