---
{"dg-publish":true,"permalink":"/math/number-theory/euclid-s-theorem/"}
---


#Math/Arithmetic 
#Math/NumberTheory 

Euclid's theorem states that there are infinitely many prime numbers was first offered by Euclid in ancient Greece. Below is the proof that there are infinitely many primes, using a method known as *proof by contradiction*:

Let's assume that there are a finite number of primes. Let $P$ represent the set of all primes such that:
$$
P=\{p_1,p_2,p_3,...,p_n\}=\{2,3,5,...,p_n\}
$$
Let $Q$ equal the product of all the primes + 1
$$
\begin{align}
Q= 2 \times 3 \times 5 \times 7 \times ... \times p_n+1\\\\
\end{align}
$$
According to the [[Math/Number Theory/Fundamental Theorem of Arithmetic\|fundamental theorem of arithmetic]], every number number greater than $1$ can be factored into a unique product of primes. 
1. $Q$ is not divisible by any of the primes from $2$ to $p_n$ since dividing $Q$ by any of them gives a remainder of $1$. 
2. Therefore, $Q$ must be prime. 
3. However, $Q$ is not part of set $P$, contradicting our earlier assumption that there is a finite number of primes that were all contained in $P$. 
4. Given this contradiction, our assumption that there are finite primes is wrong. Therefore, there must be infinite primes.

