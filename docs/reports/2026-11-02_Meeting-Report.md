# 2026-11-02_Meeting-Report

| Item | Content |
|------|---------|
| Name | Tom Morschheuser |
| Meeting Date | 2026/11/02 |
| Previous Meeting Date | 2026/10/26 |
<!-- 
---

> **Notes on preparing this document**
>
> - **Write in proper sentences as much as possible.** Do not rely on bullet points alone; use prose where explanation is needed. If you cannot put something into clear sentences, there is a good chance you have not yet organized your own thinking well enough.
> - **Define the terms you use strictly.** Starting a discussion with ambiguous terms often leads to apparent agreement that turns out to be a misunderstanding. Always give explicit definitions for terms introduced for the first time, terms you define yourself, and terms that are used differently from prior work.
> - **When you include calculation or analysis results, upload the corresponding code separately to GitHub and provide a reference link in this document.** Without the code, the reproducibility and reliability of the results cannot be verified. Every figure, table, and numerical result must be accompanied by a link to the script that generated it.

---
-->
## 1. What I Want to Discuss Today (Most Important)

<!-- List 1–3 things you most want to discuss. These are the goals of this meeting. -->
<!-- Be explicit about what kind of decision or advice you are asking for. -->

1. Literature Review
2. Breaking down research proposal
3. Further steps

## 2. Current Situation (Progress Since Last Meeting)

<!-- What have you done since the last meeting? -->
<!-- It is useful to list both what you did and what you could not do (and why). -->

Since the Last meeting, I skimmed through the literature and analyzed 3 papers to find a specific research gap

### What I did

- I went through my paper stack and investigated the top 3 papers
- Topics of the Papers 
  - [Marl for Evacuation](2026-11-02-Files/MARL_For_Evacuation.md)
  - [Marl for Tsunami Evacuation](2026-11-02-Files/MARL_For_Tsunami_Evacuation.md)
  - [Short Term Traffic Prediction](2026-11-02-Files/Short-Term-Traffic_Prediction.md)
  - These papers have in common, that they do not consider "realistic" crowd behavior (panic, non obedience, habits) and evacuation strategies. Instead they focus on the policy adapted by rl. The last paper is not for simulations
  - 
- Extracted singular topics from my research proposal
  
| Topic | Broad Question | Possible Gap |
| :--- | :--- | :--- |
| Simulating Traffic | What is the History in Simulating Traffic and what are current best practices | | |
| Reward Function Design | How can a reward function be designed to encourage efficient route prediction | 
| Multi Agent System | How can Simulation Algorithms complement reinforcement Learning agents to reduce the amount of agents |
| System Scalability | How can a single-agent-system scale to multi agent system |
| Disruption Modeling | How can Infrastructure Disturbances be modeled stochastically |
| Baseline Comparison | How does reinforcement learning compare to deep learning approaches | 
| State Definition | How does an agent perceive the network | 
| Evacuation Policies | What are major Evacuation Policies and how can they be used in collaboration with reinforcement learning


### What I could not do / What is delayed

- Identify a gap in the literature I want to pursue
- Defining a problem statement

## 3. Definitions of Terms

<!-- Define the key terms used in this document here. -->
<!-- Be especially explicit about terms you define yourself or terms that can be ambiguous. -->
- MARL: Multy Agent Reinforcement Learning

## 4. My Own Thoughts

<!-- For each item in Section 1, write your current thinking. -->
<!-- It does not need to be correct — the *process* of thinking is what matters. -->
<!-- Use prose where bullet points alone are insufficient. -->

### On Literature review

- **Current thought**: The field of MARL applications in disaster evacuation has only a few applications. For modeling realistic traffic behavior, there seems to be no application. However I still struggle to find a useful reason to model realistic traffic behavior in this context. Whats also not mentioned in these 3 papers are evacuation strategies
- **Reasoning**: The paper mentioned in [Marl for Evacuation](2026-11-02-Files/MARL_For_Evacuation.md) seems to be the only application of MARL in evacuation scenarios using microscopic vehicle simulation. 
- **Alternatives I considered**: I am currently also considering a "global" model to optimize evacuation policies. However, I have not considered literature for this yet.

### On breaking down research proposal

- **Current thought**: The research proposal is so broad, that I broke it down into sub-questions.
- **Reasoning**: Clarity reasons
- **Alternatives I considered**: Until now, none

## 5. Where I Am Stuck / What I Cannot Decide on My Own

<!-- Articulate where you are stuck and why you cannot decide on your own. -->
<!-- Making the *type* of being stuck explicit (e.g., "not enough information", "no clear criterion", "too many options") helps the discussion. -->

- Stepping away from MARL, I am not really sure in which direction to go with the literature, as there are so many applicable fields.
However, I also have not read a lot to this point.

## 6. Things I Want to Confirm

<!-- If there are simple questions or confirmations (not discussions), list them here. -->

- Are these papers too specific

## 8. Supplementary Materials

<!-- Add links to references, related materials, and past discussion notes as needed. -->

- The paper A Multi-agent Reinforcement Learning Approach for Population Routing Optimization during Disaster Evacuation is only available with IEEE. If access is needed, please ask me


## Action Items for Next Meeting (fill in after the meeting)

<!-- Note these during or right after the meeting so they can be matched against "What I did" in the next document. -->

- [ ] 
- [ ] 
- [ ] 