---
{"dg-publish":true,"permalink":"/math/probability-theory/conditional-probability/"}
---


#Math/Probability 

*Conditional Probability* refers to the likelihood of an event $A$ occurring given some other event $B$ has occurred. Mathematically, conditional probabilities are denoted as $P(A|B)$. To find the conditional probability of $A$ given $B$, you would need to use the formula below:
$$
P(A|B)=\frac{P(A\cap B)}{P(B)}
$$
## Example

Suppose 40 men and 60 women were selected for a survey on whether left-handed or right-handed. The results are captured in the table below:

|           | Left-Handed | Right-Handed | Total |
| --------- | ----------- | ------------ | ----- |
| **Men**   | 10          | 30           | 40    |
| **Women** | 20          | 40           | 60    |
| Total     | 30          | 70           | 100   |
From the table above, there are a total of 30 people who are left-handed and 70 people who are right-handed.

What is the probability a randomly picked individual from the survey is left-handed, given that they are a woman?
$$
\begin{align}
&P(W\cap L)=\frac{20}{100}\\\\
&P(W)=\frac{60}{100}\\\\
&P(L|W)=\frac{P(W\cap L)}{P(W)}=\frac{\frac{20}{100}}{\frac{60}{100}}=\frac{20}{60}=\frac{1}{3}
\end{align}
$$
In contrast, the odds of an individual being left-handed given that they are a man:
$$
\begin{align}
&P(W\cap L)=\frac{20}{100}\\\\
&P(L)=\frac{30}{100}\\\\
&P(W|L)=\frac{P(W\cap L)}{P(L)}=\frac{\frac{20}{100}}{\frac{30}{100}}=\frac{20}{30}=\frac{2}{3}
\end{align}
$$
