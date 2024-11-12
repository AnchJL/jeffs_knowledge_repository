---
{"dg-publish":true,"permalink":"/Math/Probability Theory/The Monty Hall Problem/","created":"2024-11-03T13:20:39.626-05:00","updated":"2024-11-11T21:50:24.934-05:00"}
---


#Math/Probability 

*The Monty Hall Problem* is famous probability problem named after the game show host, Monty Hall.

On Monty Hall's show, a contestant is shown three doors: door \#1, door \#2, and door \#3. Behind one of these three curtains is a valuable prize, often a car. Behind the other two curtains is a pet goat or some other undesirable prize. The contestant is tasked with selecting one of the doors.

Let's say the contestant chooses door \#1 but does not yet open it. The host opens door \#3 to reveal a goat behind it. After revealing that door \#3 does not have the prize car, then host then asks the contestant if they would like to stick with their original choice of door \#1 or if they would like to switch to picking door \#2 instead. Should the contestant switch to doors, or would it not make a difference?

Most people would think switching would not make a difference because they believe there is a 50% chance of door \#2 containing the prize. However, this is incorrect. Switching to door \#2 increases the contestants odds of winning. More generally, switching from your initial choice will always increase the odds of you winning this game.

To see why, suppose that you were playing this game and had the strategy of never switching. This means that the odds of your first selection being the correct choice is $P(W|\text{Don't Switch})=\frac{1}{3}$ while the odds of your first selection being wrong is $P(L|\text{Switch})=\frac{2}{3}$.

In contrast, suppose you played this game with the strategy of always switching. Also suppose that door \#2 has the prize car. Here are the possible scenarios if you always intend on switching:
- If you picked door \#1 and the host revealed that door #3 had the goat, then switching to door \#2 would mean you win. 
- If you picked door \#2 and the host revealed that door #3 had the goat, then switching to door \#1 would mean you lose. 
- If you picked door \#3 and the host revealed that door #1 had the goat, then switching to door \#2 would mean you win.

To summarize, having a strategy of always switching would mean you would win in two of the three scenarios described above. Notice how in order to win under this "always switch" strategy, your first choice must have been incorrect, which has a probability of $\frac{2}{3}$. This means that switching doors increases your chances of winning from $\frac{1}{3}$ to $\frac{2}{3}$.

The table below shows the full range of possibilities and your odds of winning depending on if you switch or don't switch from your initial choice.

|        | Door \# with Prize Car | Your First Choice | Door Revealed by the Host to Have a Goat | Never Switch                | Always Switch               |
| ------ | ---------------------- | ----------------- | ---------------------------------------- | --------------------------- | --------------------------- |
|        | 1                      | 1                 | 3 or 2                                   | Win                         | Lose                        |
|        | 1                      | 2                 | 3                                        | Lose                        | Win                         |
|        | 1                      | 3                 | 2                                        | Lose                        | Win                         |
|        | 2                      | 1                 | 3                                        | Lose                        | Win                         |
|        | 2                      | 2                 | 3 or 1                                   | Win                         | Lose                        |
|        | 2                      | 3                 | 1                                        | Lose                        | Win                         |
|        | 3                      | 1                 | 2                                        | Lose                        | Win                         |
|        | 3                      | 2                 | 1                                        | Lose                        | Win                         |
|        | 3                      | 3                 | 1 or 2                                   | Win                         | Lose                        |
| $P(W)$ | N/A                    | N/A               | N/A                                      | $$\frac{3}{9}=\frac{1}{3}$$ | $$\frac{6}{9}=\frac{2}{3}$$ |
| $P(L)$ | N/A                    | N/A               | N/A                                      | $$\frac{6}{9}=\frac{2}{3}$$ | $$\frac{3}{9}=\frac{1}{3}$$ |
