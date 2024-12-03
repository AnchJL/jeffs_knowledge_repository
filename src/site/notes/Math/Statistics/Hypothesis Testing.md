---
{"dg-publish":true,"permalink":"/Math/Statistics/Hypothesis Testing/","created":"2024-11-16T20:54:23.242-05:00","updated":"2024-12-03T02:01:30.489-05:00"}
---

#Math/Statistics 

[[Math/Statistics/Descriptive vs Inferential Statistics\|inferential statistics]], hypothesis testing is a tool that we use to make inferences about a population from a sample. Hypothesis testing works by constructing a *null hypothesis* about the population parameter we are interested in, and testing how unlikely a sample statistic would be to obtain if the null hypothesis was true. Typically, the null hypothesis states that a population parameter is equal to some specific value (often zero).

**Examples of null hypothesis:**
- The proportion of left-handed people equals the proportion of right handed people in the population
- The mean expenditure on gasoline by people who care about climate change is equal to the mean expenditure on gasoline by the general population.

If your sample statistic was very unlikely to get given a true null hypothesis, then we would say that your sample statistic was statistically significant. If the probability of obtaining the sample statistic was below a certain probability called the significance level, then you would have grounds to reject the null hypothesis in favour of the alternative hypothesis. If your sample statistic was not below a certain probability, then you would fail to reject the null hypothesis.

> [!Note]
> You can never accept the null hypothesis; you can only reject or fail to reject them. Hypothesis testing can never conclusively prove a claim; it can only support or weaken a claim. 

> [!Summary] How to conduct a hypothesis test:
> 1. Establish a research and null hypothesis, and an appropriate alpha value
> 2. Identify whether you are using a one (left or right) or two tail test
> 3. Calculate the relevant test-statistic from the sample statistic
> 4. Calculate the probability (i.e. p-value) of observing the sample statistic given its test-statistic.
> 5. Determine whether the p-value is below the chosen significance level $\alpha$. If $p\leq\alpha$, then you can reject the null hypothesis in favour of the research hypothesis. If $p>\alpha$, then you cannot reject the null hypothesis.
> 	- If we were to use a 90% confidence level ($1-\alpha=0.9$), then we need a p-value that is less than 0.1 to reject the null hypothesis
> 	- If we use a 95% confidence level ($1-\alpha=0.05$), then the p-value needs to be less than 0.05 for us to reject the null hypothesis
> 	- If we use a 99% confidence level ($1-\alpha=0.01$), then p-value needs to be less than 0.01 for us to reject the null hypothesis
## Example 1: Hypothesis Testing for Means

Suppose we want to learn whether people who care about climate change spend less money buying gasoline than the average Canadian adult. We draw a random sample of 100 people who donate to climate activist organizations, and we find that they spend a monthly average of $28.60 on gasoline. In contrast, the average Canadian adult spends $31.11 per month on gasoline, with a standard deviation of $1.70.

**Step 1: Identify the Null Hypothesis and the Alternative Hypothesis**
From there, we develop the following research hypothesis: Canadians who care about climate change spend less per month on gasoline than the average Canadian adult. Given this research hypothesis, we derive the following hypothesis:
- Given our research hypothesis and these facts, we get the following hypotheses:
	- Null hypothesis: Canadians who care about climate change spend the same amount of money per month on gasoline as the average adult in Canada 
		- $H_0: \mu=31.11$
	- Research/alternative hypothesis: Canadians who care about climate change spend less money per month on gasoline than the average adult in Canada 
		- $H_a: \mu<31.11$

**Step 2: Identify Whether We are Using a Left, Right, or Two-Tail Test**
Note that this research hypothesis requires a one-tailed test.

**Step 3: Calculate the Relevant Test Statistic**
Find the test statistic:
$$
\begin{align}
Z=\frac{\bar{x}-\mu}{\text{SE}}=\frac{28.60-31.11}{\frac{1.70}{\sqrt{10,000}}}=-\frac{2.51}{0.17}\\
=-14.7647
\end{align}
$$
**Step 4: Calculate the P-Value**

The probability (or p-value) of obtaining a z-score of -14.76 or lower is very small (almost 0). Whether we reject or fail to reject $H_0$ depends on our confidence level ($\alpha$ level): 

**Step 5: Decide on whether to Reject the Null Hypothesis**

If we were to use a 99% confidence level, our p-value is low enough for us to reject the null hypothesis that Canadians who care about climate change spend the same amount of money on gas as the average Canadian.

## Example 2: Hypothesis Testing for Proportions

Suppose the government wanted to implement a sugar tax, but are unsure of whether it will be popular or unpopular. Researchers took a random sample of 40 people, and found that 56% of people disapprove of such a policy.

**Step 1: Identify the Null Hypothesis and the Alternative Hypothesis**

Null hypothesis should be that the disapproval rating is 50% (the sugar tax is neither massively popular or unpopular). The alternative hypothesis is that that the disapproval rating is not equal to 50%. Thus:
$$
H_0=0.5
$$
$$
H_a\neq0.5
$$
**Step 2: Identify Whether We are Using a Left, Right, or Two-Tail Test**
Since are alternative hypothesis s states that the disapproval rating for the sugar tax is *not equal* to 50%, we should be using a two-tail test.

**Step 3: Calculate the Relevant Test Statistic**
To find the z-score, we need to find the standard error from the sample. When trying to find the standard error of a proportion statistic, we need to use the following formula:
$$
SE=\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}
$$
Where $\hat{p}$ is the sample proportion.

In this example:
$$
SE=\sqrt{\frac{0.56(1-0.56)}{40}}
$$
Thus, the z-score should be:
$$
Z=\frac{\hat{p}-p}{SE}=\frac{0.56-0.5}{\sqrt{\frac{0.56(1-0.56)}{40}}}\approx0.764
$$
**Step 4: Calculate the P-Value**
$$
\text{p-value: }2\cdot P(z>0.764)\approx0.44487
$$
**Step 5: Decide on whether to Reject the Null Hypothesis**
Since 
Let us choose an $\alpha$ level of 0.01. Given that our p-value is greater than $\alpha$ ($0.44487>0.01$), we cannot reject our null hypothesis with a confidence level of 99%.

In other words, we fail to reject the idea the hypothesis that the sugar tax would be either massively popular or unpopular.

## Type I and Type II Errors

In hypothesis testing, we could come to an incorrect conclusion about our null hypothesis. A **type I** error, also known as a false positive, occurs when we incorrectly reject a null hypothesis that was true. Conversely, a **type II** error, also known as a false negative, occurs when we incorrectly fail to reject a null hypothesis when it was false. The table below illustrates the circumstances in which we either make the correct decision or commit a type I or type II error:

| $H_0$ is... | Rejected                         | Not rejected                      |
| ----------- | -------------------------------- | --------------------------------- |
| True        | Type I Error<br>(False Positive) | Correct Decision                  |
| False       | Correct Decision                 | Type II Error<br>(False Negative) |
