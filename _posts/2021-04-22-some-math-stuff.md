---
layout: post
title: A math problem
excerpt: An interesting math problem.
---

Here's a math problem:

> For real numbers $x$ and $y$, the following is satisfied:
>
> $$x^3 + y^3 = (x + y)^2. $$
>
> Find the range of values for $x + y$.

## Solution

To begin, let's prove that $x + y \ge 0$.

Since the right-hand side is always positive, we need $x^3 + y^3$ to be positive as well. This means we can't have both $x$ and $y$ be negative, because otherwise the left-hand side would be negative. [Without loss of generality](https://artofproblemsolving.com/wiki/index.php/Without_loss_of_generality), assume that $x \ge y$. Then, either $x$ and $y$ are both positive, or $x$ is positive and $y$ is negative.

- If the latter, then we must have $x \ge -y$; otherwise, we'd get $x^3 + y^3 < 0$. In this case, $x + y \ge 0$.
- If the former, then we get $x + y \ge 0$ anyway.

Thus, $x + y \ge 0$.

Now, let's factor the left-hand side using [sum of cubes](https://www.varsitytutors.com/hotmath/hotmath_help/topics/sum-and-difference-of-cubes):

$$
\begin{align*}
x^3 + y^3 &= (x + y)^2 \\
(x + y)(x^2 - xy + y^2) &= (x + y)^2
\end{align*}
$$

We know that $x + y = 0$ is a solution from $x = y = 0$. Thus, we'll assume $x + y \neq 0$ from here on. We divide both sides by $x + y$:

$$
\begin{align*}
x^2 - xy + y^2 &= x + y \\
x^2 + 2xy + y^2 - 3xy &= x + y \\
(x + y)^2 - (x + y) &= 3xy \\
\end{align*}
$$

Let $s = x + y$ and $p = xy$. Now we're looking for the possible range of $s$. We can't quite use [AM-GM](https://artofproblemsolving.com/wiki/index.php/Arithmetic_Mean-Geometric_Mean_Inequality) since $x$ and $y$ can be negative, but we still have $p \le s^2/4$. (The proof is almost exactly the proof for 2-variable AM-GM and is left as an exercise for the reader.)

Our equation becomes:

$$
\begin{align*}
s^2 - s &= 3p \\
\end{align*}
$$

And, using $p \le s^2/4$, we get

$$
\begin{align*}
s^2 - s \le 3s^2/4 \\
s^2/4 - s \le 0 \\
s/4 - 1 \le 0 \\
s \le 4.
\end{align*}
$$

Therefore, $s$ is nonnegative and at most 4. Now it's time to prove that all values in that range are possible.

***

This is going to be quite a bash! Given a value of $s$, we want to prove that there exists $x$ and $y$ that satisfy the equation and sum to $s$. We really only need to find a value of $x$ though, since given $s$ we have $y = s - x$. We have

$$
\begin{align*}
x^2 - xy + y^2 &= x + y \\
x^2 - x(s - x) + (s - x)^2 &= s \\
3x^2 + s^2 - 3sx - s &= 0 \\
3x^2 - (3s)x + (s^2 - s) &= 0.
\end{align*}
$$

Using the quadratic formula to solve for $x$, we get

$$
\begin{align*}
x &= \dfrac{3s \pm \sqrt{9s^2 - 4(3)(s^2 - s)}}{6} \\[0.5em]
&= \dfrac{3s \pm \sqrt{-3s^2 + 12s}}{6}.
\end{align*}
$$

The discriminant is positive only for $0 \le s \le 4$, which happens to be a range we've already restricted $s$ down to. Thus, there exist $x$ and $y$ such that $x^3 + y^3 = (x + y)^2$ and $x + y = s$ for all $0 \le s \le 4$. $\quad\blacksquare$

***

And that's it for the post! I wanted to test some MathJax with this post, and looks like it works quite well! I'll probably write some more math posts in the future.