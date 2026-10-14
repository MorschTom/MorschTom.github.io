# Research Proposal

<h2> Simulating Evacuation Traffic with Reinforcement Learning </h2>

Rapid and safe evacuation during large-scale natural disasters is critical. Short-term
traffic routing combined with congestion prediction can support evacuation planning by
maintaining smooth traffic flow and minimizing total evacuation time. In this context,
traffic flow simulations allow the prediction of congestion in advance and enable
preemptive vehicle rerouting. While recent advances in reinforcement learning have
demonstrated promising results in simulating multi-agent behavior in dynamic
environments [@DRLCrowd2018], most existing research focuses on crowd simulations for entertainment
applications. This study proposes to apply similar reinforcement learning approaches to
simulate traffic routing during natural disaster evacuation scenarios and evaluate its
performance against deterministic and deep learning-based approaches.

### Problem Statement

Predicting traffic behavior has been extensively studied, with many approaches effectively
modeling recurrent congestion in relatively stable conditions, such as disruptions caused
by construction sites or accidents. However, these approaches are often not designed to
model highly dynamic conditions that occur during natural disasters. Although deep
learning techniques have been applied to dynamic traffic prediction, they rely primarily
on historical traffic patterns and may fail to adapt to rapidly changing conditions during
disasters. This study investigates whether reinforcement learning can effectively guide
traffic routing under such dynamic conditions. Specifically, the research addresses the
following questions:

* How can a reward function be designed to encourage efficient route prediction and
how can this function be integrated into a traffic simulation framework like SUMO [@SUMO2018]?
* How can infrastructure disturbances caused by natural disaster be modeled, for
example using stochastic approaches?
* How can the system be efficiently scaled to simulate large traffic networks?
* How does the reinforcement learning approach compare with existing deep learning methods?

### Objectives

The long-term goal of this research is to develop a simulation framework for routing
multiple agents through traffic networks during natural disasters. In this framework,
disaster conditions will be modeled as stochastic disruptions to the road network. The
present study focuses on evaluating whether reinforcement learning can reduce
evacuation time and congestion compared to deterministic and deep learning approaches
in disaster-affected traffic networks. Specifically, it aims to design and evaluate a
reinforcement learning approach that guides agents through non-recurrent congestion scenarios.
To achieve this objective, this study will address the following tasks:

* Conduct a comprehensive review of existing traffic simulation methods.
* Develop and implement a reward function to guide agents through disruptive traffic within a traffic simulation framework such as SUMO [@SUMO2018].
* Compare the proposed approach with existing traffic simulation methods.
* Evaluate the method through simulation experiments measuring evacuation time, traffic congestion levels, and routing efficiency.
  
This study is expected to contribute to transportation research and disaster management
planning. From a practical perspective, the results may support development and
evaluation of traffic management strategies, and identify potential congestion risks
during large-scale evacuations.

### Existing Research

A preliminary literature review shows that traffic prediction has been widely studied, and
many recent studies have applied deep learning techniques to model traffic dynamics. For
example, Xiaolei et al. [@MA2015187] used a Long Short-Term Memory (LSTM) neural network to
predict short-term traffic under regular conditions. In addition, Zemian et al. [@ke2024interpretablemixtureexpertstime] applied
a Mixture of Experts (MoE) model with a Temporal Fusion Transformer backbone to
predict both recurrent and non-recurrent traffic flow. In parallel, reinforcement learning
has gained popularity to simulate realistic crowd behavior. For example, Lee et al. [@DRLCrowd2018]
proposed a framework for simulating pedestrian interactions using Q-learning. To the
best of our knowledge, methodologies using reinforcement learning to simulate traffic
routing during non-recurrent congestion remains limited. Therefore, this study aims to
investigate whether reinforcement learning can be applied to simulate and predict traffic
behavior in disaster evacuation scenarios. This objective will be addressed by developing
a reinforcement learning-based simulation approach for guiding multiple agents through
disruptive traffic conditions.

### Research Methodology

This study primarily employs literature review and simulation-based modeling to develop
a framework and reward function for agent-based traffic simulation. This reward function
will be implemented within a traffic simulation framework to create a working proof-of-
concept model that initially simulates a single agent. This initial step will evaluate
whether the reward function can successfully guide an agent towards an evacuation goal.
In the second phase of this study, stochastic approaches for modeling disaster-related
infrastructure disruptions will be analyzed and implemented into the traffic simulation
framework. Additionally, the proof-of-concept will be extended to a small-scale multi-
agent system to simulate dynamic systems while minimizing computational costs. The
performance of the proposed method will be evaluated using metrics such as evacuation
time, traffic congestion levels, and route efficiency.
In the last phase, alternative approaches based on deterministic traffic models and deep learning methods will be
determined and compared to the reinforcement learning solution.

### Research Schedule

This study will be conducted between October 2026 and July 2028 as part of a master’s
research program. The main sub-goals are planned as follows:

* 1st semester: Perform a comprehensive literature review on reinforcement
learning for agent behavior, traffic simulation frameworks, and recent methods for
predicting traffic events. Refine the research question and define the system
design.
* 2nd semester: Develop the reward function, implement a proof-of-concept model,
and investigate stochastic methods for simulating disaster events.
* 3rd semester: Implement disaster scenarios within the simulation environment,
extend the model to multiple agents, and analyze the simulation results.
* 4th semester: Compare the proposed model with other traffic simulation
approaches, write the thesis, finalize the manuscript, and prepare for thesis
defense.
