---
{"dg-publish":true,"permalink":"/Math/Statistics/Sampling Distribution/","created":"2024-11-12T01:00:48.877-05:00","updated":"2024-11-17T00:26:09.685-05:00"}
---

#Math/Statistics 

The way we try to estimate a population parameter is by taking a sample from the population and deriving a statistic we can use to estimate the value of the parameter. Note that if another sample were to be taken, it will likely not be the same value as the statistic obtained from the last sample.

A **Sampling Distribution** is the frequency distribution of all the different sample statistics if we were to sample the population multiple times. If we have a sufficiently large enough sample, then the sampling distribution will approximate a [[Math/Statistics/Normal Distribution\|Normal Distribution]] according to the [[Math/Statistics/Central Limit Theorem\|Central Limit Theorem]]. We will also find that the [[Math/Statistics/Mean, Median, and Mode#Mean\|mean]] of the sampling distribution will come closer and closer to the true population parameter.

## Standard Error

The *standard error* is the [[Math/Statistics/Variance and Standard Deviation\|standard deviation]] of a sampling distribution. For  is obtained by taking the standard deviation $\sigma$ of a sample and dividing by the square root of its sample size, $n$:
$$
\text{SE}=\frac{\sigma}{\sqrt{n}}
$$
Increasing the size of each sample reduces the standard error of the sampling distribution.
## Example
Example: say we have a population of three billiard balls numbered 1, 2, and 3. We know the mean of the population is $\frac{1+2+3}{3}=2$. We can also find the mean by taking multiple samples of two billiard balls to estimate the population mean. 

| Billiard Balls Picked, with Replacement | Sample Mean: $\bar{x}$ |
| --------------------------------------- | ---------------------- |
| 1,1                                     | 1                      |
| 1,2                                     | 1.5                    |
| 1,3                                     | 2                      |
| 2,1,                                    | 1.5                    |
| 2,2                                     | 2                      |
| 2,3                                     | 2.5                    |
| 3,1,                                    | 2                      |
| 3,2                                     | 2.5                    |
| 3,3                                     | 3                      |
If we create a frequency distribution of the sample means then we will have the *sampling distribution*. From the table above, we get the following frequency table and histogram showing the sampling distribution.

| Sample Mean | Frequency |
| ----------- | --------- |
| 1           | 1         |
| 1.5         | 2         |
| 2           | 3         |
| 2.5         | 2         |
| 3           | 1         |
![Sampling Distribution Example.png](/img/user/Sampling%20Distribution%20Example.png)
Notice that with the sampling distribution in the above graph is centered around 2, which is also the true mean of the billiard ball population.