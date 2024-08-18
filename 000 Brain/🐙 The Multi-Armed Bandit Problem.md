---
Created On: 2023-08-28, 08:34
Unique ID: 202308280834
---

**Tags:** #DefinitionCards 

# 🐙 The Multi-Armed Bandit Problem

#### What is the Multi-Armed Bandit Problem?
?
Given a set of competing or alternative choices with unknown outcomes and the ability to simultaneously utilize a limited number of options, how do you learn enough about the system to maximize your results? 
i.e., how valuable is the "exploration" of a choice vs. the "exploitation" of a choice.
Suppose a gambler only plays one slot machine in the casino. In that case, they are increasing the likelihood of success on that machine but throwing out the possibility of finding a machine with a much higher payout period. If they play every machine only once, they have almost no chance of leveraging the machine with the highest payout.
There are optimal statistical solutions to the problem, but the real-life implementation (i.e. choosing a job) of this problem introduces enough volatility such that **it is impossible to find an optimal solution.** 
The most common solution is to explore the things that we have the least confidence about, because this can teach us the most.
<!--SR:!2024-12-18,180,250-->


Opinions about the problem

1. It is impossible to have complete information in real life 
2. It takes courage to choose an option to exploit, but decisive exploitation can also lead to more options to experiment
3. You learn the most during the exploitation phase
4. Example - people don’t take exit row seats on southwest flights. 


---
# References
[[📗 Optionality - Survive and Thrive]]
[Wiki](https://en.wikipedia.org/wiki/Multi-armed_bandit)
