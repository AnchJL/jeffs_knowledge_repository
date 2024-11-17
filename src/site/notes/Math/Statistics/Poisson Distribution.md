---
{"dg-publish":true,"permalink":"/Math/Statistics/Poisson Distribution/","created":"2024-11-11T17:24:37.322-05:00","updated":"2024-11-16T11:47:22.000-05:00"}
---

#Math/Statistics 

A *Poisson Distribution* is a type of probability distribution for [[Math/Statistics/Types of Variables#Discrete Variables\|discrete variables]] around a given mean or expected value. For an expected value of $\lambda$ in a given time frame, the formula for the probability of event $x$ occurring in the same time frame is the following:
$$
P(X=x)=\frac{\lambda^xe^{-\lambda}}{x!}
$$
## Example 
Suppose that Bob has a bakery and expects to sell an average of 20 donuts every hour. What are the odds that Bob sells 16 donuts in a given hour?

In this scenario, $x=16$ and $\lambda=20$. Plugging those values into the equation for the Poisson distribution yields:
$$
P(X=16)=\frac{20^{16}e^{-20}}{16!}\approx6.46\%
$$
Therefore, the odds that Bob will sell 16 donuts in an hour is 6.46%

Graphing the Poisson distribution above for $\lambda=20$ yields the following:
![Poisson Distribution Example (lambda=20).png](/img/user/Poisson%20Distribution%20Example%20(lambda=20).png)