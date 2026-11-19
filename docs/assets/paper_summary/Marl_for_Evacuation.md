# A Multi-agent Reinforcement Learning Approach for Population Routing Optimization during Disaster Evacuation

[Click here to go back to the paper_inventory](../../paper_inventory.md)

## Summary

This study proposes a Multi-Agent Reinforcement
Learning (MARL) model to address the population evacuation
routing problem under information-limited network conditions.
In the proposed formulation, evacuees are organized into groups,
each governed by a distinct RL agent, reflecting realistic social
behavior in which individuals tend to evacuate collectively. The
RL agent groups balance two competing objectives: (i) minimiz-
ing travel time to designated shelters, and (ii) avoiding proximity
to disaster-affected zones. To overcome the limitations of par-
tial observability, the study introduces a transformer-based observation
encoder (OE) that enables information sharing among evacuees
within a group to capture evacuees’ observation relationships
without relying on global network status. This study evaluates the
proposed framework in the microscopic traffic simulation SUMO
to model a population evacuation scenario in the Manhattan
transportation network.

## Environments

### Transportation Network

Defined as a direct graph \(G\).

\(G = (V,E)\)

* \(V\) = Set of Nodes
* \(E\) = Set of Edges

One edge \(e = (u,k) \in E\) denotes direct road from node \(u\) to node \(k\) with 

- \(\forall u,k \in V\)

A set of Nodes \(V\) contains all intersections including origins \(O\) and destination points \(D\) of evacuees as Origin-Destination pairs \(OD\). These are denoted as: 

* Set of Origin notes \(O = \{o_1, ..., o_{|O|}\} \subset V\)
* Set of Destination notes \(D = \{d_1, ..., d_{|D|}\} \subset V\)
* Assumption: \(O \cap D = \emptyset\) (no origin and destination point is the same)

Every \(OD\) pair has a demand denoted as \(de(o,d)\) which modeles evacuees moving from origin to shelter and is taken as given.

Also traffic density is modeled as a vector.

\(f^{e,t} \in \mathbb{R}_+\)

## System State
  
No global Network status, status is set by a markov-decision-game

RL-Agents are trained by a set of experiences defined by:

* Set of individual evacuee Agents: \(I \{i_1,..., i_N\}\)
* Agent groups managed by RL-Agent: \(c \in C\)
* Observation space: \(O = E \times \{0, 1\}^{|E|} \times \mathbb{R}_+\)
* local Observation of each agent: \(\omega^{i,t} = (e^{i,t}_{current}, v^{i,t}_{next}, f^{i,t}_{current}) \in {O}\).
    * \(e\) = current edge, \(v\) = next set of nodes, \(f\) = current congestion level
* Action space: \(A \subset \{0, 1\}^{|E|}\)
    * action \(a^{i,t} \in A\) represents the next chosen edge
* Reward function: \(R : O \times A \mapsto \mathbb{R} \)


## Methodology

Agents are guided by two machine learning models

* Transformer Model for Information Sharing
* Q-Learning Agent for Routing decisions
