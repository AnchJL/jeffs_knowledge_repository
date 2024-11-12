---
{"dg-publish":true,"permalink":"/Math/Algebra/Proof that Square Root 2 is Irrational/","created":"2024-10-09T01:02:01.119-04:00","updated":"2024-11-11T21:46:44.534-05:00"}
---

#Math/Algebra 

The method below uses [[proof by contradiction\|proof by contradiction]] to show that $\sqrt{2}$ is irrational.

First, assume that $\sqrt{2}$ is rational. This means we can express $\sqrt{2}$ as:
$$
\begin{align}
\sqrt{2}=\frac{a}{b}\\\\
\end{align}
$$
Where $a$ and $b$ are integers, and $\frac{a}{b}$ is a fraction in its simplest form and therefore cannot be further reduced.
$$
\begin{align}
&\sqrt{2}\cdot b=a&\text{Multiply both sides by $b$.}\\\\
&2b^2=a^2&\text{Square both sides.}

\end{align}
$$
Note that $a^2$ and $b^2$ are also integers since the product of two integers is another integer. We know that $a^2$ is even since it is divisible by two. Since $a^2$ is even, a cannot be odd because the product of two odd numbers is itself an odd number. Therefore $a$ must be an even because the product of two even numbers is even. Given that $a$ is even, there is some integer $k$ in which $a=2k$.

$$
\begin{align}
&2b^2=(2k)^2\\\\
&2b^2=4k^2\\\\
&b^2=2k^2&\text{Divide both sides by 2.}\\\\
\end{align}
$$
Since $b^2$ is twice of $k^2$, then that means $b^2$ is also even.

However, if both $a^2$ and $b^2$ are even, then that means $\frac{a}{b}$ can be further reduced by dividing both the numerator and denominator by $2$. This contradicts the earlier assumption that $\sqrt{2}$ is equal to the irreducible fraction $\frac{a}{b}$.

Therefore, $\sqrt{2}$ is cannot be rational.

