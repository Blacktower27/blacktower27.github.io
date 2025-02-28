---
title: "Container Scheduling with Dynamic Computing Resource for Microservice Deployment in Edge Computing"
collection: publications
category: conferences
permalink: /publication/container-scheduling/
excerpt: "This paper proposes a reinforcement learning approach to optimize microservice scheduling in edge computing environments, improving efficiency by 65%."
date: 2024-02-28
venue: "MSN 2024 - 20th International Conference on Mobility, Sensing and Networking"
authors: "Jingxi Lu, Wenhao Li, Jianxiong Guo, Xingjian Ding, Zhiqing Tang, Tian Wang"
citation: "J. Lu, W. Li, J. Guo, X. Ding, Z. Tang, and T. Wang, 'Container Scheduling with Dynamic Computing Resource for Microservice Deployment in Edge Computing,' in MSN 2024."
paperurl: ""
status: "Accepted, awaiting publication"
---

With the massive increase of Internet of Things devices and their data, executing applications by using **microservice architecture** has emerged as the predominant trend. 

As container technology evolves, microservices can be lightweightly deployed in resource-constrained edge nodes. However, existing container scheduling algorithms often **overlook the allocation of computing resources on edge servers**. When multiple containers are assigned to an edge node, it is usually assumed that they share a **uniform CPU frequency**, which is **unrealistic**.

In this paper, we first **formulate an online container-based microservice scheduling problem** with dynamic computing power to **minimize total delay and energy consumption**, where we need to determine:
1. The **assignment between microservices and edge nodes**.
2. The **allocation of computing power** to each microservice.

We propose a **Soft Actor-Critic (SAC) based reinforcement learning algorithm** to address this problem, integrating:
- A **GRU unit** in the policy network to capture decision correlation.
- An **action selection mechanism** to **accelerate convergence**.

Finally, we implemented a **simulated scheduling system**, demonstrating that our algorithm **outperforms commonly used baselines by up to 65%** in terms of the total objective.
