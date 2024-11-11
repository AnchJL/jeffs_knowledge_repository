---
{"dg-publish":true,"permalink":"/math/number-theory/euler-s-totient-function/"}
---


#Math/NumberTheory 

*Euler's Totient Function*, expressed as $\phi(n)$, returns the number of integers between 1 and n that are coprime with $n$. Integers that are $\leq n$ and coprime with $n$ are often called *totatives* of $n$.

**Example**:
There are 4 integers that are coprime with 10 and less than 10: 1, 3, 7, and 9.
$\therefore\phi(10)=4$

The *Reduced Residue System Modulo n* is a set of integers $\{b_1,b_2,...,b_{\phi(n)}\}$ such that GCD$(b_r,n)=1$ and $r\neq s$, $b_r\neq b_s \pmod{n}$. In plain English, this means that all the $b$ values are incongruent with each other modulo $n$ and that they are all coprime with $n$.

Examples:

| $n$ | $\phi(n)$ | Some Reduced Residue Systems |
| --- | --------- | ---------------------------- |
| 4   | 2         | {1,3},{-1,1},{3,5}           |
| 8   | 4         | {1,3,5,7}{-3,-1,1,3}         |
| 10  | 4         | {1,3,7,9},{7,9,11,23}        |
| 9   | 6         | {1,2,4,5,7,8},...            |
