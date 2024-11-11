---
{"dg-publish":true,"permalink":"/math/number-theory/solving-linear-congruences/"}
---


#Math/NumberTheory 

You can solve a linear [[Math/Number Theory/Congruence Relation\|congruence]] $ax\equiv b\pmod{n}$ if and only if GCD$(a,n)|b$, that is to say when $b$ is a multiple of the greatest common divisor of $a$ and $n$.
## Proof

Since the above is an *if and only if* statement, we have to prove the above proposition in the *forwards* and *backwards* direction.

**Forwards Direction**:
Suppose $x_0$ is a solution.
1. $ax_0\equiv b\pmod{n}$
2. $n|ax_0-b$
3. $ax_0-b=nk$ for some integer $k$
4. $b=ax_0-nk$
5. Notice that (4) is an integer linear combination of $a$ and $n$:
$$
b=ax_0+n(-k)
$$
6. Notice that all linear combinations of $a$ and $n$ are a multiple of GCD($a,n$) (see the [[Math/Number Theory/Euclidean Algorithm#Extended Euclidean Algorithm\|extended Euclidean algorithm]] for why).
7. $b=l\text{GCD}(a,n)$
8. $\therefore \text{GCD}(a,n)|b$

**Backwards Direction**:
1. Given GCD$(a,n)|b$ then that means $b=\text{GCD}(a,n)\cdot m$ for some integer $m$
2. GCD$(a,n)=ay+nz$ for integers $y$ and $z$ (see the [[Math/Number Theory/Euclidean Algorithm#Extended Euclidean Algorithm\|extended Euclidean algorithm]] for proof of this)
3. $b=(ay+nz)m=a(ym)+n(zm)$
5. $b-a(ym)=n(zm)$
6. From (5), $a(ym)\equiv b \pmod{n}$
7. From (6), it can be seen that $ym$ is a solution to the linear congruence $ax\equiv b\pmod{n}$

**Example 1**: Consider $4x\equiv3\pmod{18}$
$$
\begin{align}
\text{GCD}(4,18)=2 \not{|}3\\\\
\therefore\text{There is no solution}
\end{align}
$$
**Example 2**: Consider $4x\equiv6\pmod{18}$
$$
\begin{align}
&\text{GCD}(4,18)=2|6\\\\
&\therefore\text{There is a solution}\\\\
&4x=18k+6&k\in\mathbb{Z}\\\\
&k=0 \rightarrow4x=0+6=6\rightarrow x=\frac{3}{2}&\times\\\\
&k=1 \rightarrow4x=18+6=24\rightarrow x=6&\checkmark\\\\
&k=2 \rightarrow4x=36+6=42\rightarrow x=\frac{3}{2}&\times\\\\
&k=3 \rightarrow4x=54+6=60\rightarrow x=15&\checkmark\\\\
&\therefore \text{We found two solutions above: }\\\\
&x\equiv6\pmod{18}\text\:{ and }\:x\equiv15\pmod{18}
\end{align}
$$
## Strategy for Solving $ax\equiv b\pmod{n}$

1. $a$ is invertible modulo $n$ if andonly if GCD($a$,$n$)=1
	- $ax+ny=1$
	- $x$ is the inverse of $a$ (or $a^{-1}$)
	- $ax\equiv1\pmod{n}$
2. $ca\equiv cb\pmod{n}\leftrightarrow a\equiv b\pmod{\frac{n}{\text{GCD}(c,n)}}$
3. $ax\equiv b\pmod{n}$ has a solution if and only if GCD$(a,n)|b$
4. If $ax\equiv b\pmod{n}$ has a solution, then there are GCD($a,n$) solutions separated by $\frac{n}{\text{GCD}(a,n)}$

**Example**: Solve $12x\equiv16\pmod{32}$

1. $\because$ GCD$(12,32)=4$ and $4|16$
2. $\therefore$ There is GCD$(12,32)=4$ solutions, each with a distance of $\frac{32}{4}=8$ apart from each other
3. Factor out the 4: $4(3x)\equiv4*4\pmod{32}$
4. $3x\equiv4\pmod{8}$
5. Notice that 3 is relatively prime with 8 (i.e. their GCD=1). This means that 3 has an inverse modulo 8.
6. We can use the [[Math/Number Theory/Euclidean Algorithm#Extended Euclidean Algorithm\|extended Euclidean algorithm]] to solve for (4):
	7. $3x+8y=4$
	8. 8=3(2)+2
	9. 3=2(1)+1
	10. 2=1(2)+0
	11. Since 1 is the final non-zero remainder, GCD(8,3)=1
	12. From (8), 2=8(1)+3(-2)
	13. From (9), 1=3+2(-1)
	14. Substitute (8) into (9): 1=3+(8(1)+3(-2))(-1)
	15. 1=3+8(-1)+3(2)=3(3)+8(-1)
	16. Multiply both sides by 4: $4=3(12)+8(-4)=3x+8y$
	17. $\therefore x=12$
18. From (17), we can say $x\equiv12\pmod{8}$ which is congruent to $x\equiv4\pmod{8}$
19. From (18) and (2), we would obtain the four solutions for $x$ below:
	- $x\equiv4\pmod{32}$
	- $x\equiv12\pmod{32}$
	- $x\equiv20\pmod{32}$
	- $x\equiv28\pmod{32}$
Check:
$$
\begin{align}
&12(4)\pmod{32}=48\pmod{32}=16&\checkmark\\
&12(12)\pmod{32}=144\pmod{32}=16&\checkmark\\
&12(20)\pmod{32}=224\pmod{32}=16&\checkmark\\
&12(28)\pmod{32}=336\pmod{32}=16&\checkmark\\
\end{align}
$$