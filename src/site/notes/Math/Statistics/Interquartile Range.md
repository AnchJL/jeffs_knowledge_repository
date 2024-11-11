---
{"dg-publish":true,"permalink":"/Math/Statistics/Interquartile Range/","created":"2024-11-07T22:55:52.188-05:00","updated":"2024-11-11T00:04:14.886-05:00"}
---


#Math/Statistics 

The interquartile range is another measure of the spread of data in a sample besides the [[Math/Statistics/Variance and Standard Deviation\|Variance and Standard Deviation]]. The interquartile range measure the spread by taking the difference between third and first quartile. In more mathematical terms:
$$
\text{IQR}=Q_3-Q_1
$$
$Q_3$ represents the value that is larger than 75% of all the values in a sample, while $Q_1$ represents the value that is larger than 25% of the sample.

## Example

Find the interquartile range following sample: $\{23,4,6,11,3,15,14,13\}$
1. First, rearrange the values from least to greatest: 3,4,6,11,13,14,15,23
2. To find the 

| $i$ | $x_i$ |
| --- | ----- |
| 1   | 3     |
| 2   | 4     |
| 3   | 6     |
| 4   | 11    |
| 5   | 13    |
| 6   | 14    |
| 7   | 15    |
| 8   | 23    |

To find $Q_1$, find the $x_i$ value that corresponds to a value of $i=\frac{n}{4}$ (rounded up to the nearest whole number). In this case, $n=8$ and so the value of $i$ corresponding to $Q1$ is 
$$i=\frac{8}{4}=2$$
Looking at the table above, the $x_i$ value that corresponds to $i=2$ is $x_2=4$. Therefore, $Q_1=4$.

To find $Q_2$, find the $x_i$ value that corresponds to a value of $i=\frac{3}{4}n$. In this case,
$$
i=\frac{3}{4}\cdot8=\frac{24}{4}=6
$$
Looking at the table above, $x_6=14$. Therefore, $Q_3=14$.

Given the $Q_1$ and $Q_3$ values above, the interquartile range is: 
$$
\text{IQR}=Q_3-Q_1=14-4=10
$$
