---
title: "Hedging Autocallable Notes with Deep Reinforcement Learning"
excerpt: "Developed a deep reinforcement learning model using the deep deterministic policy gradient algorithm to delta and 
gamma hedge auto-callable notes. The Loss distribution of the final model had a standard deviation 10% lower than that of the baseline hedging model."
collection: portfolio
date: 2024-04-01
---
EXECUTIVE SUMMARY 
Autocallable Notes are a popular type of structured and are attractive because they offer 
higher returns than traditional bonds while still offering the principal protection that bonds offer 
(Cuim et al. 2023). This greater return comes from the fact that a standard autocallable note pays 
a coupon (C) if the underlying asset of the note (S) is greater than a value called the coupon 
barrier (CB) at an observation date (OD). An autocallable note also gets automatically called if 
the underlying asset is greater than a value, which is called the autocall barrier (AB), at a given 
observation date. If the autocallable note is automatically called at an observation date or the 
note reaches its maturity date, the investor will receive the face value of the note. The structure 
of the autocallable note’s payoff leads to difficult problems within the area of risk management. 
The Delta, which is the change in the price of the autocallable note with respect to the change in 
the price of the underlying asset and is a measure used for hedging of autocallable note, can 
increase to large values when the underlying asset approaches the barriers because of the 
discontinuous nature of the payoffs. The Gamma, which is the change in the notes Delta with 
respect to the change in the underlying asset, around the barriers also increases and decreases to 
large and small amounts because of the movement of Delta around the barriers. Delta and Delta
Gamma Neutral dynamic hedging is difficult because of these barriers and can lead to a large 
standard deviation in profit and loss distributions, as large amounts of the underlying or hedging 
option may be bought when hedging near the barriers. Therefore, strategies that address this 
issue would be valuable as they would lead to more optimal hedging. Dynamic Delta and Delta
Gamma hedging can be framed as a sequential decision-making process within a stochastic 
environment. This type of problem is able to be addressed by an area within Machine Learning 
called Reinforcement Learning. This paper uses a Deep Reinforcement Learning (DRL) 
algorithm called Deep Deterministic Policy Gradient (DDPG) to Delta and Delta-Gamma hedge 
two different autocallable notes. Three experiments were conducted in which a DDPG model 
was trained to either Delta hedge or Delta Gamma hedge an autocallable note. Each trained 
model was then compared to the baseline Delta Neutral or Delta-Gamma Neutral model. This 
comparison was done using each model's Profit and Loss distribution over many hedging trials. 
The results of the experiments show the viability of using DRL to hedge an autocallable note. 
Another experiment was done to explore the importance of hyperparameter tuning when training 
a DDPG model. In this experiment the optimal hyperparameters for a DDPG Delta-Gamma 
III 
hedging model were found and compared to the baseline hedging model. Future work is 
suggested to explore the use of different DRL algorithms, hedging different autocallable note 
structures, using different underlying processes, and using different hedging options when Delta
Gamma hedging.
