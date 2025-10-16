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

<!-- # Class 1 -->

## Fields

```{=latex}
\begin{center}
\fcolorbox{gray}{gray!10}{\parbox{0.97\linewidth}{%
```
**Definition (field):** A **field** $F$ is a set with two binary operations

$$
+: F \times F \to F,\ (x, y) \mapsto x + y
$$
$$
\cdot: F \times F \to F,\ (x, y) \mapsto x \cdot y
$$

that satisfy these properties:

- (A0) existence of additive identity or neutral element: there is $0 \in F$ such that $x + 0 = x$ for all $x \in F$
- (A1) additive commutativity: for all $x, y \in F$, $x + y = y + x$
- (A2) additive associativity: for all $x, y, z \in F$, $x + (y + z) = (x + y) + z$
- (A3) existence of additive inverse: for all $x \in F$ there is $y$ such that $x + y = 0$
- (M0) existence of multiplicative identity or neutral element: there is $1 \in F, 1 \neq 0$ such that $x \cdot 1 = 1 \cdot x = x$ for all $x$
- (M1) multiplicative commutativity: for all $x, y \in F$, $x \cdot y = y \cdot x$
- (M2) multiplicative associativity: for all $x, y, z \in F$, $x \cdot (y \cdot z) = (x \cdot y) \cdot z$
- (M3) existence of multiplicative inverse: for all $x \in F, x \neq 0$ there is $y$ such that $x \cdot y = 1$
- (D) distributivity: for all $x, y, z \in F$, $(x + y) \cdot z = x \cdot z + y \cdot z$
```{=latex}
}}
\end{center}
```

**Fact:** $\{ 0 \}$ is not a field because we require that the multiplicative identity be distinct from 0. If we allowed $0 = 1$, then $F$ is the trivial field, i.e., $F = \{ 0 \}$.

**Fact:** The smallest field is $F_2 = \{ 0, 1 \}$ with addition and multiplication defined as:

Addition:

| $+$ | 0 | 1 |
|-----|---|---|
| 0   | 0 | 1 |
| 1   | 1 | 0 |

Multiplication:

| $\cdot$ | 0 | 1 |
|---------|---|---|
| 0       | 0 | 0 |
| 1       | 0 | 1 |

**Fact:** If $(F, +, \cdot)$ is a field, then $0 \cdot x = 0$ for all $x$.  
**Proof:**

$$
0 \cdot z = (0 + 0) \cdot z = 0 \cdot z + 0 \cdot z
$$
Adding the additive inverse of $0 \cdot z$ to both sides, we get
$$
0 = 0 \cdot z
$$

**Fact:** The additive and multiplicative inverses are unique.

**Proof:** Let $x \in F$, suppose $y, z$ are both additive inverses of $x$.

$$
y = y \\
y = y + 0 \\
y = y + (x + z) \\
y = (y + x) + z \\
y = z
$$

Since the additive and multiplicative inverses are unique, we denote the additive inverse and multiplicative inverse of $x$ respectively as $-x$ and $x^{-1}$.

```{=latex}
\begin{center}
\fcolorbox{gray}{gray!10}{\parbox{0.97\linewidth}{%
```

**Definition (Group):**  A set $G$ with a binary operation $*$ is a **group** if it has

- existence of inverse
- existence of identity
- associativity

```{=latex}
}}
\end{center}
```

Note that commutativity is not required. A group with commutativity is known as a **commutative group**.

```{=latex}
\begin{center}
\fcolorbox{gray}{gray!10}{\parbox{0.97\linewidth}{%
```
**Definition (Field):** $(F, +, \cdot)$ is a field if

- $(F, +)$ is a commutative group
- $(F \setminus \{ 0 \}, \cdot )$ is a commutative group
- distributive properties hold
```{=latex}
}}
\end{center}
```








