---
title: "Math 3140 Notes"
author: "Frank Ma"
date: "2025-09-09"
toc: true
header-includes:
  - \usepackage[margin=1in]{geometry}
  - \fontsize{12}{14}\selectfont
  - \usepackage{xcolor}
---

<!-- # Class 3 -->

## Subspaces 

```{=latex}
\begin{center}
\fcolorbox{gray}{gray!10}{\parbox{0.97\linewidth}{%
```
**Proposition (Subspace Test):** Let $V$ be a vector space over $F$, $W \subseteq V$, then $W \leq V$ if and only if 
1. $W$ is non-empty
2. $W$ is closed under addition
3. $W$ is closed under scalar multiplication
```{=latex}
}}
\end{center}
```

**Proof** 

($\implies$):  If $W \leq V$, then $0_V \in W$ hence $W \neq \emptyset$. 2 and 3 are true so that $+$ and $\cdot$ are well defined.

($\impliedby$): Assume $1, 2, 3$, take $w \in W$ arbitrary. By 3, $-1 \cdot w = -w \in W$. By 2, $-w + w = 0 \in W$. 

By 2 and 3, $+$ and $\cdot$ are well defined in $W$. All other properties are true because they are true in $V$. 

## Intersections of subspaces and spans

```{=latex}
\begin{center}
\fcolorbox{gray}{gray!10}{\parbox{0.97\linewidth}{%
```
**Theorem (Intersection of subspaces):** Let $\{ w_i \}_{i \in I} $ be a collection of subspaces in $V$. Then 
$$
  W = \bigcap_{i \in I}W_i 
$$
is a subspace of $V$. 

*The intersection of arbitrarily many subspaces of $V$ is a subspace of $V$*
```{=latex}
}}
\end{center}
```

**Proof**: 

1) Since $0 \in w_i$ for all $i$, $0 \in W$
2) Take $u, v \in W$ arbitrary
$$
\begin{align*}
    u, v \in W &\implies u, v \in W_i \text{ for all } i \\
    &\implies u + v \in W_i \text{ for all } i \\
    &\implies u + v \in W
\end{align*}
$$
3) Take $u \in W$, $a \in F$ arbitrary, 
$$
\begin{align*}
    u \in W & \implies u \in W_i  \text{ for all } i \\
    & \implies au \in W_i  \text{ for all } i \\
    & \implies au \in W
\end{align*}
$$

```{=latex}
\begin{center}
\fcolorbox{gray}{gray!10}{\parbox{0.97\linewidth}{%
```
**Definition (Span):** Let $V$ be a vector space over $F$, $S \subseteq V$, the span of $S$ is defined by 
$$
  <S> = \bigcap_{S \subseteq W \leq V} W
$$

*The span of a set $S$ is the intersection of all subspaces in $V$ containing the set $S$*
```{=latex}
}}
\end{center}
```

**Note**
- by intersection of subspaces theorem, the span is a subspace, $<S>\ \leq V$, 
- when $<S> = V$, $S$ is called a **generating set** for $V$
- If there exists $S \subseteq V$, $<S> = V$, and $S$ is finite, then $V$ is **finitely generated**
- $<S>$ is also denoted $span(S)$

```{=latex}
\begin{center}
\fcolorbox{gray}{gray!10}{\parbox{0.97\linewidth}{%
```
**Definition (Linear Combination):** Let $S$ be a subset of $V$, a vector space over $F$. A linear combination of elements of $S$ is an element $v \in V$ that can be written as 
$$
  v = \sum_{i = 1}^{k} a_i s_i  
$$
for some $s_i \in S, a_i \in F, k \in \mathbb{N}$

*A linear combination of elements of $S$ is a finite sum of elements of $S$*
```{=latex}
}}
\end{center}
```

```{=latex}
\begin{center}
\fcolorbox{gray}{gray!10}{\parbox{0.97\linewidth}{%
```
**Theorem (Span and Linear Combination):** Let $V$ be a subspace over $F$ and $S$ a subset of $V$, $S \neq \emptyset$, then 

