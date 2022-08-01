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

An Algebra is a vector space with an additional operator that is bilinear.

We will consider three classes of algebras, $$(A, *)$$ is called:
1. Commutative if $$a*b = b*a \quad \forall a,b \in A$$
2. Associative if $$(a*b)*c = a*(b*c) \quad \forall a,b,c \in A$$
3. Unital if $$\exists e \in A$$ st $$\forall a \in A a*e=e*a=a$$

For our purposes, an algebra satisfying atleast one of the above properties will be considered *reasonable*.

***Examples***
1. $$(\mathbb{C}, \cdot)$$ The complex numbers with standard complex multiplication is *commutative,* *associative* and *unital*
2. $$(\bar{\mathbb{C}}, *)$$ The complex numbers with the following multiplication: $$\forall z_1, z_2 \in \mathbb{C} \quad z_1 * z_2 = \bar{z_1} * \bar{z_2}$$ is *commutative,* *associative* but *not unital*
3. $$(\mathbb{R} \bigoplus \mathbb{R}, *)$$ with the following multiplication: $$ \forall u = (u_1, u_2) v = (v_1, v_2) \quad u*v = (u_1v_1, u_2,v_2)$$ is *commutative,* *associative* and *unital*
4. $$(M(n,K), \cdot)$$ The group of $$n \times n$$ matrices with entries from field $$K$$ with the usual matrix multiplication. is *associative,* *unital* but *not commutative*
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

We have the standard basis $$e_1 = (1,0), e_2 = (0,1)$$. As complex multiplication is *commutative* it is sufficient to define six coefficients: $$ \begin{pmatrix} \alpha_{1} & \alpha_{2} & \alpha_{3}\\\ \beta_{1} & \beta_{2} & \beta_{3} \end{pmatrix}$$ 
$$= \begin{pmatrix} 1 & 0 & -1\\\ 0 & 1 & 0 \end{pmatrix}$$
1. $$e_1 * e_1 = \alpha_{1}e_1 + \beta_{1}e_2 = e_1$$ $$\iff$$ $$(1,0)*(1,0) = (1,0) $$ $$\iff$$ $$1 \cdot 1 = 1$$
2. $$e_1 * e_2 = \alpha_{2}e_1 + \beta_{2}e_2 = e_2$$ $$\iff$$ $$(1,0)*(0,1) = (0,1) $$ $$\iff$$ $$1 \cdot i = i$$
3. $$e_2 * e_2 = \alpha_{3}e_1 + \beta_{3}e_2 = -e_1$$ $$\iff$$ $$(0,1)*(0,1) = (-1,0) $$ $$\iff$$ $$i \cdot i = -1$$

So for $$x = (x_1, x_2), y = (y_1, y_2) \in \mathbb{C}$$ we have the expected product
- $$ (x_1, x_2)*(y_1, y_2)$$ $$ = (\alpha_{1}x_1y_1 + \alpha_{3}x_2y_2 , \beta_{2}x_1y_2 + \beta_{2}x_2y_2) = (x_1y_1 - x_2y_2, x_1y_2 + x_2y_2)$$

**Definition: Left Multiplication Matrix, norm, trace** 

Given an algebra $$(A,*)$$ take a fixed element $$x \in A.$$ We define 
1. The so-called *left multiplication matrix,* $$J_A(x): A \rightarrow A,$$ is $$ J_A(x) \cdot y := x * y$$
2. The *norm of A:* $$ \quad \gamma_2 := \det J_A(x)$$
3. The *trace of A:* $$\quad \gamma_1 := \operatorname{Tr} J_A(x)$$

