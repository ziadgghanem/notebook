---
layout: post
title: 'Functional Analysis'
---

## $$\Huge 1. \textstyle{Balls}$$ 
Consider a normed space $$V\textstyle{.}$$ Recall that a set $$U \subset V$$ is said to be $$\textit{open}$$ if

$$ 
\begin{eqnarray*} 

\LARGE
\forall_{ u \in U} \:
\exists_{\epsilon \geq 0} \:
\forall_{ v \in V} \:
\| u - v \| < \epsilon \Rightarrow	v \in U\\

\LARGE
\iff 
\forall_{ u \in U} \:
\exists_{\epsilon \geq 0} \:
B_{\epsilon}(u) \subset U
\end{eqnarray*} 
$$ 
{: style="text-align: center"}


Where $$B_{\epsilon}(u) := \{v \in V: \| u - v \| < \epsilon\}$$ is the open ball of radius $$\epsilon$$ centered at $$u$$.

We now define the algebraic sum of sets $$A,B \subset V\textstyle{,}$$  the algebraic sum of an element $$x_0 \in V$$ with the set $$A \subset V\textstyle{,}$$ and the scalar multiplication of sets in $$V\textstyle{.}$$

$$ 
\begin{eqnarray*} 

\LARGE
A + B := \{a + b: a \in A, b \in B\} \\
\LARGE
x_0 \in V \qquad x_0 + A := \{x_0 + a: a \in A\} \\
\LARGE
r \in \mathbb{R} \qquad rA := \{ra: a \in A\} 
\end{eqnarray*} 
$$ 
{: style="text-align: center"}

### $$\textbf{Proposition 1.01}$$

$$ 
\begin{eqnarray} 

\LARGE
B_{\epsilon}(x_0) = x_0 + B_{\epsilon}(0) = x_0 + \epsilon B_1(0) \tag{..1.01a} \label{1.01a} \\
\LARGE
B_{\epsilon}(x_0) + B_{\delta}(y_0) = (x_0+y_0) + (\epsilon + \delta)B_{1}(0) \tag{..1.01b} \label{1.01b}
\end{eqnarray} 
$$ 
{: style="text-align: center"}

### $$\textit{Proof}$$
$$\eqref{1.0.1a}:$$
First, we note that any open (or closed) ball, $$B{r}(z)$$, is a convex set, i.e.: $$ \forall_{ t \in [0,1]} \forall_{ x,y \in B{r}(z)} tx + (1-t)y \in B{r}(z).$$

We recall that any normed space $$(V, \|\cdot\|) $$ is a metric space $$(V,d(\cdot,\cdot)),$$ with induced metric $$d(u,v) = \|u-v\|,$$ and any metric space is a topological space $$(V, \Tau) $$


### $$\textbf{Proposition 1.02}$$

$$ 
\begin{eqnarray} 
\LARGE
\textstyle{Let} (V, \|\cdot\|) \textstyle{be a normed space with topology} \tau, \textstyle{then}: \\
\LARGE
U \in \Tau \Rightarrow \forall_{ x_{0} \in V} x_{0} + U \in \Tau \tag{..1.02a} \label{1.02a} \\ 
\LARGE
U \in \Tau \Rightarrow \forall_{ r \neq 0} rU \in \Tau \tag{..1.02b} \label{1.02b} 
\end{eqnarray} 
$$ 
{: style="text-align: center"}


### $$\textit{Proof}$$
$$\eqref{1.0.2a}:$$
Let $$U \in \Tau$$ then $$\forall_{ x \in U} \exists_{\epsilon > 0} B_{\epsilon}(x) \subset U$$
So, $$\forall_{ x_{0} \in V} x_0 + B_{\epsilon}(x) \subset x_0 + U $$
By $$\label{1.01a}$$ this is equivalent to $$ B_{\epsilon}(x+x_0) \subset x_0 + U \iff x_0 + U \in \Tau$$
More generally if $$A \in V$$ then 
$$A+U = \{a+x: a \in A, x \in U \} = \cup_{a \in A} a + U \in \Tau $$