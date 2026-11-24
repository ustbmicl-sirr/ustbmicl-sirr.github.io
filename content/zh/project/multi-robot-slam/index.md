---
title: 多机器人协同 SLAM
summary: 学习驱动的多机器人主动 SLAM 与不确定性感知探索
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

## 机器人下一步该去哪里？

两台机器人探索一条陌生走廊时，可以分头进入不同房间以扩大地图，也可以重访同一扇门，利用共同观测校正相对位置。主动 SLAM 研究如何在获取新信息和降低已有地图的不确定性之间做选择。

![协作 SLAM 中感知、估计、决策与控制的闭环](/media/sirr/active-slam-framework.png)

图中，估计模块根据观测更新机器人位姿和地图，决策模块据此选择下一步动作。机器人移动后，新观测又进入估计模块。图引自 Bowen Lv、Shihong Duan 的[综述图 1](https://doi.org/10.3390/app16031412)，采用 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) 许可。

## 已发表工作

- [学习驱动的多机器人主动 SLAM：概念框架与综述](/zh/publication/active-slam-survey/) (Applied Sciences 16(3), 1412)。综述将分布式状态估计与机器人探索决策放在同一框架下，比较各个模块及完整系统在仿真和真实机器人上的验证进展。
- [因子图引导的不确定性感知 SLAM 探索](/zh/publication/factor-graph-slam/) (IEEE/RSJ IROS 2026)。这项工作研究如何利用因子图提供的 SLAM 估计信息，引导强化学习策略在选择探索动作时考虑不确定性。
- [未知环境中基于图的自主探索决策学习可解释性研究](/zh/publication/graph-exploration/) (IEEE ISPA 2024)。机器人为什么选择某个位置作为下一步探索目标？这项工作研究如何解释基于图表示的自主探索决策。

## 哪些环节已有实机验证？

综述表 3 汇总了文献中的验证情况。因子图后端和前沿探索规划都有多机器人部署记录；将估计与决策集成后，多机器人实机验证仍然有限。读实验结果时，应区分单个模块的表现与整套系统的表现。[查看原表](https://www.mdpi.com/2076-3417/16/3/1412#table_body_display_applsci-16-01412-t003)
