---
{"dg-publish":true,"permalink":"/Math/Number Theory/Greatest Common Divisor/","created":"2024-10-26T21:52:53.560-04:00","updated":"2024-11-10T21:02:12.602-05:00"}
---


#Math/NumberTheory 

The Greatest Common Divisor (GCD), otherwise known as Greatest Common Factor (GCF), refers to the largest possible integer that [[Math/Arithmetic/Division\|divides]] two natural numbers $a$ and $b$ without leaving behind a remainder.

$$
\text{GCD}(a,b)|a \text{ and GCD}(a,b)|b
$$
Examples:

The GCD of 15 and 20 is 5.

The GCD of 49 and 21 is 7

## Finding the Greatest Common Divisor

Suppose there are two natural numbers $a$ and $b$, where $b>a$.

### Trial and Error

One method of finding the greatest common divisor is to try test out every integer $n_i\leq a$ to see determine the largest value of $n$ that divides $a$

**Example**: Find the GCD of 12 and 18
- 1|12 and 1|18
- 2|12 and 2|18
- 3|12 and 3|18
- 4|12 but not 18
- 5 does not divide 12 or 18
- 6|12 and 6|18
- 7 does not divide 12 or 18
- 8 does not divide 12 or 18
- 9 does not divide 12 but 9|18
- 10 does not divide 12 or 18
- 11 does not divide 12 or 18
- 12 does not divide 12 or 18

Looking at the list above, we can see that the largest number that divides 12 and 18 is 6. Using trial and error is thorough, but it can take a very long time to go go through every integer $n_i\leq a$.

### Prime Factorization

Another method of finding the greatest common divisor is by using [[Math/Number Theory/Fundamental Theorem of Arithmetic\|Prime Factorization]]. This method works by taking the prime factorization of $a$ and $b$, and then multiplying the factors they have in common to find the GCD.

**Example 1**: Find the GCD of 12 and 18
$$
\begin{align}
&12=2^2\times3^1=2\times2\times3\\
&18=2^1\times3^2=2\times3\times3\\
&\because \text{12 and 18 share $2^1$ and $3^1$ as common factors}\\
&\therefore \text{GCD}(12,18)=2^1\times3^1=6
\end{align}
$$
Example 2: Find the GCD of 24 and 60
$$
\begin{align}
&24=2^3\times3^1\\
&60=2^2\times3^1\times5^1\\
&\because 24 \text{ and 60 share $2^2$ and $3^1$ as common factors}\\
&\therefore \text{GCD}(24,60)=2^2\times3^1=12
\end{align}
$$
### Euclidean Algorithm

The fastest method for finding the greatest common divisor for two numbers is by using the [[Math/Number Theory/Euclidean Algorithm\|Euclidean Algorithm]].

#### Example 1: Find the GCD of 12 and 18
1. GCD(18,12)=GCD(18 mod 12, 12)=GCD(6,12)
2. GCD(12 mod 6, 6)= GCD(0,6)
3. $\therefore$ From (2), GCD(18,12)=6

Alternatively,
$$
\begin{align}
&18=12*1+6\\
&12=6*2+0\\
&\because\text{6 is the largest non-zero remainder}\\
&\therefore\text{6 is the greatest common divisor of 12 and 18}
\end{align}
$$
#### Example 2: Find the GCD of 24 and 60
1. GCD(24,60)=GCD(60 mod 24,24)=GCD(12,24)
2. GCD(24 mod 12, 12)=GCD(0,12)
3. $\therefore$From (2), GCD(24,60)=12
