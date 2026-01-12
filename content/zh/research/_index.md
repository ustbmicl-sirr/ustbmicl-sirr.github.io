---
title: 研究方向
type: landing

sections:
  - block: markdown
    content:
      title: 研究方向
      subtitle: 群智能与多智能体系统
      text: |
        ## 研究架构

        ```
        ┌────────────────────────────────────────┐      ┌────────────────────────────────┐
        │         关键技术层 Core Technologies    │      │    学习范式层 Learning Paradigms│
        ├────────────────────────────────────────┤      ├────────────────────────────────┤
        │                                        │      │                                │
        │  MARL + Robots    Swarm Intelligence   │      │  PINN         Federated RL     │
        │  ────────────     ──────────────────   │      │  物理信息NN    联邦强化学习     │
        │                                        │      │                                │
        │  • Factor Graph   • Bio-inspired       │ ───► │  Human-in-Loop    Sim2Real     │
        │    因子图           仿生算法           │      │  人在环           仿真到实际   │
        │                                        │      │                                │
        │  • Equivariant    • Consensus          │      └────────────────────────────────┘
        │    GNN 等变GNN      一致性协议         │
        │                                        │
        │  • Manifold       • Mean Field         │
        │    流形             平均场             │
        │                                        │
        └────────────────────────────────────────┘
        ```

        ---

  - block: markdown
    content:
      title: "🤖 MARL + Robots"
      text: |
        | 研究任务 | 核心问题 |
        |:---|:---|
        | **协同定位 (Localization)**: 多机器人/无人机分布式定位、SLAM | 传感器噪声、通信延迟、数据融合 |
        | **协作导航 (Navigation)**: 路径规划、避障、编队控制 | 动态环境、安全约束、实时性 |
        | **协同寻源 (Source Seeking)**: 目标搜索、信号源定位、环境监测 | 稀疏观测、不确定性、Sim2Real |

        **关键技术:** MARL + 优化算法

  - block: features
    content:
      title: ""
      items:
        - name: 因子图 (Factor Graph)
          icon: project-diagram
          icon_pack: fas
          description: |
            基于因子图的概率推理与优化，结合自注意力因子图神经网络(SA-FGNN)实现多智能体协同定位与目标跟踪。
        - name: 等变GNN (Equivariant GNN)
          icon: brain
          icon_pack: fas
          description: |
            E(n)-等变图神经网络编码多智能体几何关系，保证策略对平移、旋转、排列的对称性。
        - name: 流形 (Manifold)
          icon: globe
          icon_pack: fas
          description: |
            基于流形几何的安全约束建模，结合CBF实现安全控制与几何优化。

  - block: markdown
    content:
      title: "🐝 Swarm Intelligence"
      text: |
        | 研究任务 | 核心问题 |
        |:---|:---|
        | **涌现行为 (Emergent Behavior)**: 从简单规则产生复杂集体行为 | 行为设计、可预测性、稳定性分析 |
        | **自组织协调 (Self-Organization)**: 无中心化的群体决策与任务分配 | 局部通信、全局收敛、可扩展性 |
        | **群体智能优化 (Swarm Optimization)**: 大规模智能体协同搜索与优化 | 计算复杂度、收敛速度、多目标权衡 |

        **关键技术:** 行为树 + 仿生算法

  - block: features
    content:
      title: ""
      items:
        - name: 行为树 (Behavior Tree)
          icon: sitemap
          icon_pack: fas
          description: |
            模块化行为建模框架，支持复杂行为的组合、复用与动态切换，实现可解释的涌现行为设计。
        - name: 仿生算法 (Bio-inspired)
          icon: bug
          icon_pack: fas
          description: |
            蚁群优化(ACO)、粒子群优化(PSO)、蜂群算法等自然启发的分布式优化与涌现行为方法。
        - name: 一致性协议 (Consensus)
          icon: sync-alt
          icon_pack: fas
          description: |
            分布式一致性算法，实现自组织、间接协调(Stigmergy)与全局收敛。

  - block: markdown
    content:
      title: "⚙️ 学习范式"
      text: |
        **跨领域的学习方法与训练框架**：

  - block: features
    content:
      title: ""
      items:
        - name: PINN (物理信息神经网络)
          icon: atom
          icon_pack: fas
          description: |
            将物理定律(PDE/ODE)嵌入神经网络，实现数据高效的动力学建模与安全约束学习(Zubov PDE → CBF)。
        - name: 联邦强化学习 (Federated RL)
          icon: network-wired
          icon_pack: fas
          description: |
            分布式、隐私保护的多智能体训练框架，支持异构数据与去中心化学习。
        - name: 人在环 (Human-in-Loop)
          icon: user-cog
          icon_pack: fas
          description: |
            人机协作的交互式学习，结合人类反馈优化群体控制策略。
        - name: Sim2Real (仿真到实际)
          icon: exchange-alt
          icon_pack: fas
          description: |
            域随机化与域自适应技术，实现从仿真环境到真实机器人的策略迁移。

  - block: markdown
    content:
      title:
      text: |
        ---

        ## 研究理念

        - **仿生启发**: 借鉴自然界群体系统
        - **可扩展性**: 从小规模到大规模集群
        - **鲁棒性**: 去中心化、容错设计
        - **自适应性**: 动态环境中的自组织

        ---

        如有合作意向，欢迎[联系我们](/zh/contact/)。
---
