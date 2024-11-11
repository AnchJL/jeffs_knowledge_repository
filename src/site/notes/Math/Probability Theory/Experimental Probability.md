---
{"dg-publish":true,"permalink":"/Math/Probability Theory/Experimental Probability/","created":"2024-11-09T10:38:17.953-05:00","updated":"2024-11-10T21:49:33.597-05:00"}
---


#Math/Probability 
#Math/Statistics 

In contrast to *theoretical probability*, which is calculated from a hypothetical sample space, *experimental probability* is obtained from past data or observations. More specifically, experimental probability is calculated by finding the proportion of observed outcomes that meet a specific condition.

In theory, the probability of flipping a coin and getting it to land on heads is $P(H)=\frac{1}{2}$, because there are a total of two outcomes {H,T} and only one of them is heads. Based on this theoretical probability, we expect to get 5,000 heads from 10,000 coin flips. However, suppose we actually did perform 10,000 coin flips and got heads 9,000 times. From this experimental data, the probability of the flipped coin landing on heads is $\frac{9}{10}$. The experimental probability is very different from the theoretical probability.

## Example

It is easy to obtain the theoretical probability of relatively simple evens like a coin flip or a dice roll. However, the theoretical probabilities of complicated events, such as the probability of a sports team winning x number of points in a match, are practically impossible to determine. There are two many variables that are impossible to fully factor, such as the weather, the chemistry between the teams, their relative skills, etc. For these types of situations, it makes more sense to look at the *experimental probability*, which is an estimate of the chances of an event occurring based on past data.

Below is a [[histogram\|histogram]] that shows the number of games a football team has had that scored within a particular range. This team had 2 games where they scored 0-9 points, 4 games where they scored between 10-19 points, 5 games where they scored between 20-29 points, 3 games where they scored between 30-39 points, and 2 games where they scored 40-49 points.
```chart
type: bar
labels: [0-9 Points,10-19 Points,20-29 Points,30-39 Points,40-49 Points]
series:
  - title: Number of Games
    data: [2,4,5,3,2]
tension: 0.16
width: 80%
labelColors: false
fill: false
beginAtZero: true
bestFit: false
bestFitTitle: undefined
bestFitNumber: 0
```
In total, the team has played $2+4+5+3+2=16$ games so far. They are about to play their 17th game. What is the probability that they will score more than 30 points in their 17th game, i.e. $P(points\geq30)$?

According to the data above, the team had $3+2=5$ games where they scored more than 30 points. Therefore, the experimental probability of them scoring more than 30 points in their next game is:
$$
P(points\geq30)=\frac{5}{16}
$$
Remember that the above probability is just an estimate based on past experiential data. Things might have changed since their 16th game that could affect the outcome.
