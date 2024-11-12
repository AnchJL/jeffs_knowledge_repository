---
{"dg-publish":true,"permalink":"/Math/Algebra/Quadratic Formula/","created":"2024-10-02T01:47:14.730-04:00","updated":"2024-11-11T21:47:31.584-05:00"}
---

#Math/Algebra 

The quadratic formula is used to find the solutions/roots of a [[Math/Algebra/Quadratic Equation\|quadratic equation]]. Consider a quadratic equation in standard form below with y set to 0:

$$
ax^2+bx+c=0, \text{where a and b are coefficients and c is a constant.}
$$
The solutions for $x$ can be found using the quadratic formula below:

$$
x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}
$$
## Deriving the Quadratic Formula

Deriving the quadratic formula requires the use of a method known as [[Math/Algebra/Completing the Square\|Completing the Square]]. See below for the steps in how the quadratic formula was derived from a quadratic equation:
$$
\begin{align}
&ax^2+bx+c=0\\
\\
&x^2+\frac{b}{a}x+\frac{c}{a}=0 &\text{Divide both sides by $a$}\\
\\
&x^2+\frac{b}{a}x+(\frac{b}{2a})^2-(\frac{b}{2a})^2+\frac{c}{a}=0 &\text{Complete the square}\\
\\
&(x+\frac{b}{2a})^2=\frac{b^2}{4a^2}-\frac{c}{a}=\frac{b^2-4ac}{4a^2}\\
\\
&x+\frac{b}{2a}=\pm\sqrt{\frac{b^2-4ac}{4a^2}}=\frac{\pm\sqrt{b^2-4ac}}{2a} &\text{Take the square root of both sides}\\
\\
&x=\pm\frac{\sqrt{b^2-4ac}}{2a}-\frac{b}{2a} &\text{Solve for x}\\
\\
&x=\frac{-b\pm\sqrt{b^2-4ac}}{2a} &\text{Simplify}\\
\end{align}
$$

Note that $b^2-4ac$ is known as the *discriminant*. The types of solutions to a quadratic equation depend on the value of the discriminant.

| Value of Discriminant | Type of Solution          |
| --------------------- | ------------------------- |
| $b^2-4ac>0$           | Two real solutions        |
| $b^2-4ac=0$           | Exactly one real solution |
| $b^2-4ac<0$           | Imaginary solutions       |
