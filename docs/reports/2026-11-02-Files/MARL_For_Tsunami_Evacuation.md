# Optimizing evacuation paths using agent-based evacuation simulations and reinforcement learning

## Metadata

Authors: Tomoyuki Takabatake * , Keito Asai , Hiroki Kakuta , Nanami Hasegawa <br>
Release Date: 2025/01 <br>
Journal: International Journal of Disaster Risk Reduction <br>

## What they did


+ Simulate Agent Based Tsunami Evacuation
  + Algorithm optimizes route of individuals that did no safely evacuate
  + Optimizing the policy to select roads, that are affected later by tsunami
  + Also considers congestion levels and evacuation shelter capacity
+ Utilizing worst case scenario (Everybody evacuation at the same time)
+ State Space has knowledge of every node
+ Using Fastest route in first iteration and updating that route for unsuccessful individuals
+ Simulation with agent-based tsunami model
  

## Focus

+ Focus on Tsunami Evacuation
+ Evacuation by foot
+ One policy for each evacuee
+ safe evacuation, not necessarily fast
+ Study area is a costal city Wakayama Prefecture, Japan
  
## Findings

+ Evacuation routing with reinforcement learning tremendously reduce number of casualties
+ High rewards for successful evacuation minimizes casualty rates.
 

## What they did not do

+ utilizing sparse information, The algorithm assumes full knowledge of the network
+ considering vehicles
+ Considering a distribution of evacuation starting points (all start from buildings)
+ Evacuation Speed are not variable (Only considering speed drops in congestion and constant speeds based on age)
+ No utilization of evacuation strategies, only the optimization of the RL
+ No realistic behavior (Like panic)
+ application and test limited to one city and one scenario

## Questions I have

+ Papers states that evacuees use groups of 3, but how do they influence each other? Are they just guided by the same agent and seen as one unit?


[Return to the Meeting Report](../2026-11-02_Meeting-Report.md)