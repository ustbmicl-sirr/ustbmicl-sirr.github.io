---
title: 研究方向
type: landing

sections:
  - block: markdown
    content:
      title: 🎉 最新成果
      text: |
        <div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); padding: 2rem; border-radius: 10px; color: white; margin-bottom: 2rem;">
          <h3 style="color: white; margin-top: 0;">📄 论文录用</h3>
          <p style="font-size: 1.1em; font-weight: 500; margin-bottom: 1rem;">
            <strong>HIERARCHICAL MARL FOR TASK ALLOCATION: DISTRIBUTED SUBTASK SELECTION WITH MUTUAL INFORMATION</strong>
          </p>
          <p style="margin-bottom: 0.5rem;">
            ✅ 已被 <strong>IEEE ICASSP 2026</strong> 录用
          </p>
          <p style="margin-bottom: 0.5rem;">
            📅 会议时间：2026年5月3-8日
          </p>
          <p style="margin-bottom: 0;">
            📍 会议地点：西班牙巴塞罗那
          </p>
        </div>

        <p style="text-align: center; color: #666; font-size: 0.9em;">
          <em>ICASSP 是世界上最大、最全面的专注于信号处理及其应用的技术会议</em>
        </p>

  - block: features
    content:
      title: 三大研究方向
      text: 点击卡片查看详情
      items:
        - name: MARL + Robots
          icon: robot
          icon_pack: fas
          description: |
            **多机器人主动协同决策**

            面向无人机编队、仓储AGV、搜救机器人等场景，研究多机器人在通信受限、动态变化环境中的协同定位、导航与寻源问题。

            **关键技术**：因子图+时序GNN状态表征、协调图奖励分配、Safe MARL+PINN安全保证、Sim2Real迁移部署

            [查看详情](#marl-robots)
        - name: Swarm Intelligence
          icon: bugs
          icon_pack: fas
          description: |
            **群体智能与涌现行为**

            借鉴蚁群、蜂群等自然群体的协作机制，研究如何从简单局部规则涌现复杂集体行为，实现无中心化的自组织协调。

            **关键技术**：行为树模块化建模、仿生优化算法(ACO/PSO)、分布式一致性协议、Mean Field大规模近似

            [查看详情](#swarm-intelligence)
        - name: 智慧 IoT
          icon: network-wired
          icon_pack: fas
          description: |
            **大模型协同推理**

            针对边缘设备资源受限的挑战，研究大模型在分布式环境下的高效部署与隐私保护推理，实现计算资源的群智协同。

            **关键技术**：模型压缩与量化、边缘-云分裂推理、联邦学习隐私保护、动态任务卸载调度

            [查看详情](#智慧-iot)

  - block: markdown
    id: marl-robots
    content:
      title: ""
      text: |
        ---
        ## 🤖 MARL + Robots

        **多机器人主动协同决策**：让机器人群体在不确定环境中自主做出最优决策

        > 核心问题：如何让多个机器人在**通信受限**、**观测不完全**、**动态变化**的环境中，通过**分布式学习**实现**安全高效**的协同决策？

        | 任务 | 场景 | 核心挑战 |
        |:---:|:---|:---|
        | **协同定位** | 无人机编队、GPS拒止、协作SLAM | 传感器噪声 · 通信延迟 · 异构融合 |
        | **协作导航** | 编队控制、仓储AGV、动态避障 | 安全约束 · 死锁避免 · 可扩展性 |
        | **协同寻源** | 气体泄漏检测、搜救、信号追踪 | 稀疏观测 · 探索利用 · 环境复杂 |

        <details>
        <summary><strong>🔧 关键技术</strong></summary>

        - **因子图 + 时序GNN**：多机器人时空关系表征与联合状态估计
        - **协调图 + 奖励分配**：值分解与因子图消息传递实现信用分配
        - **Safe MARL + PINN + CBF**：物理约束学习与安全保证
        - **Sim2Real**：域随机化 · 系统辨识 · 渐进式部署

        </details>

        <details>
        <summary><strong>📚 参考工作</strong></summary>

        - **phMARL** (TRO 2025): Port-Hamiltonian 物理信息 MARL
        - **GCBF+** (CoRL 2023): GNN + CBF 可扩展安全控制
        - **MAD-PINN** (2025): PINN 求解分布式微分博弈

        </details>

  - block: markdown
    id: swarm-intelligence
    content:
      title: ""
      text: |
        ---
        ## 🐝 Swarm Intelligence

        **群体智能**：从简单个体规则涌现复杂集体行为

        > 核心问题：如何设计简单的局部规则，使群体在**无中心控制**下涌现出**可预测**、**可扩展**、**鲁棒**的集体智能行为？

        | 任务 | 场景 | 核心挑战 |
        |:---:|:---|:---|
        | **涌现行为** | 群体聚集/分散、集体迁移、协同捕食 | 规则设计 · 可预测性 · 稳定性 |
        | **自组织协调** | 任务分配、编队重构、负载均衡 | 局部信息 · 冲突解决 · 收敛性 |
        | **群体优化** | 组合优化、神经架构搜索、路径规划 | 高维空间 · 多模态 · 动态目标 |

        <details>
        <summary><strong>🔧 关键技术</strong></summary>

        - **行为树 (Behavior Tree)**：模块化行为建模，可与LLM结合
        - **仿生算法**：ACO · PSO · 蜂群算法，模拟自然群体行为
        - **一致性协议**：无中心化分布式一致性，理论保证收敛

        </details>

        <details>
        <summary><strong>📚 参考工作</strong></summary>

        - **MRBTP** (AAAI 2025): 多机器人行为树规划
        - **IKT-BT** (T-Cyber 2025): 通信窃听实现间接知识迁移
        - **Mean Field MARL**: 大规模群体的平均场近似

        </details>

  - block: markdown
    id: intelligent-iot
    content:
      title: ""
      text: |
        ---
        ## 📡 智慧 IoT

        **大模型优化与协同推理**：群智在边缘计算场景的应用

        > 核心问题：如何在**资源受限**的边缘设备上实现**高效**、**隐私保护**的大模型推理与协同学习？

        | 任务 | 场景 | 核心挑战 |
        |:---:|:---|:---|
        | **大模型优化** | 移动端LLM、嵌入式AI、实时推理 | 模型规模 · 计算密集 · 精度损失 |
        | **模型分裂推理** | 边缘-云协同、隐私敏感应用 | 分割决策 · 通信瓶颈 · 隐私泄露 |
        | **联邦学习** | 跨机构医疗AI、分布式机器人学习 | Non-IID · 通信效率 · 拜占庭攻击 |

        <details>
        <summary><strong>🔧 关键技术</strong></summary>

        - **模型分裂**：大模型分割到多设备协同推理
        - **边缘-云协同**：动态任务卸载与资源调度
        - **联邦学习**：数据不出本地，支持异构数据和设备

        </details>

        <details>
        <summary><strong>🔗 与群智的联系</strong></summary>

        智慧IoT = **计算资源的群智协同**：分布式计算节点通过协作实现高效推理

        </details>

  - block: markdown
    content:
      title: 研究理念
      text: |
        **群智 (Swarm Intelligence)** 是贯穿三大方向的核心理念：

        | 方向 | 群智体现 |
        |:---|:---|
        | **MARL + Robots** | 物理世界的群智 — 多机器人协同 |
        | **Swarm Intelligence** | 自然界的群智 — 涌现行为 |
        | **智慧 IoT** | 计算资源的群智 — 协同推理 |

        **共同特点**：分布式协作 · 涌现智能 · 可扩展性 · 鲁棒性

        ---

        如有合作意向，欢迎[联系我们](/zh/contact/)。
---
