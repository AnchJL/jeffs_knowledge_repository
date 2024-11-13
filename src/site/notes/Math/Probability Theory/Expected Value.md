---
{"dg-publish":true,"permalink":"/Math/Probability Theory/Expected Value/","created":"2024-11-12T01:01:39.636-05:00","updated":"2024-11-12T01:24:30.939-05:00"}
---

#Math/Probability 
#Math/Statistics 

The *expected value* of a probability distribution is the average value that would be obtained from performing a large number of trials. Generally, the expected value is calculated from the adding all the possible values of a random variable, weighted by their corresponding probabilities.

For continuous variables, the formula for the expected value is typically obtained through integration, i.e.:
$$
E(X)=\int_{-\infty}^{\infty}xP(X=x)\,dx
$$
For discrete variables, the expected value is generally obtained through summation:
$$
\sum_{i=1}^{n}x_iP(X=x_i)
$$
For the well-known probability distributions, we have derived simpler formulas for their expected values.

The table below lists several famous probability distributions, with formulas for their expected value. 

| Type of Probability Distribution    | Expected Value     |
| ----------------------------------- | ------------------ |
| [[Bernoulli Distribution\|Bernoulli Distribution]]          |                    |
| [[Math/Statistics/Binomial Distribution\|Binomial]] | $E(X)=np$          |
| [[Math/Statistics/Normal Distribution\|Normal]]     | $\mu$ or $\bar{X}$ |
| Standardized Normal                 | 0                  |
| [[Math/Statistics/Poisson Distribution\|Poisson]]   | $\lambda$          |
