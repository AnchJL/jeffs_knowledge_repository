---
{"dg-publish":true,"permalink":"/math/statistics/binomial-distribution/"}
---


#Math/Probability 
#Math/Statistics 

A *Binomial Distribution* is a type of probability distribution for a binomial variable, which measures the number of times one of two discrete outcomes occur given $n$ number of trials (i.e. a sample size of $n$)

A variable is considered a binomial variable when the following conditions are met:
 - Each trial is an independent event (meaning that previous trials have no effect on the probability of future trials
- Each trial can be classified as one of two discrete outcomes ("success" or "failure")
- We have a fixed number of trials
- Probability of success on each trial is constant

Suppose that the probability of a successful trial is $p$. Given $n$ number of trials, the probability of a observing $k$ number of successes is given by the following formula:
$$
\begin{align}
P(X=k)&=(^nC_k)(p)^k(1-p)^{n-k}\\\\
&={n\choose k}(p)^k(1-p)^{n-k}\\\\
&=\frac{n!}{k!(n-k)!}p^k(1-p)^{n-k}
\end{align}
$$
Where function $^nC_k$ is known as the [[Combination Formula\|Combination Formula]] or *choose function*. It reads "n choose k". What this function means is that given $n$ trials, how many different ways can we select $k$ successes?

Another way of looking at the above formula is:

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin settings under 'Saving'


# Excalidraw Data
## Text Elements
Number of
Combinations 
Probability
of Success 
Probability
of Failure 
Number of
Failures 
Number of
Successes 


</div></div>

# Example 1

Suppose that I roll 4 dice. What are the odds that exactly 3 of those dice will land on a one?

Let $X$ represent the number of dice that land on a one. We are trying to find $P(X=3)$.

We know that $X$ is a binomial variable because:
- Each dice roll is independent of each other.
- Each trial can be classified as one of two discrete outcomes ("landing on one" vs "not landing on one")
- We have a fixed number of trials of $n=4$
- The probability of rolling a one on each trial (i.e. each roll of a die) is constant: $p=\frac{1}{6}$

We can map out all the possible dice rolls in the table below:

| Combination Number | Die #1  | Die #2  | Die #3  | Die #4  | Probability                                         |
| ------------------ | ------- | ------- | ------- | ------- | --------------------------------------------------- |
| 1                  | One     | One     | One     | Not One | $$\frac{1}{6}*\frac{1}{6}*\frac{1}{6}*\frac{5}{6}$$ |
| 2                  | One     | One     | Not One | One     | $$\frac{1}{6}*\frac{1}{6}*\frac{5}{6}*\frac{1}{6}$$ |
| 3                  | One     | Not One | One     | One     | $$\frac{1}{6}*\frac{5}{6}*\frac{1}{6}*\frac{1}{6}$$ |
| 4                  | Not One | One     | One     | One     | $$\frac{5}{6}*\frac{1}{6}*\frac{1}{6}*\frac{1}{6}$$ |

Remember that the probability of a die landing on one is $\frac{1}{6}$ and the probability of a die not landing on one is $\frac{5}{6}$. Moreover, each combination of dice rolls has 3 dice landing on one and 1 dice not landing on 1. Therefore, by using the [[Math/Probability Theory/Multiplication Rule for Probability\|Multiplication Rule for Probability]], we can say that each dice roll combination above has a probability of
$$
\left(\frac{1}{6}\right)^3\left(\frac{5}{6}\right)^1
$$

We can also observe that there are 4 combinations in total in the above table. Another way of finding the number of combinations of choosing 3 ones from 4 dice is to use the choose function: $^4C_3={4\choose3}=4$.

Given all this information, we can know calculate the probability of getting 3 ones from rolling 4 dice:
$$
\begin{align}
P(X=3)&={4\choose3}\left(\frac{1}{6}\right)^3\left(1-\frac{1}{6}\right)^{4-3}\\\\
&={4\choose3}\left(\frac{1}{6}\right)^3\left(\frac{5}{6}\right)^{1}\\\\
&\approx0.0154=1.54\%\\\\
\end{align}
$$
Therefore, the probability of getting exactly 3 out of 4 dice to land on one is 1.54%.

Note that if we want to find, say, the probability of getting less than 3 out of 4 dice landing on one, then we would have to add the following probabilities:
$$
P(X<3)=P(X=0)+P(X=1)+P(X=2)
$$
Below are the probabilities for each possible value for X.
$$
\begin{align}
P(X=0)={4\choose0}\left(\frac{1}{6}\right)^0\left(\frac{5}{6}\right)^4=0.482\\
P(X=1)={4\choose1}\left(\frac{1}{6}\right)^1\left(\frac{5}{6}\right)^3=0.386\\
P(X=2)={4\choose2}\left(\frac{1}{6}\right)^2\left(\frac{5}{6}\right)^2=0.116\\
P(X=3)={4\choose3}\left(\frac{1}{6}\right)^3\left(\frac{5}{6}\right)^1=0.0154\\
P(X=4)={4\choose4}\left(\frac{1}{6}\right)^4\left(\frac{5}{6}\right)^0=0.0007
\end{align}
$$
If we were to insert those probabilities into a histogram, we would get the following left-skewed binomial distribution below:
```chart
type: bar
labels: [0,1,2,3,4]
series:
  - title: Probability of Getting x out of 4 dice to Roll a One
    data: [0.482,0.386,0.116,0.015,0.0008]
tension: 0.2
width: 80%
labelColors: false
fill: false
beginAtZero: false
bestFit: false
bestFitTitle: undefined
bestFitNumber: 0
```