***Example*** \\
Take $$(\mathbb{C}, \cdot)$$ the complex numbers with their usual multiplication. For any, $$z_1 = (x_1,y_1), z_2 = (x_2,y_2),$$ we should have $$z_1 \cdot z_2 = (x_1 x_2 - y_1 y_2, x_1 y_2 + x_2 y_1)$$ The appropriate left multiplication matrix is: $$J_A(z_1) = \begin{pmatrix}x_1 & -y_1\\\ y_1 & x_1\end{pmatrix}$$ with norm  $$\gamma_2 = \det (J_A(x)) = x_1^2 + y_1^2 = \lVert z_1 {\rVert}_{2}^2$$ and trace $$ \gamma_1 = \operatorname{Tr} J_A(x) = 2x_1$$
- To confirm we take $$J_A(z_1)z_2 = \begin{pmatrix}x_1 & -y_1\\\ y_1 & x_1\end{pmatrix} \begin{pmatrix}x_2 \\\ y_2 \end{pmatrix} = \begin{pmatrix}x_1 x_2 - y_1 y_2 \\\ x_1 y_2 + x_2 y_1 \end{pmatrix} = z_1 \cdot z_2$$

***Example*** \\
Take $$(\mathbb{R} \bigoplus \mathbb{R}, *)$$ equipped with multiplication $$(x_1,y_1)*(x_2,y_2) = (x_1 x_2, y_1 y_2)$$ this algebra has
1. Left multiplication matrix:  $$J_A(z_1) = \begin{pmatrix}x_1 & 0\\\ 0 & y_1\end{pmatrix}$$ 
2. Norm: $$\gamma_2(z_1) = x_1 y_1$$
3. Trace: $$\gamma_1(z_1) = x_1 + y_1$$

**Theorem (Cayley-Hamilton):** \\
Let $$(A,*)$$ be a $$2-$$dimensional algebra, then $$ \forall x,y \in A x*(x*y) = \gamma_{1}(x) (x*y) - \gamma_{2}(x) y$$ \\

**Corollary** \\
If in addition $$(A,*)$$ is commutative, we have $$x*(x*x) = x^3 = \gamma_{1}(x) x^2 - \gamma_{2}(x) x$$ 

**Lemma** \\ 
for any $$n \times n$$ matrix $$A$$ with characteristic polynomial $$P( \lambda ) = a_0 + a_1 \lambda + \cdots + a_n \lambda^n$$
we have 
- $$P(A) =  a_0 + a_1 A + \cdots + a_n A^n$$ $$= 0$$

i.e. any square matrix $$A$$ annihilates its own characteristic polynomial. We will show this is the case for $$n=2$$ \\
***Proof (Lemma)*** \\
Take $$A =  \begin{pmatrix}a & b\\\ c & d\end{pmatrix}$$ it is well known that the characteristic polynomial of a $$2x2$$ matrix is given by - $$ P( \lambda ) = \lambda^2 -  \operatorname{Tr}(A) \lambda + \det(A) \cdot \mathbb{1}_{2}$$ 

Here we have, $$\det(A) = ad - bc$$ and $$\operatorname{Tr}(A) = a + d$$. \\
Now let's evaluate $$A$$ with its characteristic polynomial: $$P(A) = A^2 - \operatorname{Tr}(A) A + \det(A) \cdot \mathbb{1}_{2} $$

- $$ P(A) = \begin{pmatrix}a & b\\\ c & d\end{pmatrix} \begin{pmatrix}a & b\\\ c & d\end{pmatrix} - (a+d) \begin{pmatrix}a & b\\\ c & d\end{pmatrix} + \begin{pmatrix}ad - bc & 0\\\ 0 & ad - bc\end{pmatrix} $$
- $$ = \begin{pmatrix}a^2 + bc - a^2 - ad + ad - bc & ab + bd - ab - db\\\ ca + dc - ac + dc & cb + d^2 - ad - d^2 + ad -bc\end{pmatrix}
 = \begin{pmatrix}0 & 0\\\ 0 & 0\end{pmatrix} $$

