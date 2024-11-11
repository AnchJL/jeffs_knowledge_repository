---
{"dg-publish":true,"permalink":"/math/number-theory/modular-multiplicative-inverse/"}
---


#Math/NumberTheory 

Take three integers, $a$, $b$, and $n$. We say that $b$ is the inverse of $a$ modular $n$ when:
$$ab\equiv1\pmod{n}$$
## Proposition: an integer $a$ is invertible modular $n$ if and only if [[Math/Number Theory/Greatest Common Divisor\|GCD]]($a,n$)=1

Proof in the forward direction:
1. Suppose $a$ is invertible mod $n$.
2. There is an integer $b$ such that: $ab\equiv1\pmod{n}$
3. This means that $n|(ab-1)$ and $ab-1=nk$ where $k$ is some integer
4. $ab-nk=1$
5. Note that all linear combinations of $a$ and $n$ are multiples of the GCD($a,n$). Thus: $ab-nk=m\text{GCD}(a,n)=1$, for some integer $m$
6. From (5), 
$$
\begin{align}
&\because m\text{GCD}(a,n)=1\\
&\therefore \text{GCD}(a,n)|1 \rightarrow\text{GCD}(a,n)=1
\end{align}
$$
Proof in the reverse direction:
1. Suppose GCD$(a,n)=1$
2. There are integers $x$ and $y$ such that $ax+ny=1$
3. $ax-1=n(-y)$
4. From (3): $ax\equiv1\pmod{n}$

## How to find modular inverses

There are two methods you can use to find the multiplicative inverse of a number modulo $n$

### Method 1: Trial and Error

Find all the inverse pairs for mod 20.

All the invertible numbers that are invertible mod 20 are all the integers that are less than 20 and are relatively prime with 20:
$$
\{1,3,7,9,11,13,17,19\}
$$
- The inverse of 1 mod 20 is 1 (because $1\times1=1$ and $1\pmod{20}=1$)
- The inverse of 3 mod 20 is 7 (because $7\times3=21$ and $21\pmod{20}=1$)
- The inverse of 9 mod 20 is 9 (because $9\times9=81$ and $81\pmod{20}=1$)
- The inverse of 11 mod 20 is 11 (because $11\times11=121$ and $121\pmod{20}=1$)
- The inverse of 19 mod 20 is 19 (because $19\equiv-1\pmod{20}$ and so multiplying both sides by 19 yields $19^2\equiv(-1)^2\equiv1\pmod{20}$
- $17\equiv-3\pmod{20}$ and $13\equiv(-7)\pmod{20}$
	- $17*13\equiv(-3)(-7)\equiv21\equiv1\pmod{20}$
	- $\therefore$The inverse of 13 and 17 are inverses of each other mod 20
### Method 2: [[Math/Number Theory/Euclidean Algorithm#Extended Euclidean Algorithm\|Extended Euclidean Algorithm]]

Example: Find the modular inverse of $34\pmod{143}$

First, we will need to find the greatest common divisor of 34 and 143

1. 143=34(4)+7
2. 34=7(4)+6
3. 7=6(1)+1
4. 6=1(6)+0
5. $\because1$ is the last non-zero remainder 
6. $\therefore1=\text{GCF}(143,34)$, which means that 143 and 34 are relatively prime and that 34 is invertible.

Now we use the above equations as a linear combination of remainders to solve for integers $x$ and $y$ in the following modular equation: 
$$34x\equiv1\pmod{143}\leftrightarrow34x+143y=1$$
7. From (1), $7=143(1)+34(-4)$
8. Substitute (7) into (2): 
$$
\begin{align}
34=(143(1)+34(-4))(4)+6\\
34=143(4)+34(-16)+6\\
6=34(17)+143(-4)
\end{align}
$$
9. Substitute (7) and (8) into (3):
$$
\begin{align}
143(1)+34(-4)=(34(17)+143(-4))(1)+1\\
143(1)+34(-4)=34(17)+143(-4)+1\\
34(-21)+143(5)=34x+143y=1\\
\therefore x=-21
\end{align}
$$
10. From (9): the inverse of 34 mod 143 is:
$$x\equiv(-21)\pmod{143}$$
To get a positive inverse for 34 mod 143, simply add a multiple of 143 to -21. In this case, let's just add 143 to -21 to get:
$$x\equiv122\pmod{143}$$
Check:
$$
\begin{align}
\frac{34(122)-1}{143}=\frac{4148-1}{143}=\frac{4147}{143}=29\\\\
\end{align}
$$
$\because143|(34*122-1)$
$\therefore$The multiplicative inverse of 34 mod 143 is 122.
