---
{"dg-publish":true,"permalink":"/Sampling Distribution/","created":"2024-11-12T01:00:48.877-05:00","updated":"2024-11-13T02:31:28.184-05:00"}
---

#Math/Statistics 

The way we try to estimate a population parameter is by taking a sample from the population and deriving a statistic we can use to estimate the value of the parameter. Note that if another sample were to be taken, it will likely not be the same value as the statistic obtained from the last sample.

A **Sampling Distribution** is the frequency distribution of all the different values that can be obtained from the statistic, if we were to sample the population multiple times.

# Example
Example: say we have a population of three billiard balls $\{1,2,3\}$, and we take multiple samples of two to estimate the population mean. 

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
If we create a frequency distribution of the sample means then we will have the *sampling distribution*. If we have a sufficiently large enough sample, then the sampling distribution will approximate a [[Math/Statistics/Normal Distribution\|Normal Distribution]] according to the [[Math/Statistics/Central Limit Theorem\|Central Limit Theorem]]. We will also find that the mean of the sampling distribution will come closer and closer to the true population parameter.
