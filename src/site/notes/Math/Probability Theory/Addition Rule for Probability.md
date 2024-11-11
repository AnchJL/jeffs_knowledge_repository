---
{"dg-publish":true,"permalink":"/math/probability-theory/addition-rule-for-probability/"}
---


#Math/Probability 

The addition rule for probability states that the [[Math/Probability Theory/What is Probability\|probability]] of event $A$ *or* event $B$ occurring is equal to the sum of the probability of $A$ with the probability of $B$ minus the probability of $A$ and $B.$ In mathematical terms:
$$
P(A\cup B)=P(A)+P(B)-P(A\cap B)
$$
The reason why we cannot just add $P(A)$ and $P(B)$ because there is a subset of the sample space where $A$ and $B$ can occur simultaneously, and so adding the probability of $A$ with the probability of $B$ would double count the probability of $A\cap B$ twice. To remove the effect of double counting, we need to subtract the sum $P(A)+P(B)$ by $P(A\cap B)$.


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/excalidraw/double-counting-in-union-operations/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin settings under 'Saving'


# Excalidraw Data
## Text Elements
A 
B 
U 


</div></div>

In the image above, adding set $A$ with set $B$ involves adding the middle part twice.
## Example:

Suppose you have the following set:
- 8 green cubes
- 9 green spheres
- 5 yellow cubes
- 7 yellow spheres

In total, we have 29 objects in that set. The probability of selecting a cube from that set is: 
$$P(C)=\frac{8+5}{29}=\frac{13}{29}$$
Meanwhile, the probability of selecting a yellow object is:
$$P(Y)=\frac{5+7}{29}=\frac{12}{29}$$
The probability of selecting a yellow cube is: 
$$P(C\cap Y)=\frac{5}{29}$$
Now let us ask what is the probability of selecting a cube *or* a yellow object? There are 8 green cubes and 5 yellow cubes, meaning there are 13 cubes in total. Meanwhile, there are 5 yellow cubes and 7 yellow spheres, meaning there are 12 yellow objects in total. When trying to find the number of objects that are cubes or yellow, we cannot simply just add 13 with 12 because we would be counting the set of 5 yellow cubes twice. To fix that, we would have to subtract 5 from the sum of 13 and 12.

Therefore, the probability of picking a cube or yellow object is:
$$
P(C\cup Y)=\frac{\text{\# of yellow objects}+\text{\# of cubes}-\text{\# of yellow cubes}}{\text{total \# of objects}}
$$
$$
P(C\cup Y)=\frac{12+13-5}{29}=\frac{20}{29}
$$
Alternatively, we can find $P(C\cup Y)$ by adding the probability of picking a cube with the probability of picking a yellow object, and then subtract the probability of picking a yellow cube.
$$
\begin{align}
P(C\cup Y)&=P(C)+P(Y)-P(C\cap Y)\\\\
P(C\cup Y)&=\frac{13}{29}+\frac{12}{29}-\frac{5}{29}
\end{align}
$$
## Mutually Exclusive Events

Events $A$ and $B$ are said to be mutually exclusive if it is impossible for $A$ and $B$ to occur at the same time. In other words,
$$
P(A\cap B)=0
$$
Thus, in the case of mutually exclusive events:
$$
P(A\cup B)=P(A)+P(B)
$$
