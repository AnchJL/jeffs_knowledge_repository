---
{"dg-publish":true,"permalink":"/Math/Number Theory/Diophantine Equations/","created":"2024-10-26T01:51:11.955-04:00","updated":"2024-11-23T17:28:24.826-05:00"}
---


#Math/NumberTheory

Diophantine equations refer to any equation with integer coefficients and demands integer solutions.

An example of Diophantine equations includes Pythagorean triples: 
$$
\begin{align}
&a^2+b^2=c^2&a,b,c\in\mathbb{Z}
\end{align}
$$
## Linear Diophantine Equations

Question: Given the natural numbers $a$, $b$, and $c$, what integer solution for $x$ and $y$ exist such that 
$$
\begin{align}
&ax+by=c\\\\
&a,b,c\in\mathbb{N} \text{ and } x,y\in\mathbb{Z}
\end{align}
$$
Note that if $c=GCD(a,b)$ then there exists an integer solution where
$$
ax+by=\text{GCD}(a,b)
$$
See the [[Math/Number Theory/Euclidean Algorithm#Extended Euclidean Algorithm\|extended Euclidean Algorithm]] for solving equations of the form above.

In other cases...

Let $d=$GCD($a$,$b$)
$\Rightarrow d|a$ and $d|b$
$\Rightarrow d|(ax+by)$
$\Rightarrow d|c$
Given $a$, $b$, and $c$ are natural numbers, the equations $ax+by=c$ has integer solutions if and only if GCD($a$,$b$)|$c$. In other words, there is a solution if $c$ is a multiple of GCD($a$,$b$).

> [!Example] Example 1
 Solve $3x+6y=2$
> $$
> \begin{align}
> &\text{GCD}(3,6)=3\neq2\\\\
> &\because 2\neq\text{GCD}(3,6)\\\\
> &\therefore \text{There is no solution for }x,y\in\mathbb{N}
> \end{align}
> $$

## Example 2:

Solve $10x+12y=4$
$$
\begin{align}
\text{GCD}(10,12)=2\\\\
\because \text{GCD(10,12)}|4\\\\
\therefore \text{There is an integer solution for $x$ and $y$}\\\\
\end{align}
$$
To solve the above equation, you can either use the [[Math/Number Theory/Euclidean Algorithm#Extended Euclidean Algorithm\|extended Euclidean Algorithm]] or by trial and error. Let's use the extended Euclidean algorithm method:

$$
\begin{align}
&12=10*1+2\\
&10=2*5+0\\\\
&\text{Now to solve for the remainders.}\\
&2=12(1)-10(1)\\
&2=10(-1)+12(1)\\
&2*2=2[10(-1)+12(1)] &\text{Multiply both sides by 2}\\
&4=10(-2)+12(2)\\\\
&\because 4=10(-2)+12(2)\\
&\therefore x=-2 \text{ and } y=2
\end{align}
$$

