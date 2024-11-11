---
{"dg-publish":true,"permalink":"/Math/Probability Theory/What is Probability/","created":"2024-11-03T01:22:52.213-05:00","updated":"2024-11-10T21:48:48.836-05:00"}
---


#Math/Probability

Probability is simply the measure of how likely a certain outcome will occur when we are uncertain about what will happen.

For example, let's say I have a fair coin, which means that each side has an equal chance of landing facing upwards. The probability of getting heads can be denoted as $P(H)$. Probability is about the chances of a random event occurring.

$$
\text{Probability}=\frac{\text{number of possibilities that meet my conditions}}{\text{number of possibilities}}
$$
In the case of the coin flip:
- The number of possibilities is 2 (the coin could either land on heads or tails)
- The number of possibilities in which the coin lands on heads is 1
$$
\therefore P(H)=\frac{1}{2}=50\%
$$
Another way to conceptualize probability is to run an event numerous times and to find the proportion of those recurring events in which your conditions are met. To use the coin example: 50% represents the proportion of coin flips that would land on heads if I flipped the coin many times repeatedly. The greater number of times I run the experiment (i.e. flip the coin), the closer the proportion of times it lands on heads will be 50%.

The set of possible outcomes is known as the *sample space*, and the number of possible outcomes is the size of the sample space.

A *trial* refers to an instance in which you "run" a simulation to obtain an outcome.

## Basic Rules of Probability

1. A greater value of $P(A)$ means that event $A$ is more likely to occur.
2. The probability of an event $A$ can only be between 0 and 1, where a probability of 0 means it is impossible while a probability of 1 means it is certain to happen:
$$
0\leq P(A)\leq 1
$$
$$
P(A)=0\rightarrow \text{It is impossible for $A$ to occur}
$$
$$
P(A)=1\rightarrow\text{It is certain that $A$ will occur}
$$
## Practice Examples

### Example 1

Suppose you have a bag with 9 red marbles, 2 blue marbles, and 3 green marbles. What is the probability of randomly selecting non-marble from the bag.

Let us denote $R$, $B$, $G$ as the event of picking a red, blue, and green marble respectively in a trial. The sample space can be represented as 
$$\{R,R,R,R,R,R,R,R,R,B,B,G,G\}$$
The size of the sample space is $9+2+3=14$, which is also the total number of possible outcomes. The number of those possibilities that meet our conditions of picking a non-blue marble is simply the sum of red and green marbles in the bag: $9+3=12$.

Given the above, the probability of selecting a non-blue marble from the bag is:
$$
P(\neg B)=\frac{\text{number of non-blue marbles in the bag}}{\text{number of marbles in the bag}}=\frac{12}{14}=\frac{6}{7}
$$

### Example 2

Note that probability does not always deal with discrete quantities. Consider this scenario: A large circle of area $324\pi$ contains a smaller circle of area $16\pi$. If you were to pick a random point within the larger circle, what is the probability that point also lies inside the smaller circle?

The probability that the chosen point lies in the smaller circle can be represented as a proportion of the area of the large circle that is occupied by the area of the smaller circle. Thus,
$$
P(S)=\frac{\text{Area of Small Circle}}{\text{Area of Large Circle}}=\frac{16\pi}{324\pi}=\frac{4}{81}
$$
