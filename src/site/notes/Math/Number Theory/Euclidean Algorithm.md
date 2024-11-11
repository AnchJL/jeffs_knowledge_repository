---
{"dg-publish":true,"permalink":"/Math/Number Theory/Euclidean Algorithm/","created":"2024-10-23T00:50:45.396-04:00","updated":"2024-11-10T21:02:21.682-05:00"}
---


#Math/NumberTheory 

The Euclidean Algorithm is the process for finding the Greatest Common Divisor (GCD), aka the Greatest Common Factor (GCF), of any pair of natural numbers.

Suppose you have two integers $a$ and $b$, where $a>b$. If we repeatedly perform the divisibility algorithm:
$$
\begin{align}
&a=bq_1+r_1\\
&b=r_1q_2+r_2\\
&r_1=r_2q_3+r_3\\
&...\\
&r_{n-3}=r_{n-2}q_{n-1}+r_{n-1}\\
&r_{n-2}=r_{n-1}q_{n}+0&\text{You eventually get a remainder of zero}\\
\end{align}
$$
The last non-zero remainder of the above is the GCD of $a$ and $b$. Because it can find the greatest common divisor of pairs of numbers, Euclid's algorithm is useful for reducing fractions to their simplest form and for solving [[Math/Number Theory/Diophantine Equations\|linear Diophantine equations]].

## Proof that you eventually get a remainder of $0$:

Notice that the sequence $\{r_1, r_2, r_3, ...\} \subset \mathbb{N}$, meaning that all the remainders are natural numbers and are decreasing. It decreases because as you keep dividing by $q_i$, then $r_i$ subsequently gets smaller and smaller. Therefore, the sequence truncates at, say $R_{n-1}$, which is the last non-zero remainder of the above process.

## Proof that $r_{n-1}|a$ and $r_{n-1}|b$

Below is the proof that $r_{n-1}$ is a common divisor of $a$ and $b$.

From the above equation $r_{n-2}=r_{n-1}q_{n}$, it can be seen that :
$$
\begin{align}
r_{n-1}|r_{n-2}
\end{align}
$$
We can also see from $r_{n-3}=r_{n-2}q_{n-1}+r_{n-1}$ that $r_{n-1}$ divides both terms on the right hand side, then that means:
$$
r_{n-1}|r_{n-3}
$$
If we keep applying these steps recursively, we will eventually see that:
$$
\begin{align}
&r_{n-1}|(b=r_1q_2+r_2)\\\\
&r_{n-1}|(a=bq_1+r_1)\\\\
&\therefore{r_{n-1}\text{ is a common divisor of $a$ and $b$}}
\end{align}
$$
## Proof of Euclidean Algorithm

1. Suppose $d|a$ and $d|b$ (i.e. we have another common divisor of $a$ and $b$)
2. From (1), $d|(a-bq_1) \leftrightarrow d|r_1$. $d$ divides the first non-zero remainder
3. But that implies $d|(b-r_1q_2)\leftrightarrow d|r_2$
4. We can apply this recursively, like in the previous proof.  If we keep going, we eventually get to $d|r_{n-1}$
	- This means that the last non-zero remainder is divisible by $d$.
		- This implies that $d\leq r_{n-1}$
	- Remember that $d$ could be any arbitrary divisor of $a$ and $b$. In order for $r_{n-1}$ to be greater than $d$ and be a common divisor to $a$ and $b$, $r_{n-1}$ must be the greatest possible divisor. 
5. $\because d\leq r_{n-1}$ and $r_{n-1}|a,b$
6. $\therefore r_{n-1}=GCD(a,b)$


## Example 1:

Find the greatest common denominator of 5295 and 4321

$$
\begin{align}
&5295=4321\times1+974\\
&4321=974\times4+425\\
&974=425\times2+124\\
&425=124\times3+53\\
&124=53\times2+18\\
&53=18\times2+17\\
&18=17\times1+1\\
&17=1\times17+0\\
&\because \text{1 is the last non-zero remainder}\\
&\therefore \text{1=GCD(5295,4321)}\\\\
\end{align}
$$
Interestingly, the above calculation shows that 5295 and 4321 are relatively prime (i.e. coprime).


## Example 2:

Find the greatest common denominator of 100 and 64
$$
\begin{align}
100=64\times1+36\\
64=36\times1+28\\
36=28\times1+8\\
28=8\times3+4\\
8=4\times2+0\\
\because \text{4 is the last non-zero remainder}\\
\therefore \text{4=GCD(100,64)}
\end{align}
$$
## Extended Euclidean Algorithm

The extended Euclidean algorithm can be used to solve equations of the form
$$
ax+by=\text{GCD}(a,b)
$$
Where $a,b\in\mathbb{N}$ and $x,y\in\mathbb{Z}$. The extended Euclidean algorithm works is by using substitution for the values of $a$ and $b$ from the equations derived using Euclid's algorithm to solve for

### Example 1

Solve for $24x+9y=\text{GCD}(24,9)$

Use Euclid's algorithm:
1. $24=9*2+6$
2. $9=6*1+3$
3. $6=3*2+0$
The last non-zero remainder is 3. Therefore, 3 is the greatest common divisor of 24 and 9. Therefore.
$$
24x+9y=3
$$
4. From (1), $6=24*1-9*2$
5. From (2), $3=9*1-6*1$
6. Substitute (4) into (5): 
$$
\begin{align}
&3=9*1-(24*1-9*2)*1\\\\
&3=9*1-24*1+9*2&\text{Expand the bracket.}\\\\
&3=9*3-24*1&\text{Collect like terms.}\\\\
&3=24*(-1)+9*3=24x+9y&\text{Rearrange to match $24x+9y.$}\\\\
&\therefore x=-1 \text{ and } y=3\\\\
&\text{Check: }24*(-1)+9*3=-24+27=3
&\end{align}
$$