***Proof (Cayley-Hamilton)*** \\
Take the left multiplication matrix, $$J_A(x)$$, with characteristic polynomial $$P( \lambda ) = \lambda^2 -  \operatorname{Tr}(J_A) \lambda + \det(J_A) \cdot \mathbb{1}_{2}$$
- Now, by Lemma we have $$ P(J_A(x)) = J_A(x)^2 - \operatorname{Tr}(J_A(x)) J_A(x) + \det(J_A(x)) \cdot \mathbb{1}_{2} = 0 $$ 
- $$\rightarrow $$ $$ J_A(x)^2 = \operatorname{Tr}(J_A(x)) J_A(x) - \det(J_A(x)) \cdot \mathbb{1}_{2}$$
- $$\rightarrow $$ $$ J_A(x)^2 y = \operatorname{Tr}(J_A(x)) J_A(x) y - \det(J_A(x)) y = \gamma_{1}(x)(x*y) -  \gamma_{2}(x) y$$
- Note $$J_A(x) \cdot y := x * y$$ $$\rightarrow$$ $$x*(x*y) = x*(J_A(x)y) = J_A(x) J_A(x) y = J_A(x)^2 y$$ 

**Definition (Idempotence, Nilpotence)** \\
Let $$(A,*)$$ be a $$K$$-algebra
1. $$a \in A, \, a \neq 0$$ is called idempotent if $$a^2 = a$$
2. $$b \in A, \, b \neq 0$$ is called 2-nilpotent if $$b^2 = 0$$

***Example (Idempotent)*** \\
Any unital algebra $$(A,*)$$ has the obvious idempotent: the unital element $$\exists e \in A$$ with $$\forall a \in A a*e=e*a=a$$ and in particular $$e^2 = e*e = e$$

***Example (2-Nilpotent)*** \\
Consider the group of $$n \times n$$ matrices $$(M(n, \mathbb{R}), \cdot)$$. Take $$a = \begin{pmatrix}0 & 1\\\ 0 & 0\end{pmatrix}$$ and check that $$a^2 = 0$$.

**Theorem** \\
Let $$(A,*)$$ be any $$K$$-algebra. If $$A$$ does not admit 2-nilpotents then $$A$$ must admit at least one idempotent.

***Proof*** \\
Consider the map $$\phi :A \rightarrow A$$ given by $$\phi(u) = u-u^2$$ and assume by contradiction that $$A$$ admits no 2-nilpotents, i.e. $$ \forall u \in A \backslash 0, u^2 \neq 0$$

(i) We note that $$\phi_0:= u$$ is a principal part of $$\phi$$ near the origin with $$\operatorname{Ind}(0, \phi_0) = 1$$

(ii) On the other hand, $$\phi_{\infty}:= u^2$$ is a principal part of $$\phi$$ for some sufficiently large ball $$B_R(0)$$ where, by assumption as $$A$$ does not admit 2-nilpotents, $$\phi_{\infty}$$ is admissible and about which $$deg(\phi_{\infty}, B_R(0)) = deg$$ \\
*remark:* if $$A$$ were such that it admitted at least one 2-nilpotent, $$\hat{u} \in A$$, then it follows that $$ (\alpha u)^2 = 0$$ for all $$ \alpha \in K$$. And so, a algebraic $$2-nilpotent$$ corresponds to a ray solution of the equation $$u^2 = 0$$ such that any ball about the origin would not be an admissible domain for $$\phi_{\infty}$$

(iii) Recall, that a field is homotopically admissible to all of its principal parts, in particular, it must be the case that $$ind(0,\phi_0 ) = ind(0,\phi_{\infty})$$. However, $$ind(0,\phi_0 ) = 1$$ and $$ind(0,\phi_{\infty})$$ is even. 

And so there does not exist an admissible homotopy between $$\phi_0$$ and $$\phi_{\infty}$$ hence there exists $$u^' \in A$$ with $$\phi(u^') =0$$ 
<hr width="50%">

**Definition (3 -Nilpotence)** \\
Let algebra $$(A,*)$$ be associative -or- commutative -or- both. Then $$a \in A$$ is called 3-nilpotent if $$a^2 \neq 0$$ but $$a^3 = 0$$

***Example (3-Nilpotent)*** \\
Take $$(M(3, \mathbb{R}), \cdot)$$ and $$a =  \begin{pmatrix}0 & 1 & 0\\\ 0 & 0 & 1\\\ 0 & 0 & 0\end{pmatrix}$$

