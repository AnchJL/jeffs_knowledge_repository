---
{"dg-publish":true,"permalink":"/math/number-theory/divisibility/"}
---

#Math/NumberTheory 

Given two integers, $a$ and $b$, where $a \neq 0$, we write $a|b$ to say that $a$ [[Math/Arithmetic/Division\|divides]] $b$ if $b=am$ for some integer of $m$. In other words, $a$ divides $b$ without leaving behind a remainder.

Example:
- $2|8 \text{ because } 8=2 \cdot 4$

## Properties of divisibility:

### If $a|b$ and $b|c$ then $a|c$

This is known as the transitive property of divisibility
**Proof:**
1. If $a|b$ then $b=am$ for some integer $m$.
2. If $b|c$ then $c=bn$  for some integer $n$
3. From (1) and (2), $c=amn$
4. Since $m$ and $n$ are integers, their product is an integer. Therefore, let integer $m'=mn$
5. From (3) and (4), $c=am'$.
6. $\therefore c$ is divisible by $a$ (or $a|c$)

### If $a|b$ then $ca|cb$

**Proof**:
1. If $a|b$ then $b=am$ for some integer $m$
2. Multiply both sides by integer $c$ such that: $cb=cam$
3. Notice that $cb=(ca) \cdot m$ means that $cb$ divided by $ca$ equals integer $m$.
4. $\therefore ca|cb$
### If $a|b$ and $a|c$ then for all integers of x and y (i.e. $x,y\in \mathbb{Z}$), $a|(bx+cy)$

**Proof**:
1. If $a|b$ then $b=am$ for some integer $m$
2. If $a|c$ then $c=an$  for some integer $n$
3. From (1), $bx=amx$
4. From (2), $cy=any$
5. Since the product of two integers is another integer, let integer $m'=mx$ and integer $n'=ny$
6. From (3), (4), and (5)
	(i) $bx=am'$
	(ii) $cy=an'$
7. Hence, $a|bx$ and $a|cy$
8. Add the equations (i) and (ii) together: $bx+cy=am'+an'$
9. Factor out $a$: $bx+cy=a(m'+n')$
10. Since the sum of two integers is another integer, let $l=m'+n'$
11. From (9) and (10), $bx+cy=al$
12. $\therefore a|(bx+cy)$

### If $a|1$ then $a=\pm 1$

Although this may seem obvious and intuitive, we can still write a mathematically rigorous proof for this claim.

**Proof**:
1. Suppose $a|1$.  Then that means $1=am$ for some integer of $m$.
2.  From (1), 1=|a||m|
3. From (2), $1 \leq |a|$ because $a$ represents any arbitrary integer and the absolute value of any arbitrary integer has to be greater than 1, which is the smallest positive integer.
4. We can also deduce from (2) that $\frac{1}{|m|} \leq 1$ using the same logic used in step (3)
5. From (2), $|a|=\frac{1}{|m|}$
6. From (3), (4), and (5), we obtain the following: $1 \leq (|a|=\frac{1}{|m|}) \leq 1$
7. $\because 1 \leq |a| \leq 1$
8. $\therefore$ The only possible value for $|a|$ is 1, and so $a=\pm1$

