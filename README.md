# Breast_Cancer_probability_RL

This Repository contains data of 10000 women's probability of cancer at early stage and advanced stage at each mammogram screening along with state transition probabilities.
Patoents start screening at age 40 and goes under screening each year as recommendation.

### file 1: "all_women_data.csv"

#### Data Dictionary:
Patient ID	- ID of patient  
Age	- Age of patient at time of screening  
State 0 (Healthy)	- probability of women being Healthy(No Cancer)  
State 1 (Early Cancer)	- probability of women having early stage cancer  
State 2 (Late Cancer)	 - probability of women having advance stage cancer  
State 3 (Cancer Death)	- probability of death from cancer  
State 4 (Other Death)	- probability of death from other causes  
Risk Score - risk score is calculated using [(1 - probability of being healthy) * 100] - This risk scores can be used as states in RL models

### file 2: "state_transition_probabilities"

This file contains state transition probabilities at each age for RL model for Regular Mammogram and Biopsy actions.   
It considers cancer risk score as a state of RL model(i.e. MDP) and calculate teansition probabilities of states at different age.

#### Data Dictionary:

Age - Age of patient  
From State - current state of patoent (current risk score)  
To State - future state (otehr risk scores)  
Probability - probability of transitioning from one state to another state  