**Definition (Zero-divisors)** \\
If $$(A,*)$$ is a K-algebra, then $$x \in A, x \neq 0$$ is called a zero-divisor if $$\exist y \in A, y \neq 0$$ such that $$x*y=0$$

***Remark*** \\
Any 2-nilpotent element, $$x$$, is a zero-divisor of itself.

In order to embark on the perilous, crucial passage from algebra theory to their application in the study of dynamical systems we will have to discuss special classes of algebra. The first of which is the *division algebra*
**Definition (Division-algebra)** \\
$$(A,*)$$ is called a division algebra if it does not admit zero-divisors.

***Examples (Division-algebras)*** \\
1. $$\mathbb{C}$$ is a division algebra
2. $$\bar{\mathbb{C}}$$ is a division algebra
3. $$\mathbb{R} \bigoplus \mathbb{R}$$ is not a division algebra, take for instance $$(1,0)*(0,1) = (0,0)$$

The next special classes of algebra are so-called regular and singular algebras.
**Definition (Regular-algebra)** \\
$$(A,*)$$ is called a regular algebra if $$\exists x \in A$$ such that $$J_A(x)$$ is invertible.

**Definition (Singular-algebra)** \\
On the other hand, we call an algebra $$(A,*)$$ singular if $$\forall x \in A$$ the matrix $$J_A(x)$$ is singular.

***Remark*** \\
We will see that the norm is an important tool for regular algebras and not so for singular algebras.

**Proposition** \\
Suppose $$(A,*)$ is singular, then every element $$x\in A$$ is a zero-divisor.

***Proof*** \\
Take $$(A,*)$$ singular, and  $$x \in A$$ then $$J_A(x)$$ is, in particular, singular. As a singular matrix, $$J_A(x)$$, has a nontrivial kernel in $$A$$ i.e. $$\exists y \neq 0 \in A$$ with $$J_A(x)y = x * y = 0$$ hence, $$x$$ is a zero divisor.

**Theorem (Classification of Commutative 2-dimensional Algebras)** \\
All 2-dimensional commutative algebras are completely described, up to isomorphism, with six classes. They are distinguished by 2 invariants: number of idempotents, number of 2-nilpotents

**Definition (Rank 3-algebra)** \\
A real commutative algebra $$(A,*)$$ is called rank-3 if $$x^3 = \gamma_1(x) x^2 - \gamma_2(x) x$$

***Remark*** \\
Recall that, in linear algebra, the rank of a matrix is the dimension of the vector space spanned by its columns.

**Theorem (First Main Theorem)** \\
Let $$(A,*)$$ be a real commutative 2-dimensional rank-3 algebra, then:
1. Regular algebra A is a division algebra iff the norm is uniformly positive definite or uniformly negative definite i.e. iff $$\gamma_2(x) > 0 \forall x \neq 0 \in A$$ or  $$\gamma_2(x) < 0 \forall x \neq 0 \in A$$
2. Regular algebra A, admits a basis of zero-divisors iff the norm is indefinite i.e. iff $$\exists x,y \neq 0$$ such that $$\gamma_2(x) > 0$$ and $$\gamma_2(y) < 0$$
3. A admits a 2-nilpotent elelment iff the norm is uniformly positive semi-definite or uniformly negative semi-definite i.e. iff $$ \gamma_2(x) \geq 0 \forall x \in A$$ and $$\exists y \neq 0$$ with $$ \gamma_2(y) = 0$$ or $\gamma_2(x) \leq 0 \forall x \in A$$ and $$\exists y \neq 0$$ with $$ \gamma_2(y) = 0$$
4. A is singular iff the norm is identically zero i.e. iff $$\gamma_2(x) \equiv 0$$

***Proof (Coordinate Based)*** \\
$$(1)$$ *A is a division algebra $$\iff$$ $$\gamma_2(x)$$ is positive or negative definite.*

We will need the following lemma: \\
*Lemma A:* Let $$e_1, e_2$$ be a basis in $$A$$ inducing the following multiplication table $$\begin{pmatrix}a_1 & a_2 & a_3\\\ b_1 & b_2 & b_3\end{pmatrix}$$ such that 

$$ 

$$
