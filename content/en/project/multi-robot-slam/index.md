---
title: Multi-Robot Cooperative SLAM
summary: Learning-based multi-robot active SLAM and uncertainty-aware exploration
tags:
  - SLAM
  - Multi-Robot
  - Swarm Intelligence
date: '2024-01-01'

external_link: ''

image:
  caption: ''
  focal_point: Smart
---

## Where should the robots go next?

Two robots exploring an unfamiliar corridor could enter different rooms to extend their map. They could also revisit the same doorway to correct their relative poses using a shared observation. Active SLAM asks how to choose between discovering new space and reducing uncertainty in the map already built.

![Feedback loop connecting perception, estimation, decisions and control in collaborative SLAM](/media/sirr/active-slam-framework.png)

Follow the loop from estimation to decision and back. Each robot uses its current pose and map estimates to choose an action. Moving changes what it can observe next. Figure 1 from the [survey by Bowen Lv and Shihong Duan](https://doi.org/10.3390/app16031412), licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## Published work

- [Learning-Based Multi-Robot Active SLAM: A Conceptual Framework and Survey](/publication/active-slam-survey/) (Applied Sciences 16(3), 1412). The survey connects distributed state estimation with decentralized decisions about where to explore. It compares the evidence for individual components and for complete systems in simulation and on robots.
- [Factor Graph Guided Deep Reinforcement Learning for Uncertainty Aware SLAM Exploration](/publication/factor-graph-slam/) (IEEE/RSJ IROS 2026). This work studies how uncertainty in SLAM estimates can guide a reinforcement learning policy as it selects the next exploration action.
- [Explaining Graph-based Decision Learning for Autonomous Exploration in Unknown Environments](/publication/graph-exploration/) (IEEE ISPA 2024). How can a robot explain its choice of where to explore next? The paper studies this question for exploration policies that represent an unknown environment as a graph.

## Which components have been tested on robots?

Table 3 of the survey compares validation across the literature. Factor-graph backends and frontier planners both have established multi-robot deployments. Evidence from physical robot teams is more limited when estimation and decision-making are evaluated together. [See the original table](https://www.mdpi.com/2076-3417/16/3/1412#table_body_display_applsci-16-01412-t003).
