---
{"dg-publish":true,"permalink":"/math/number-theory/congruence-relation/"}
---


#Math/NumberTheory 

Below is a general example of a congruence relationship

$a\equiv b \pmod{n}$

The way say the above expression is "$a$ is congruent to $b$, module $n$." What that means is that $a-b$ is divisible by $n$, i.e. $n|(a-b)$. Another way to interpret it is that $a$ and $b$ have the same remainder when divided by $n$.

**Examples**: 

$8\equiv3\pmod{5}$ because $5|(8-3)$

$20\equiv 4\pmod{8}$ because $8|(20-4)$

$13\equiv-1\pmod{7}$ because $7|(13-(-1))$
## Proof that $a\pmod{n}=b\pmod{n}$ means that $n|(a-b)$

If $a$ and $b$ divided by $n$ yield the same remainder, then:
1. $a=nq_1+r$
	Where $q_1\in\mathbb{Z}$
2. $b=nq_2+r$
	Where $q_2\in\mathbb{Z}$
3. Subtract equation (2) from equation (1): 
$$
\begin{align}
&a-b=nq_1+r-nq_2-r\\\\
&a-b=nq_1-nq_2\\\\
&a-b=n(q_1-q_2)\\\\
&\because q_1,q_2\in\mathbb{Z}\\\\
&\therefore (q_1-q_2)\in\mathbb{z}\\\\
&\therefore n|(a-b)
\end{align}
$$


## Congruence Relation Properties

Proposition: congruence modulo $n$ is an equivalence relation. What that means is that the following three things are true:
1. Congruence relations are *reflexive*: For all integers $a$, $a$ is congruent to itself
2. Congruence relations are symmetrical: For all integers of $a$ and $b$, if $a\equiv b \pmod{n}$ then $b\equiv a\pmod{n}$
3. Congruence relations are *transitive*: For all integers $a$, $b$, and $c$, if $a\equiv b\pmod{n}$ and $b\equiv c\pmod{n}$ then $a\equiv c\pmod{n}$

### Proof of (3)

Suppose $a\equiv b\pmod{n}$ and $b\equiv c\pmod{n}$
1. $a-b=nk$ where $k$ is some integer
2. $b-c=nl$ where l is some integer
3. Add (1) and (2): 
$$
\begin{align}
&a-b+b-c=nk+nl\\\\
&a-c=nk+nl=n(k+l)\Rightarrow n|(a-c)\\\\
&\because n|(a-c)\\\\
&\therefore a\equiv c\pmod{n}
&\end{align}
$$

## Equivalence Classes

Let us look at another definition that can be looked at for all equivalence relations. For integer $x$ define the equivalence class of $x$ with respect to $\equiv\pmod{n}$ by:
$$
[x]\equiv\{a\in\mathbb{Z}|a\equiv x\pmod{n}\}
$$
Example: $n=3$
Set $x=0$, meaning we want an equivalence class of 0, which would be all integers of $a$ such that $a\equiv0\pmod{3}$:
$[0]=\{a\in\mathbb{z}|a\equiv0\pmod{3}\}=\{0,\pm3,\pm6\}$
In other words, all those integers of $a$ are part of the equivalence class of $0\mod{3}$

$x=1,[1]=\{a\in\mathbb{z}|a\equiv1\pmod{3}\}=\{...,-5,-2,1,4,7,10,...\}$
All the above integers of $a$ are part of the equivalence class of $1\mod{3}$

### Fact: There are exactly $n$ equivalence classes modulo $n$.

Those equivalence classes are given as follows: 
$$[0],[1],[2],...[n-1]$$
**Definition**: If we fix n, then the set of *least residues* is given by the set:
$${0,1,...,n-1}$$
**Claim**: For all integers $a$, $a$ is congruent to exactly one of the least residues modulo $n$.

