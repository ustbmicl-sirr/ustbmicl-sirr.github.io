---
title: 研究方向
type: landing

sections:
  - block: markdown
    content:
      title: ""
      text: |
        ## 小组主线

        面向**跨域、部分可观测**的机器人群体主动导航：研究如何由局部观测推断环境、链路、角色与域参数的结构化后验，如何据此联合选择可执行协作边与动作，以及任务—协作结构如何在仿真到真实迁移中保持、适应与恢复。

        > **用概率因子图认识不确定世界，用 GraphSwarm 形成协作结构，用离在线多智能体学习实现可验证 Sim2Real 主动导航。**

        ---

        > **News** | ICASSP 2026 · Hierarchical MARL for Task Allocation
        > Heng Zhang, Shihong Duan, Yadong Wan · Barcelona · [DOI](https://doi.org/10.1109/ICASSP55912.2026.11462585)

  - block: features
    content:
      title: 主要工作
      text: 当前证据链上的四层工作（语义 SLAM / VLA 为后续扩展）
      items:
        - name: 结构化推断
          icon: project-diagram
          icon_pack: fas
          description: |
            **动态概率因子图**

            对状态、地图、链路、角色与域参数做后验推断；明确随机变量、势函数与推断算法。

            [详情](#inference)
        - name: 协作涌现
          icon: sitemap
          icon_pack: fas
          description: |
            **GraphSwarm**

            可执行协作结构（感知 / 通信 / 任务边）的形成、保持、失效与恢复。

            [详情](#graphswarm)
        - name: 离在线决策
          icon: robot
          icon_pack: fas
          description: |
            **DT + Graph-MARL**

            离线长时行为先验与在线分布式残差适应；支撑寻源、任务分配与主动探索。

            [详情](#decision)
        - name: 可验证迁移
          icon: exchange-alt
          icon_pack: fas
          description: |
            **Sim2Real**

            物理校准更新域相关因子；在规模、通信与真实平台上验证迁移，而非只报仿真成功率。

            [详情](#sim2real)

  - block: markdown
    id: inference
    content:
      title: ""
      text: |
        ---
        ## 结构化推断 · 动态概率因子图

        因子图用于部分可观测群体的**后验推断**，不把任意关系图或注意力矩阵泛称为因子图。

        | 隐变量 | 含义 |
        |:---|:---|
        | \(X_t\) | 机器人状态 |
        | \(M_t\) | 地图 / 目标 / 环境 |
        | \(C_t\) | 通信链路可靠性 |
        | \(R_t\) | 角色或协作意图 |
        | \(\Theta_t\) | 动力学、观测与通信域参数 |

        相关论文：[因子图引导的不确定性感知 SLAM 探索](/zh/publication/factor-graph-slam/)

  - block: markdown
    id: graphswarm
    content:
      title: ""
      text: |
        ---
        ## 协作涌现 · GraphSwarm

        科学对象是**可执行协作结构**：动作会同时改变位置、未来观测、通信拓扑与任务协作关系。

        | 图 | 回答的问题 |
        |:---|:---|
        | 感知图 \(G^{\mathrm{sen}}\) | 谁观测谁 / 观测质量 |
        | 通信图 \(G^{\mathrm{com}}\) | 谁能与谁可靠通信 |
        | 任务图 \(G^{\mathrm{task}}\) | 谁与谁协作完成子任务 |

        **代表产出**：源导航 CG-MCTS（IROS 2026，录用）；协同定位与跟踪中的因子图 / 协调结构（JSAC / IoT-J, 2024）


  - block: markdown
    id: decision
    content:
      title: ""
      text: |
        ---
        ## 离在线决策 · DT + Graph-MARL

        Decision Transformer 提供可测量的长时行为先验；Graph-MARL 在图约束下完成在线分布式适应，而不是把二者写成两条平行主线。

        相关论文：[基于子目标的多智能体分层强化学习](/zh/publication/subgoal-collaboration/)、[分布式任务分配](/zh/publication/icassp-2026-hierarchical-marl/)

  - block: markdown
    id: sim2real
    content:
      title: ""
      text: |
        ---
        ## 可验证迁移 · Sim2Real

        用 PINN / 系统辨识更新域相关动力学与观测因子；优先研究交互结构与观测/通信因子变化，动力学偏移作为物理校准因素。

        相关论文：[视觉导航域适应](/zh/publication/sim2real-navigation/)、[学习驱动的多机器人主动 SLAM：概念框架与综述](/zh/publication/active-slam-survey/)

  - block: markdown
    content:
      title: 边界
      text: |
        - 当前**不**把 Graph-Semantic SLAM / VLA、通用涌现理论或工业 IoT 升为并列主科学问题。
        - 无线信道与嵌入式感知是群体通信/部署的**支撑能力**，服务主线验证，不单独叙事。
        - 非平凡性来自新科学对象、作用机理与可辨识/迁移边界，而非堆叠网络与 loss。
---
