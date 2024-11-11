---
{"dg-publish":true,"permalink":"/math/probability-theory/sets/"}
---


#Math/Probability 
#Math/SetTheory

A *set* is a collection of *distinct* objects. This could be a set of cars, people, numbers, etc. We use curly brackets to contain the items in a set. 

For example $A=\{1,2,3,4,5\}$ and $B=\{2,4,6,8,10\}$ are both sets.

Note you cannot have the same element more than once in a set. For example, $C=\{1,1,3\}$ would not be a proper set because the number "1" appears twice. Also note that the order of the elements in a set do not matter; e.g. $\{1,2,3\}=\{2,3,1\}$
## Set Operations:

### Intersection

The *intersection* operation takes the elements that are present in both set $A$ *and* in set $B$. Using the same sets for $A$ and $B$ above, the intersection of $A$ and $B$ is:
$$
A\cap B=\{2,4\}
$$

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin settings under 'Saving'


# Excalidraw Data
## Text Elements
A 
B 
U 


</div></div>

### Union

The *union* operation takes all the elements that are in $A$ *or* $B$. Using the same sets for $A$ and $B$ above, the union of $A$ and $B$ is:
$$
A\cup B=\{1,2,3,4,5,6,8,10\}
$$

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin settings under 'Saving'


# Excalidraw Data
## Text Elements
A 
B 
U 


</div></div>

### Difference Between Sets (Relative Complements)

The difference between set $A$ and set $B$ can be expressed as follows:
$$
\begin{align}
A&=\{1,2,3,4,5\}\\\\
B&=\{2,3,6,8,10\}\\\\
A-B=A\setminus B&=\{1,3,5\}
\end{align}
$$
What taking the difference does it that you subtract from $A$ the elements it shares with $B$. 

Other ways of expressing the difference between sets include "$B$ subtracted from $A$" or "Relative complement of $B$ in $A$" (i.e. what are the elements not in $B$ that are but are in $A$). The Venn diagram below illustrates what $A-B$ looks like:


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin settings under 'Saving'


# Excalidraw Data
## Text Elements
A 
B 
U 


</div></div>


Let's look at what the relative complement of $A$ in $B$:
$$
B-A=\{14,15,6\}
$$
Note that a set subtracted by itself gives the empty set (otherwise known as the null set $\emptyset$), which is a set without any elements:
$$
A\setminus A=A-A=\{\}=\emptyset
$$
## Universal Set

The universe is often depicted as a rectangle and denoted with the letter $U$. The universal set includes everything relevant to the discussion.

*Absolute Complement* of set $A$ is the universal set minus $A$:
$A'=U-A=U\setminus A$

Suppose that our universe is the entire set of integers: $U=\mathbb{Z}$

Suppose $A=\{1,2,3,4,5\}$ is a subset of the universal set.
- $1,2,3,4,5\in A$
- Meanwhile: $1,2,3,4,5\not\in A'$

## Subsets

Suppose you had the following sets:
- $A=\{1,2,3,4,5\}$
- $B=\{1,2,4\}$
- $C=\{1,2,3,4,6\}$

Given the above, we can say that $B$ is a subset of $A$ because every element in $B$ is in $A$:
$$
B\subseteq A
$$
We can  also say that $B$ is a *strict subset* (or *proper subset*) of $A$ because although every member in $B$ is in $A$, not every member in $A$ is in $B$:
$$
B\subset A
$$
An interesting thing to note is that every set is a subset of itself, although they are not a strict subset of themself:
$$
A\subseteq A
$$
$$
A\not\subset A
$$
Let us look at $C$. We can say that $B$ is a proper subset of $C$ because every element in $B$ is in $C$. We can also say that C is not a subset of $A$ because not every element in $C$ is in $A$.

## Supersets

Suppose you had the following sets:
- $A=\{1,2,3,4,5\}$
- $B=\{1,2,4\}$
- $C=\{1,2,3,4,6\}$

Given the above sets, we can say that $A$ is a superset of $B$ because it contains every element in $B$ and more:
$A\supset B$

We can also say that $A$ is a strict or proper superset of $B$ because although $A$ contains all the elements of $B$, not every element of $A$ is in $B$.