**Proof**: Use the [[Math/Number Theory/Division Algorithm\|division algorithm]] with the following for $a$ and $n$
$$
\begin{align}
&a=nq+r,&0\leq r\leq n-1\\\\
&a-r=nq\\\\
&a\equiv r \pmod{n}
\end{align}
$$
What this means is that $a$ is congruent to a whole number between 0 and $n-1$, that is to say, one of its least residues.

The *exactly one* portion of the claim stems from the division algorithm, which states that $r$ and $q$ are unique for any value of $a$ and $n$.
## Properties of Integer Congruence

**Proposition**: If $a\equiv b \pmod{n}$ and $c\equiv d\pmod{n}$ then
$$
\begin{align}
a+c\equiv(b+d)\pmod{n}\\\\
ac\equiv bd\pmod{n}
\end{align}
$$
Congruence relations is compatible with normal arithmetic.

### Proof that $a+c\equiv(b+d)\pmod{n}$: 
1. $a-b=nk$
2. $c-d=nl$
3. Add (1) and (2)
4. $a-b-(c-d)=nk-nl$
5. $(a+c)-(b+d)=n(k+l)\Rightarrow n|[(a+c)-(b+d)]\Rightarrow (a+c)\equiv(b+d)\pmod{n}$

### Proof that $ac\equiv bd\pmod{n}$
1. Notice that $a=b+nk$ and $c=d+nl$
2. Multiply the above two equations together: $ac=(b+nk)(d+nl)$
3. $ac=bd+bnl+dnk+n^2kl$
4. $ac=bd+n(bl+dk+nkl)$
5. $ac-bd=n(bk+dk+nkl)$
6. Give the above, ac-ad is a multiple of $r$

## Proof that If $a\equiv b\pmod{m}$ and $n|m$, then $a\equiv b\pmod{n}$

Example: 
$$
\begin{align}
&5\equiv1\pmod{4}\\\\
&2|4\\\\
&5\equiv1\pmod{2}\\\\
\end{align}
$$
Proof:
1. Suppose that $a\equiv b\pmod{m}$ and $n|m$
2. $a-b=mk$ and $m=nl$, where $k$ and $l$ are integers.
3. $a-b=nlk=nk'$ where $k'$ is an integer that equals $lk$
4. From (3), n|(a-b)
5. From (4), $a\equiv b \pmod{n}$

## When can we cancel $c$ in $ca\equiv b\pmod{n}$

Example:
$$
\begin{align}
2a\equiv0\pmod{4}\\\\
2a\equiv2*0\pmod{4}\\\\
\text{Note that } a\equiv0\pmod{4}\\\\
a\equiv2\pmod{3}\\\\
\end{align}
$$
**Proposition**: for integers $a$, $b$, and $c$, we have:
$$
ca\equiv cb\pmod{n} \Leftrightarrow a\equiv b\pmod{n}
$$
**Proof**:
1. If $ca\equiv cb\pmod{n}$ then that means $ca-cb=c(a-b)=nk$, where $k$ is an integer.
2. Let $d=\text{GCD}(c,n)$
3. Divide both sides by d: $\frac{c}{d}(a-b)=\frac{n}{d}k$
4. From (2), we can infer that $\frac{c}{d}$ and $\frac{n}{d}$ are relatively prime because $d$ is their greatest common divisor of $c$ and $n$ (if $\frac{c}{d}$ and $\frac{n}{d}$ weren't relatively prime, then that means that $c$ and $n$ could be divided even further by a common divisor greater than $d$).
5. From (3) and (4), that means $(a-b)$ is a multiple of $\frac{k}{d}$
6. $a-b=nk'$ where $k'$ is an integer that is equal to $\frac{k}{d}$
7. $ca\equiv cb\pmod{n}$ if and only if $a\equiv b\pmod{\frac{n}{GCD(c,n)}}$

Example:
1. $3x\equiv12\pmod{15}$
2. $\equiv 3(4)\pmod{15}$
3. $x\equiv4\pmod{\frac{15}{GCD(3,15)}}$
4. $\equiv4\pmod{5}$ is one possible solution
5. $\equiv 9\pmod{15}$ is another solution