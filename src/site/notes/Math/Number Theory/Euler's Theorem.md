---
{"dg-publish":true,"permalink":"/math/number-theory/euler-s-theorem/"}
---


#Math/NumberTheory 
Euler's theorem states that if positive integers $a$ and $n$ are coprime (i.e. GCD$(a,n)=1$), then the following equation holds true:
$$
a^{\phi(n)}\equiv1\pmod{n}
$$
Where $\phi(n)$ represents [[Math/Number Theory/Euler's Totient Function\|Euler's Totient Function]]. 

## Proof of Euler's Theorem:

Let $\{b_1,b_2,...b_{\phi(n)}\}$ be a reduced residue system modulo $n$.

Lemma: $(ab_1)(ab_2)...(ab_{\phi(n)}) \equiv b_1b_2...b_{\phi(n)}\pmod{n}$


From the lemma, we get $a^{\phi(n)}b_1b_2...b_{\phi(n)} \equiv b_1b_2...b_{\phi(n)}\pmod{n}$
Let $x=b_1b_2...b_{\phi(n)}$ and substitute it into the congruence relation
$$
a^{\phi(n)}x\equiv x \pmod{n}
$$
Notice that since GCD$(x,n)=1$, then there is an inverse of $x\pmod{n}$. Let $y$ represent the inverse of $x\pmod{n}$ such that $xy\equiv1\pmod{n}$.
$$
\begin{align}
a^{\phi(n)}xy\equiv xy\pmod{n}\\\\
a^{\phi(n)}\equiv1\pmod{n}
\end{align}
$$
## Corollary: Fermat's Little Theorem

An interesting corollary of Euler's Theorem is [[Math/Number Theory/Fermat's Little Theorem (WIP)\|Fermat's Little Theorem (WIP)]] since the former is a generalization of the latter.

Let $p$ be prime and $a$ be an integer. If $p\not{|}a$ then $a^{p-1}\equiv1\pmod{p}$.

Why?
$p\not{|}a\rightarrow \text{GCD}(a,p)=1$
$\phi(p)=p-1$ because all the numbers less than a prime number are relatively prime to it.

**Example**: What are the last 2-digits of $7^{950}$?

**Solution**: Reduce $7950\pmod{100}$ to get the last 2 digits.
1. $7^{950}\pmod{4}$
2. $\phi(4)=2$ and $950=2\cdot475$
3. $\therefore 7^{950}=(7^2)^{475}=(49)^{475}$
4. $49^{475}\equiv1^{475}\pmod{4}\equiv1^{475}\pmod{4}$
5. $\phi(25)=20$ and $950=10\cdot47+10$
6. 