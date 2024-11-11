---
{"dg-publish":true,"permalink":"/Math/Statistics/Variance and Standard Deviation/","created":"2024-11-07T00:18:19.029-05:00","updated":"2024-11-10T22:59:04.993-05:00"}
---


#Math/Statistics

*Variance* and *standard deviation* are both measures the spread of the values in a sample or population around the [[Math/Statistics/Mean, Median, and Mode#Mean\|mean]].

The variance of a sample, denoted $\sigma^2$, can be found using the following formula:$$\sigma^2=\sum_i^n\frac{(x_i-\bar{x})^2}{n-1}$$Where $\bar{x}$ is the mean of the sample, $x_i$ represent the different values in the sample, and $n$ is the sample size.

In contrast, the variance of the population can be found using a slightly different formula:
$$
\sigma^2=\sum_i^n\frac{(x_i-\mu)^2}{n}
$$
Where $\mu$ is the mean of the population. Note that on average, the variance of the sample tends to be narrower than the variance of the population. To correct for this and get an unbiased estimator, we divide by $n-1$ for the sample variance to make it slightly wider.

The reason why the difference between $x_i$ and $\bar{x}$ is squared is because if $x_i\leq0$ then $x_i-\bar{x}$ would be negative, and squaring that difference gets rid of the negative sign.

The standard deviation is equal to the square root of the variance. The standard deviation of the sample is given by the following formula:
$$
\sigma=\sum_i^n\sqrt\frac{(x_i-\bar{x})^2}{n-1}
$$
While the formula for the standard deviation of the population is:
$$
\sigma=\sum_i^n\sqrt\frac{(x_i-\mu)^2}{n}
$$
## Example

Suppose you have the following sample: 1,2,3,4,5,6,7,8,9,10. Find the standard deviation of the sample.
1. Just from looking at the sample, we can see that it has a sample size of $n=10$
2. Now we need to look for the mean.
$$
\bar{x}=\frac{1+2+3+4+5+6+7+8+9+10}{10}=\frac{55}{10}=5.5
$$
3. Given that we know that mean and sample size, we can now find the standard deviation:
$$
\begin{align}
\sigma&=\sqrt{\frac{(1-5.5)^2+(2-5.5)^2+(3-5.5)^2+(4-5.5)^2+(5-5.5)^2+(6-5.5)^2+(7-5.5)^2+(8-5.5)^2+(9-5.5)^2+(10-5.5)^2}{10-1}}\\\\
&=\sqrt{\frac{82.5}{9}}\\\\
&\approx9.167
\end{align}
$$
