---
{"dg-publish":true,"permalink":"/Math/Statistics/Percentiles/","created":"2024-11-10T17:38:03.373-05:00","updated":"2024-11-19T00:24:13.460-05:00"}
---

#Math/Statistics 

The *m*th percentile refers to a particular value that is above m% of the values in a sample or population. For example, the 10th percentile of a sample is the observed value that is greater or equal to 10% of the observed values from the sample.

Some **Important percentiles** are:
- 50th percentile (aka the [[Math/Statistics/Mean, Median, and Mode#Median\|median]])
- 25th, 50th, 75th, and 100th percentiles are the 1st, 2nd, 3rd, and 4th quartiles respectively
- 10th, 20th, 30th, ...., 90th, and 100th percentiles are also 1st, 2nd, 3rd, ..., 9th, and 10th deciles.

## Finding the Closest Percentile of an Observed Value

To find the percentile of an observed value $x_i$ in a sample, we need to arrange all the values in the sample from least to greatest. From there, we can determine that the initial value is the $k$th smallest observed value in the sample. From there, we divide the $k$ by the sample size $n$ and then multiply the quotient by 100 to find the percentile of the $x_i$, rounded to the nearest whole number.
$$
\text{Percentile of $x_i$}=\frac{k}{n}\times100\text{ (Rounded to the nearest whole number)}
$$

> [!Example] What percentile is the 7 in $\{1,1,3,1,5,6,8,9,5,7,8,9\}$.
> 1. First, rearrange the observed from smallest to greatest: $\{1,1,1,3,5,5,6,7,8,8,9,9\}$
> 2. From the ordered sample in (1), we can see that 7 is the 8th smallest value and the sample size is 12.
> 3. The percentile of 7 is:
> $$
> \frac{7}{12}\times100=58.333...\rightarrow58
> $$
> 4. $\therefore$The observed 7 in the sample is in the 58th percentile.

## Finding the mth Percentile of a Sample

To calculate the $m$th percentile of a sample, first find out what $m\%$ of the sample size. Let $k$ represent the $m$th percentage of sample size $n$ such that $k=m\% \times n$, rounded to the nearest whole number. The $k$th smallest value from the sample is the $m$th percentile.

> [!Example] Find the 40th percentile of the following sample $\{1,1,3,1,5,6,8,9,5,7,8,9\}$.
> 1. First, rearrange the observed from smallest to greatest: $\{1,1,1,3,5,5,6,7,8,8,9,9\}$
> 2. The size of the sample is 12, and 40% of 12 is 4.8. Rounding up to the nearest whole number, the 40th percentile  is the 5th smallest value in the sample.
> 3. From looking at the ordered sample, we can see that the 5th smallest value is 5.
> 4. $\therefore$The 40th percentile of the sample is 5.
> 
