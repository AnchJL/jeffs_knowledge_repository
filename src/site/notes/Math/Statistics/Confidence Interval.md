---
{"dg-publish":true,"permalink":"/Math/Statistics/Confidence Interval/","created":"2024-11-16T20:54:44.839-05:00","updated":"2024-11-17T01:26:11.419-05:00"}
---

#Math/Statistics 

A *confidence interval* represents the range of data in which a given population parameter (i.e. the true mean or proportion) is expected to lie within. To say that $[x_1,x_2]$ is a 95% confidence interval means that there if we were to construct 100 sample confidence intervals, then 95 of them would contain the true population parameter.

The formula for a confidence interval is given by the following formula:
$$
\text{CI}_{1-\alpha}=\bar{x}\pm \text{SE}\cdot z_{\alpha/2}
$$
To find the 95% confidence interval, we will need to find the z-score in which 95% of all values in a [[Math/Statistics/Sampling Distribution\|Sampling Distribution]] lies within $\pm z$. Luckily, we know from the [[Math/Statistics/Normal Distribution#Empirical Rule\|empirical rule]] that 95% of all possible values lies within 2 standard deviations (1.96 standard deviations to be exact) from the mean of a [[Math/Statistics/Normal Distribution\|normal distribution]]. Thus, the relevant z-score for a 95% confidence interval is 1.96. Below are the formulas for a 90%, 95%, and 99% confidence interval:

- **90% Confidence Interval**: $\text{CI}_{90\%}=\bar{x}\pm1.65\cdot\text{SE}$
- **95% Confidence Interval**: $\text{CI}_{95\%}=\bar{x}\pm1.96\cdot\text{SE}$
- **99% Confidence Interval**: $\text{CI}_{95\%}=\bar{x}\pm2.575\cdot\text{SE}$
## Example:

Suppose you took a sample of 100 people who engage in a mean of 50 minutes of physical activity per day. The standard deviation of the sample is 20. Find the 95% confidence interval.

First, let's find the standard error of the population:
$$
\text{SE}=\frac{20}{\sqrt{100}}=\frac{20}{10}=2
$$
Given that 95% of the values in a normal distribution lie within 1.96 standard errors of a sampling distribution, we will need to use a z-score of 1.96.

Lower bound: $50-1.96\cdot2=46.08$
Upper bound: $50+1.96\cdot2=53.92$

Therefore, the 95% confidence interval for the sample is $[46.08,53.92]$.