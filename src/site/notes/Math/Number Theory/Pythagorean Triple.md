---
{"dg-publish":true,"permalink":"/math/number-theory/pythagorean-triple/"}
---


#Math/NumberTheory 
#Math/Trigonometry 

A Pythagorean triple is any three natural numbers, $x$, $y$, and $z$ that satisfies the [[Math/Trigonometry/Pythagorean Theorem\|Pythagorean Formula]]:
$$
x^2+y^2=z^2
$$
Examples of Pythagorean Triples:
- $3^2+4^2=5^2\Rightarrow 9+16=25$
- $5^2+12^2=13^2\Rightarrow 25+144=169$
- $6^2+8^2=10^2\Rightarrow 36+64=100$
Notice that the Pythagorean triples in the third example is double the Pythagorean triple in the first example.

A *primitive Pythagorean triple* is one where $\text{GCD}(x,y,z)=1$
- 3, 4, and 5 are a primitive Pythagorean triple
- 5, 12, and 13 are another example of a primitive Pythagorean triple
- 6, 8, and 10 are not because their greatest common divisor is 2

## Finding Primitive Pythagorean Triples

Suppose that $(x,y,z)$ is a primitive Pythagorean triple. Let's see what can be derived from this supposition. 

### Question 1: Is it possible that $x$ and $y$ are even?

1. Since $x$ and $y$ are even, they can be expressed as $x=2a$ and $y=2b$, where $a$ and $b$ are natural numbers.
2. $x^2+y^2=4a^2+4b^2=4(a^2+b^2)=z^2$
3. From (2), we can deduce that $4|z^2 \Rightarrow 2|z$
4. From (3), $z$ is not even
5. $\because x$, $y$, and $z$ are even
6. $\therefore$Their greatest common divisor has to be $\geq2$
7. $\therefore x$,$y$, and $z$ are not a primitive Pythagorean triple and so **$x$ and $y$ cannot both be even.**

### Question 2: Is it possible that $x$ and $y$ are odd?

1. Since $x$ and $y$ are odd, then they can be expressed as $x=2a+1$ and $y=2b+1$ where $a$ and $b$ are natural numbers.
2. 
$$
\begin{align}
&x^2+y^2=(2a+1)^2+(2b+1^2)\\\\
&=4a^2+2(2a)(1)+1+4b^2+2(2b)(1)+1\\\\
&=4a^2+4a+4b^2+4b+2\\\\
&=4(a^2+b^2+a+b)+2=z^2\\\
\end{align}
$$
3. From (2), we can deduce that $z^2$ is even. 
4. $z^2$ is not a multiple of 4 because dividing $z^2$ by 4 gives us a remainder of 2
5. This is a contradiction because it is impossible for a perfect square to be a multiple of 2 but not 4.
6. **$\therefore x$ and $y$ cannot both be odd**

From questions 1 and 2, the only remaining possibility for $x$ and $y$ is that one must be odd while the other is even.

## Formula for Primitive Pythagorean Triples

Supposed $(x,y,z)$ is a primitive Pythagorean triple, where $x$ is odd and $y$ is even. This means that $x^2$ is odd and $y^2$ is even, and so $z^2$ must be odd.

1. Rearrange to get: $y^2=z^2-x^2$
2. Factor using [[Math/Algebra/Factoring (work in progress)#Difference of Squares\|difference of squares]]: $y^2=(z+x)(z-x)$
3. Notice that $z-x$ and $z+x$ are even (because the sum of two odd numbers is always even)
4. So we can write $z-x=2m$ and $z+x=2n$, where $m$ and $n$ are natural numbers.
5. $y^2=(2m)(2n)=4mn$
6. Also recall that $y$ is even, so we can express it as $y=2k$ and $y^2=4k^2$
7. From (5) and (6): $4k^2=4mn\Rightarrow k^2=mn$

Given 1-7 above, we get the following conditions for primitive Pythagorean triples:
1. $x$ is odd
2. y is even (i.e. $y=2k$)
3. $z$ is odd
4. $m=\frac{z-x}{2}$
5. $n=\frac{z+x}{2}$

Note that $k^2=mn$ is a perfect square.
**Claim**: GCD(m,n)=1
**Proof**:
1. Suppose $d|m$ and $d|n$
2. From (1), 
$$
\begin{align}
d|(m+n)\\\\
d|(\frac{z-x}{2}+\frac{z+x}{2})\\\\
d|(\frac{2z}{2})\\\\
d|z
\end{align}
$$
3. Similarly, $d|x$
4. From (2) and (3), $d|\text{GCD}(x,z)\Rightarrow d|1 \Rightarrow d=1$ because 1 is the only number that can cleanly divide itself.

Since $k^2=mn$ is a perfect square with GCD$(m,n)=1$, 
then it follows that $m=p^2$ and $n=q^2$ with GCD$(p,q)=1$

1. $p^2=\frac{z-x}{2} \text{ and } q^2=\frac{z+x}{2}$
2. $2p^2=z-x \text{ and } 2q^2=z+x$
3. Substitute (2) into the equation for $y$: $y^2=(z-x)(z+x)=4p^2q^2$
4. $y=2pq$
5. Now to solve for $x$ and $z$ in terms of $p$ and $q$. From (1):
$$
\begin{align}
x=z-2p^2=2q^2-z \Rightarrow 2z=2q^2+2p^2 \Rightarrow z=q^2+p^2\\\\
z=2p^2+x=2q^2-x \Rightarrow 2x=2q^2-2p^2 \Rightarrow x=q^2-p^2
\end{align}
$$
$\therefore$ The formulas for finding primitive Pythagorean triples are
$$
\begin{align}
&x=q^2-p^2\\\\
&y=2pq\\\\
&z=q^2+p^2\\\\
&\text{Where $p$ and $q$ are coprime.}
\end{align}
$$
Remember that $x$ and z are odd and y is even, so it must be the case that $p$ is odd and $q$ is even (or vice versa).
## Example 

| $p$ | $q$ | $x$                           | $y$          | $z$                           | $x^2+y^2=z^2$ |
| --- | --- | ----------------------------- | ------------ | ----------------------------- | ------------- |
| 1   | 2   | $2^2-1^2=3$                   | $2(1)(2)=4$  | $2^2+1^2=5$                   | $9+16=25$     |
| 2   | 3   | $3^2-2^2=5$                   | $2(2)(3)=12$ | $3^2+2^2=13$                  | $25+144=169$  |
| 3   | 4   | $4^2-3^2$<br>$=16-9$<br>$=7$  | $2(3)(4)=24$ | $4^2+3^2$<br>$=16+9$<br>$=25$ | $49+576=625$  |
| 1   | 4   | $4^2-1^2$<br>$=16-1$<br>$=15$ | $2(1)(4)=8$  | $4^2+1^2$<br>$=16+1$<br>$=17$ | $225+64=289$  |
