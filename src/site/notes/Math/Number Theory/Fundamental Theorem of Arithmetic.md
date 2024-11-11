---
{"dg-publish":true,"permalink":"/math/number-theory/fundamental-theorem-of-arithmetic/"}
---


#Math/Arithmetic 
#Math/NumberTheory 

The *Fundamental Theorem of Arithmetic*, (aka the *prime factorization theorem*) every positive integer greater than $1$ can be factored into a *unique* product of [[Math/Number Theory/Prime Numbers\|primes]].

To see what is meant by unique, consider $60$ as an example number. The primes that multiply together to make up $60$ are: 
$$
2 \times 2 \times 3 \times 5=2^2\times 3^1 \times 5^1
$$
The above combination of primes and exponents is the only combination that can form a product of $60$.

## Lemma 1:

Consider the integers $a$ and $b$, and the prime number $p$. If $p|ab$ then either $p|a$ or $p|b$.

Proof:
1. Suppose that $p\not{|}a$, then [[Math/Number Theory/Greatest Common Divisor\|greatest common divisor]] of $a$ and $p$ is 1.
2. From (1), there exists integers $x$ and $y$ such that $ax+by=1$
3. $\because p|ab$ $\therefore$there is an integer d such that $pd=ab$
4. From (2), notice that $b(ax+py)=b$ because $ax+py=1$
5. $(ab)x+p(by)=b$
6. Substitute $pd=ab$ from (3) into (5): $$pdx+pby=b$$
7. Factor out $p$: $$p(dx+by)=b$$
8. Since all the terms are integers, (7) shows that b is multiple of p, meaning that $b$ is divisible by $p$.

## Lemma 2

Lemma 2 is an extension of lemma 1. According to lemma 2, if prime number $p|(a_1\times a2\times...a_n)$ then $p|a_i$ where $1\leq i\leq n$.

### Proof by induction:

Base Case $n=2$:
1. By lemma 1, if $p|a_1a_2$ then $p|a1$ or $p|a2$
2. Our **induction hypothesis**: suppose that if $p|a1...a_k$ then $p|a_i$ for some $1\leq i\leq k$
3. **Induction Step**: Suppose that $p|a_i...a_ka_{k+1}$ i.e. $p|(a_1...a_k)a_{k+1}$
4. By lemma 1, we know that that $p|a_1...a_k$ or $p|a_{k+1}$. We can apply this step recursively for different quantities of $a$
5. By the induction hypothesis, we know $p|a_i$ for $1\leq i\leq k$ or $p|a_{k+1}$.
6. $\therefore p|a_i$ for some $1\leq i\leq k+1$

## Proof of the Theorem

Theorem: for any integer $n\geq2$, we can write $$n=p^{a_1}_1p^{a_2}_2...p^{a_k}_k$$
Where $p_i$ are distinct primes and the product for $n$ is unique up to reordering (i.e. the orders of the factors do not matter).

Proof by contradiction:
1. Suppose there is a natural number that cannot be represented as a product of primes.
2. If such natural numbers exist, then that means there is a smallest natural number without prime factorization. Let $m$ represent that smallest natural number.
3. Then that means that $m$ is a composite number, otherwise, it is already in the form $p_i^{a_i}$
4. Since $m$ is composite, then $m=ab$ where $1\leq a,b \leq m$
5. Since $a$ and $b$ are smaller than $m$ and $m$ is the smallest number without prime representation, then we can conclude that $a$ and $b$ have a prime factorization.
6. However, if $a$ and $b$ can be represented as a product of primes then so can $ab$ since $ab$ equals the prime factors of $a$ multiplied by the prime factors of $b$
7. $\because ab$ has a prime representation
8. $\therefore m$ has a prime representation, which contradicts our earlier supposition that $m$ does not have a prime representation.

Proof that $n$ has a *unique* prime representation:
1. Suppose $$p_1^{a_1}p_2^{a_2} ...P_k^{a_k}=q_1^{b_1}q_2^{b_2} ...q_m^{b_m}$$
2. Notice that $p_i$ divides the left side of (1), for all possible values of i. This also means that $p_1$ also divides the right side of (1) for all possible values of i.
3. This means that $p_i|q_r^{b}$ for some remainder $r$.
4. That also means that $p_i^i=q_r^{br}$ for each value of $p$ and $q$ for some $r$, because the only way a prime can divide another prime is if they were both the same number (in which case, their greatest common divisor would be 1).