$$
  <S> = span(S) = \{ \sum_{i = 1}^{k}a_i s_i: a_i \in F, s_i \in S, k \in \mathbb{N} \} 
$$
```{=latex}
}}
\end{center}
```

**Proof**: let $L = \{ \sum_{i = 1}^k a_i s_i: a_i \in F, s_i \in S, k \in \mathbb{N} \} $.  We want to show that $L = <S>$

($L \subseteq <S>$): 

$S \subseteq <S>$ by definition. Since $S$  is closed under addition and scalar multiplication, and $\sum a_i s_i \in <S>$ . Hence $L \subseteq <S>$. 

($<S> \subseteq L$):

We show that $L$ is a subspace that contains $S$. Since $<S>$ is the intersection of all subspaces that contain $S$, $<S>$ is a subset of $L$.

$S \subseteq L$ since for any $s \in S$, $s = 1 \cdot s \in L$. 

We then show that $L$ is a subspace.
 - Existence of $0$: take all $a_i = 0$ in $\sum a_i s_i$,
 - Closure under addition: for any $\sum_{i = 1}^k a_i s_i, \sum_{i = 1}^l b_i t_i \in L$, their sum is still a linear combination of $S$
 - Closure under scalar multiplication
$$
   a \left( \sum_{i = 1}^k b_i s_i \right) = \sum_{i = 1}^k (ab_i) s_i
$$
 

Hence 
$$
  <S> = \bigcap_{S \subseteq W \leq V} W \subseteq L
$$

## Sums of subspaces

```{=latex}
\begin{center}
\fcolorbox{gray}{gray!10}{\parbox{0.97\linewidth}{%
```
**Definition (Sum of subspace):** Let $W_i$ be a set where each $W_i$ is a subspace of $V$ for all $i \in I$ 

The sum of $W_i$ is defined as 
$$
  \sum_{i \in I} W_i = <\bigcup_{i = I} W_i>
$$

*The sum of $W_i$ is the span of the union of $W_i$*. 

*The sum of $W_i$ is the set of all linear combinations of elements in the union of $W_i$. 
```{=latex}
}}
\end{center}
```

```{=latex}
\begin{center}
\fcolorbox{gray}{gray!10}{\parbox{0.97\linewidth}{%
```
**Proposition (Sum of subspaces as finite sums):** Let $W_i \leq V$ for all $i \in I$, then $w \in \sum_{i = I} W_i \iff $ there exists a finite subset $J \subseteq I$ and $w_i \in W_i$ so that 
$$
  w = \sum_{i \in J} w_i
$$

*The subspace spanned by $\bigcup_{i \in I} W_i$ is the set of finite sums of elements of $W_i$.*
```{=latex}
}}
\end{center}
```

**Note** The union of subspaces is not necessarily a subspace. 
$$
  span(e_1) \cup span(e_2) = \text{ union of two lines } \rightarrow \text{ not a subspace}
$$

However, 
$$
  span(
    span(e_1) \cup span(e_2) 
  ) \leq V
$$

**Proof** 

Define 
$$
  W = \{ w \in V \text{ s.t. } w = \sum_{i \in J} W_i \text{ for } J \subseteq I, J \text{ finite} \} 
$$

**WTS**: $W = \sum_{i \in J} W_i = < \bigcup_{i \in I} W_i> $

**Claim 1**: $W$ is a subspace of $V$

**Claim 2**: $\bigcup_{i \in I} W_i$ is a subset of $W$

**Claim 3**: $W \subset span \left( \bigcup_{i \in I} W_i \right) $ because any $w \in W$ is a linear combination of elements of $\bigcup_{i \in I} W_i $

Hence 
$$
  \bigcup_{i \in I}W_i \subseteq W \subseteq span \left( \bigcup_{i \in I} W_i \right) 
$$

Also $\text{span} \left( \bigcup_{i \in I} W_i \right)$ is the smallest subset containing $\bigcup_{i \in I} W_i$, hence 
$$
  span \left( \bigcup_{i \in I} W_i  \right)  \subseteq W
$$

Hence
$$
  W = span \left(   \bigcup_{i \in I}W_i \right)
$$




