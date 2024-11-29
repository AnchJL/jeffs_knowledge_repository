---
{"dg-publish":true,"permalink":"/Math/Probability Theory/Bayes' Theorem/","created":"2024-11-04T23:33:00.638-05:00","updated":"2024-11-24T14:43:21.228-05:00"}
---


#Math/Probability 

Bayes' Theorem states that the probability of event $A$ given event $B$ is equal to the product of the probability of $A$ and the probability of $B$ given $A$, over the probability of $B$. In other words:
$$
P(A|B)=\frac{P(A)\cdot P(B|A)}{P(B)}
$$
> [!Example] Suppose a contagious disease affects 1% of the population. You take a medical test for the disease and the results were positive. What is the probability of you having the disease if the test provides a true positive result for 90% of infected patients (i.e. 10% of infected patients get a false negative) and a true negative result for 90% of non-infected patients (i.e. 10% of non-infected patients get a false positive)?
> 
> At first glance, it would seem that the probability of you having the disease given that you tested positive, $P(Disease|Positive)$, is 0.9. However, that is wrong.
> 
> We can use calculate the actual probability using Bayes' theorem.
> $$P(Disease|Positive)=\frac{P(Disease)\cdot P(Positive|Disease)}{P(Positive)}$$
> 
> We already know that $P(Disease)=0.01$ and $P(Positive|Disease)=0.9$.
> 
> To figure out $P(Positive)$, we'll have to add the probability that you tested positive if you had the disease with the probability that you tested positive if you do not have the disease:
> $$
> P(Positive)=P(Positive|Disease)\cdot P(Disease)+P(Positive|\neg Disease)\cdot P(\neg Disease)
> $$
> $$
> =0.90\cdot0.01+0.10\cdot0.99
> $$
> Substituting those above values into our Bayesian formula yields:
> $$
> P(Disease|Positive)=\frac{0.01\cdot0.90}{0.90\cdot0.01+0.10\cdot0.99}=0.0833...
> $$
> $\therefore$ You have a ~8.33% of being infected with the disease given that you tested positive.

Bayes' theorem forms the basis of [[Bayesian Statistics\|Bayesian Statistics]] and inferences, which involves the use of evidence to update the probability of our prior beliefs.
## Proof

Recall from the formula for [[Math/Probability Theory/Multiplication Rule for Probability\|Multiplication Rule for Probability]]:
1. $P(A\cap B)=P(A)\cdot P(B|A)=P(B)\cdot P(A|B)$
2. To solve for $P(A|B)$ divide both sides by $P(B)$:
$$
P(A|B)=\frac{P(A)\cdot P(B|A)}{P(B)}
$$
