---
{"dg-publish":true,"permalink":"/Math/Statistics/Hypothesis Testing/","created":"2024-11-16T20:54:23.242-05:00","updated":"2024-12-01T13:43:28.909-05:00"}
---

#Math/Statistics 

Hypothesis testing is another tool besides [[Math/Statistics/Confidence Interval\|confidence intervals]] that we use to make inferences about a population from a sample. Hypothesis testing works by constructing a *null hypothesis* about the population parameter we are interested in. Typically, the null hypothesis states that a population parameter is equal to some specific value (often zero)

**Examples of null hypothesis:**
- The proportion of left-handed people equals the proportion of right handed people in the population
- The mean expenditure on gasoline by people who care about climate change is equal to the mean expenditure on gasoline by the general population

**Two possible outcomes of hypothesis testing:**
1. Reject the null hypothesis in support of the research or alternative hypothesis
2. Fail to reject the null hypothesis

> [!Note]
> You can never accept the null hypothesis; you can only reject or fail to reject them. Hypothesis testing can never conclusively prove a claim; it can only support or weaken a claim. 

> [!Summary] How to conduct a hypothesis test:
> 1. Establish a research and null hypothesis, and an appropriate alpha value
> 2. Identify whether you are using a one (left or right) or two tail test
> 3. Calculate the relevant test-statistic from the sample statistic
> 4. Calculate the probability (i.e. p-value) of observing the sample statistic given its test-statistic.
> 5. Determine whether the p-value is below the chosen $\alpha$. If $p\leq\alpha$, then you can reject the null hypothesis in favour of the research hypothesis. If $p>\alpha$, then you cannot reject the null hypothesis.
> 	- If we were to use a 90% confidence level ($1-\alpha=0.9$), then we need a p-value that is less than 0.1 to reject the null hypothesis
> 	- If we use a 95% confidence level ($1-\alpha=0.05$), then the p-value needs to be less than 0.05 for us to reject the null hypothesis
> 	- If we use a 99% confidence level ($1-\alpha=0.01$), then p-value needs to be less than 0.01 for us to reject the null hypothesis
## Example

Suppose we want to learn whether people who care about climate change spend less money buying gasoline than the average Canadian adult. From there, we develop the following research hypothesis: Canadians who care about climate change spend less per month on gasoline than the average Canadian adult. Given this research hypothesis, we derive the following hypothesis:
- We draw a random sample of 100 people who donate to climate activist organizations, and we find that they spend a monthly average of $28.60 on gasoline.
- In contrast, the average Canadian adult spends $31.11 per month on gasoline, with a standard deviation of $1.70.
- Given our research hypothesis and these facts, we get the following hypotheses:
	- Null hypothesis: Canadians who care about climate change spend the same amount of money per month on gasoline as the average adult in Canada 
		- $H_0: \mu=31.11$
	- Research/alternative hypothesis: Canadians who care about climate change spend less money per month on gasoline than the average adult in Canada 
		- $H_a: \mu<31.11$
		- Note that this research hypothesis requires a one-tailed test.
- Fine the test statistic:
$$
\begin{align}
Z=\frac{\bar{x}-\mu}{\text{SE}}=\frac{28.60-31.11}{\frac{1.70}{\sqrt{10,000}}}=-\frac{2.51}{0.17}\\
=-14.7647
\end{align}
$$
The probability (or p-value) of obtaining a z-score of -14.76 or lower is very small (almost 0). Whether we reject or fail to reject $H_0$ depends on our confidence level ($\alpha$ level): 

If we were to use a 99% confidence level, our p-value is low enough for us to reject the null hypothesis that Canadians who care about climate change spend the same amount of money on gas as the average Canadian.