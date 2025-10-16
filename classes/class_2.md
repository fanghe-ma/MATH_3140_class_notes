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

<!-- # Class 2 -->

## Vector Spaces

```{=latex}
\begin{center}
\fcolorbox{gray}{gray!10}{\parbox{0.97\linewidth}{%
```
**Definition (Vector space):** A vector space over a field $F$, denoted $V$, is a set with two operations
- $+: V \times V \to V, (u, v) \mapsto u + v$
- $\cdot: V \times V \to V, (u, v) \mapsto u \cdot v$

such that
- (V): $(V, +)$ is a commutative group
- (SM1): $a \cdot (v + w) = a\cdot v + a \cdot w$ for all $a \in F, v, w \in V$
- (SM2): $ (a + b) \cdot v = a\cdot v + b \cdot v$ for all $a, b \in F, v \in V$
- (SM3): $(a \cdot b) \cdot v = a \cdot (b \cdot v)$ for all $a, b \in F, v \in V$
- (SM4): $1 \cdot v = v$ for all $v \in V$
```{=latex}
}}
\end{center}
```

If $V$ is a vector space, we refer to elements of $V$ as vectors. As a corollary to the above axioms, we have the following properties:
- $0 \cdot v = \mathbf{0}$ for $0 \in F$, all $v \in V$
- $a \cdot \mathbf{0} = \mathbf{0}$ for all $a \in F$
- The additive inverse of $v$ is unique and denoted $-v$
- Subtraction is defined as $v - w := v + (-w)$ for all $v, w \in V$
- For all $v \in V$, $ (-1) \cdot v = -v$
    - Proof: $\mathbf{0} = 0 \cdot v = (1 + (-1)) \cdot v = v + (-1) \cdot v$

## Subspaces

```{=latex}
\begin{center}
\fcolorbox{gray}{gray!10}{\parbox{0.97\linewidth}{%
```
**Definition (Subspace):** Let $(V, +)$ be a vector space over $F$, a subset $U \subseteq V$ is a subspace if $U$ is a vector space, denoted
$$
  U \leq V
$$
```{=latex}
}}
\end{center}
```

**Note:** If $W \leq V$, $0_W = 0_V$.

**Proof:**
$$
\begin{aligned}
0_W &= 0_W + 0_V \\
&= 0_W + 0_V + (-0_W) \\
&= 0_V
\end{aligned}
$$