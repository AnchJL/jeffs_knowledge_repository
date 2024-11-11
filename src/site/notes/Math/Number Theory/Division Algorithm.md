---
{"dg-publish":true,"permalink":"/math/number-theory/division-algorithm/"}
---


#Math/NumberTheory 

The division algorithm is technically not an algorithm; it is a theorem that states for integers $a$ and $b$ (where $b > 0$), there are unique integers $q$ and $r$ such that:
$$
\begin{align}
&a=bq+r\\\\
&\text{Where }0\leq r <b
\end{align}
$$
Note that $q$ is the quotient and $r$ is the remainder.

**Example 1**:

Consider the integers $a=21$ and $b=2$
$$
\begin{align}
a=bq+r \Rightarrow 21=2q+r\\\\
q=10\\\\
r=1
\end{align}
$$

**Example 2**:

Consider the integers $a=35$ and $b=6$
$$
\begin{align}
a=bq+r \Rightarrow 35=6q+r\\\\
q=5\\\\
r=5
\end{align}
$$
## Proof of Theorem

Consider the following set $S=\{a-bx|x\in \mathbb{Z},a-bx\geq0\}$

Example: $a=12$ and $b=5$

| x     | a-bx (i.e. 12-5x) |
| ----- | ----------------- |
| -2    | 22                |
| -1    | 17                |
| 0     | 12                |
| 1     | 7                 |
| 2     | 2                 |
| ~~3~~ | ~~-3~~            |
Notice that $x$ is the quotient and $a-bx$ is the remainder. Any negative remainders are not considered as part of the set because it violates the condition that $a-bx\geq0$. Therefore, values of $a-bx$ where $x\geq0$ are not part of $S$.

In this case, $S=\{2,7,12,17 ...\}$, where each element are the remainders for various values of $x$.

It may be important to look at the smallest element in the set $S$. So it will have a minimum as long as $S$ is not an empty set. If $S$ is empty, then there can be no minimum element; so $S$ cannot be empty.

Claim: $S \not= \not O$ in the following cases:
- Case 1: $a\geq0$ (x=0)
	- $a-b(0)=a \in S$
- Case 2: $a<0$ set $x=a$
	- a-ba=a(1-b)
	- Notice that $a$ is negative and $(1-b)$ is negative because we specified that $b$ is an integer greater than $0$, meaning that $b$ is an integer that is greater than or equal to 1.
	- Therefore, $a(1-b)$ is positive and must be greater than 0
	- Therefore, $a-ba \in S$
## Proof that the smallest element of $S$ must be smaller than $b$

Let $r=\min(S)$ and q be the corresponding x-value
- Now we need to show that $0\leq r<b$
- $r=a-bq\Rightarrow a=bq+r$
- We can show that r is in the acceptable range by using proof by contradiction.
- Suppose that $r\geq b$, contrary to our initial condition.
- This means that $r=a-bq \geq b$
	- $(r-b=a-bq-b)\geq (b-b = 0)$
	- $r-b \in S$ but $r-b\leq r$. This means we have found an element of $S$ that is smaller than the minimum element of $S$, which is not possible.
	- Therefore, we have a contradiction. Therefore, the smallest range element of $S$ must be smaller than $b$

## Proof of the Uniqueness of $r$ and $q$

1. Suppose that $q,q',r,r'$ are such that $a=bq+r=bq'+r'$. Assume $r'\geq r$. If the quotient and remainder are not unique, then $q$ and $r$ should be different from their $q'$ and $r'$ counterparts.
2. From (1), rearrange the equation to get: $bq-bq'=r'-r$
3. Factor out $b$ from $b(q-q')=r'-r$
	- Note that the left hand side is a multiple of $b$
	- Note that the right hand side $0\leq r'-r <b$ (because both $r$ and $r'$ must be smaller than $b$)
	- The only way this is possible is if LHS=RHS=0 because $0$ is the only multiple of $b$ that is less than $b$
4. $\because r'-r=0 \ \therefore r'=r$
5. $\because b(q'-q)=0 \ \therefore q'=q$
6. $\because r$ and $q$ are not different from $r'$ and $q'$ $\therefore$ there is a unique remainder and quotient for the equation $a=bq+r$, thus proving the division algorithm.
