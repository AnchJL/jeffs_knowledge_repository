---
{"dg-publish":true,"permalink":"/Math/Statistics/P-Hacking/","created":"2024-12-03T01:33:54.857-05:00","updated":"2024-12-04T23:04:43.651-05:00"}
---

#Math/Statistics 

P-hacking is the practice of manipulating data or data analyses to artificially obtain statistically significant results (i.e. a low enough p-value). 

In [[Math/Statistics/Hypothesis Testing\|Hypothesis Testing]], failing to reject the null hypothesis means there is a lack of evidence against the null hypothesis, However, that does not mean there is evidence in favour of the null hypothesis. Given this, results in which you are unable to show any statistically significant effect or relationship are boring and unlikely to get published. Non-results are unlikely to get published, and so scientists are incentivized to rely on p-hacking to obtain statistically significant results to publish.

> [!Note]
> Remember that p-hacking is not always done maliciously. P-hacking can be inadvertently performed through a lack in the researcher's statistical knowledge or through a simple mistake.

## Family-Wise Error Rate

One way p-hacking is done is by conducting similar tests over and over again until you obtain a significant result. The more statistical analyses you perform, the more likely you are to obtain a statistically significant result at least once by chance, even if it was a false positive (i.e. a [[Math/Statistics/Hypothesis Testing#Type I and Type II Errors\|type I error]]). The likelihood of obtaining a false positive through repeated testing is known as the *Family-Wise Error Rate*. See the comic by xkcd below for a humorous example of p-hacking through multiple testing.

[Comic #882 by xkcd: Significant](https://xkcd.com/882/)
![XKCD Comic on P-Hacking.png](/img/user/XKCD%20Comic%20on%20P-Hacking.png)

In the comic above, the scientists conducted 20 different statistical tests to determine if a particular colour of jelly beans is linked to acne. Supposing that the null hypothesis is true (that the color of jelly beans has no effect on acne), we would have a 5% chance of obtaining a false positive if we were to use a 5% significance level. Repeating the same experiment 20 times for different colours would have a $1-0.95^{20}\approx64.15\%$ chance of producing at least one or more statistically significant result, even if the null hypothesis was true. In other words, there is a family-wise error rate of 64.15%.

### Reducing the Family-Wise Error Rate

A way to reduce the family-wise error rate is to divide your initial significance level by the number of tests or analyses you are performing. To use the jellybean example above: if you were conducting statistical tests on 20 different colours of jellybeans to see if they were linked to acne and if you wanted to use a significance level of 0.05, then your new significance level that you should use is $\frac{0.05}{20}=0.0025$ or $0.25\%$.

Under this new significance level, the probability of you getting one or more significant result through chance is $1-0.9975^{20}\approx0.0488$ or $4.88\%$.