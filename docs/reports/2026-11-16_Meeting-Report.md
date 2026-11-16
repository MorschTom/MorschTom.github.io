# 2026-11-16_Meeting-Report

| Item | Content |
|------|---------|
| Name | Morschheuser Tom |
| Meeting Date | 2026/11/16 |
| Previous Meeting Date | 2026/11/09 |

## Results of previous Meeting

| Topic | Description | Scheduled  today |
| :---- | :---------- | :--------------: |
| Decision | Expand on the household goal chaining as a research topic | |
| Literature Review | Expand literature review on household goal chaining during disaster evacuation scenarios. | x |
| Literature Review | Analyze and learn the methodology used by papers that did household chaining like Pamela M. Murray‐Tuite 2003 | x |
| Task | Specify the wording for the problem statement and the research objective | |
| Task | Build a tentative to-do list with time-schedule | x |
| Task | Build a playground schematic for the simulation and environment | |
| Task | Check how TD-Estimation can be integrated into this research theme | |

Todays Topic: research topic and time-schedule.

## Done

### Time Schedule

This time scheduled is designed to be expanded in the future.

| Due | Meeting No | Task | description |
| :-: | :--------: | :--- | :---------- |
| 11/16 | 4 | analyze the methodology for modeling household chaining | analyze mainly the papers from Murray-Tuite and Mahmassani 2003, 2004. |
| 11/23 | 5 | verify the research gap | perform further literature review (starting point: Murray-Tuite and Mahmassani 2003, 2004). |
| 11/23 | 5 | Outline for playground | define an outline for a playground schematic the simulation and environment can be based on. |
| 11/30 | 6 | small literature review | perform literature review on reinforcement learning and agent based simulation methods to specify the research objective |
| 11/30 | 6 | Define the research objective | Use the insights from previous tasks to formulate the research objective into proper wording |
| 12/02 | | Presentation | prepare seminar presentation |
| 12/7 | 7 | Check the TD-Estimation | Do another literature review to check if or how TD-Estimation can be incorporated into this research scheme. |
| 12/14 | 8 | Playground Schematic | Build the playground schematic for the simulation |
| ~2027/01 | | Abstract for 0.5 Project | |


### Methodology of Murray Tuite

two sequential linear integer program with a dynamic traffic assignment-simulation tool (DYNASMART-P)

Simulation is done in 4 steps

1. Calculate expected travel time to the destination using k-shortest-path algorithm
2. Calculate a optimal meeting location with a linear Integer program for all household members with car. Goal is to minimize the maximum travel time for each member.

      - Meeting locations are parks, shopping centers...
      - Problem is solved based on an evoked network (not the actual network, combination of perceive travel times and informations of actual network) specific to each household, using the perceived travel times from k-shortest-path
      - Linear integer program minimizes the perceived travel time to the meeting location from every family members location
          - constraints are the maximum perceived travel time for every meeting location, only one location, maximum distance to every member and minimum distance to disaster zone
          - The meeting location determined by this is used to compute vehicle routing

**3. Second Linear Integer Program solves a vehicle routing problem.**

- vehicle routing problem is formulated as a traveling salesman problem
    - People with vehicles are salesmen, people without vehicles are customers
    - Salesman starts at home and visits every customer exactly once
    - vehicles should reach the meeting location at a similar time

$$
\min
\sum_{k,l \in C} \left| 
\sum_{i,j \in N} t_{ij}x^{k}_{ij}
-
\sum_{i,j \in N} t_{ij}x^{l}_{ij} \right|
$$

* Indices for the vehicles are denoted by k and l.
* C is the set of vehicles available to household h. 
* The decision variables are $x^{k}_{ij}$ which take the value one if vehicle k uses the hyperlink connecting nodes i and j.
* $t_{ij} is the perveived travel time between nodes i and j.
* $N$ is the set of Nodes in the Graph.

- Also optimizes the amounts of vehicles in the network at the same time with a similar formulation.
- The results of this program are fed into travel simulation.

**4. Travel simulation with DYNASMART-P. Drivers may resequence en route. But The second Linear Integer Program is not rerun.**

- Not specific, just uses routing from the simulation environment. New strategy is not developed, just adjustments to the route using real time information
- Test Network is in Texas, south-central Fort Worth
- 5 Test Groups (1-2 Drivers, 1-3 Children, 1-3 Pickup locations)

**System State**
- No Formal System State, implicitly defined through inputs
- Network State
    - Travel times calculated on everyday traffic times are used as perceived travel times.
    - Perceived travel time is used as basis for the pickup point calculation.
    - every used node connection has a perceived travel time.
- Household state
    - perceived travel times
    - Vehicle fleet with seat capacity
    - Network Information: Meeting locations, start locations of vehicles, current location of members.
- Hazard State
    - Static Hazard locations, so far away, that not influencing the pickup locations
- En Route Rerouting
    - only conceptually, using the logic of the simulator
    - not mentioned how rerouting functions or is triggered
    - Retriggering of Second Linear Integer program is possible, but not part of this papers scope

### Research Focus

Statement from this paper is what I want to focus on:

"Depending on
information supply strategies, and the particular problem formulation and operational
scenario, the drivers may make changes to their original plans. Those may call for re-
application of the preceding step; however such iterative schemes are outside the scope of
the present paper."

## Delayed

Still working on skimming the literature on household chaining.

Tentative results as follows:

- Minimizing maximum travel time for each household member through picking a optimal meeting locations where every member meets and optimizing the pickup order and who picks up who through 2 linear Integer Programs. Also household waits at a meeting place in the danger zone for every car to arrive. (M. Tuite)
- Stated, that en route routing of pickups and communication is still open research question (Pel et al.)

## Discussion Results

## References

Murray-Tuite, Pamela M., and Hani S. Mahmassani. "Model of household trip-chain sequencing in emergency evacuation." Transportation Research Record 1831.1 (2003): 21-29.

Pel, A.J., Bliemer, M.C.J. & Hoogendoorn, S.P. A review on travel behaviour modelling in dynamic traffic simulation models for evacuations. Transportation 39, 97–123 (2012). [10.1007/s11116-011-9320-6](https://doi.org/10.1007/s11116-011-9320-6)