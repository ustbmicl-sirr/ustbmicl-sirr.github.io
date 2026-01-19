---
title: Research
type: landing

sections:
  - block: markdown
    content:
      title: 🎉 Latest Achievement
      text: |
        <div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); padding: 2rem; border-radius: 10px; color: white; margin-bottom: 2rem;">
          <h3 style="color: white; margin-top: 0;">📄 Paper Acceptance</h3>
          <p style="font-size: 1.1em; font-weight: 500; margin-bottom: 1rem;">
            <strong>HIERARCHICAL MARL FOR TASK ALLOCATION: DISTRIBUTED SUBTASK SELECTION WITH MUTUAL INFORMATION</strong>
          </p>
          <p style="margin-bottom: 0.5rem;">
            ✅ Accepted by <strong>IEEE ICASSP 2026</strong>
          </p>
          <p style="margin-bottom: 0.5rem;">
            📅 Conference Date: May 3-8, 2026
          </p>
          <p style="margin-bottom: 0;">
            📍 Location: Barcelona, Spain
          </p>
        </div>

        <p style="text-align: center; color: #666; font-size: 0.9em;">
          <em>ICASSP is the world's largest and most comprehensive technical conference focused on signal processing and its applications</em>
        </p>

  - block: features
    content:
      title: Three Research Directions
      text: Click cards for details
      items:
        - name: MARL + Robots
          icon: robot
          icon_pack: fas
          description: |
            **Multi-Robot Active Decision-Making**

            Targeting UAV swarms, warehouse AGVs, and search-and-rescue robots, we study cooperative localization, navigation, and source seeking in communication-limited, dynamic environments.

            **Key Tech**: Factor Graph + Temporal GNN, Coordination Graph Credit Assignment, Safe MARL + PINN, Sim2Real Transfer

            [View Details](#marl-robots)
        - name: Swarm Intelligence
          icon: bugs
          icon_pack: fas
          description: |
            **Emergent Collective Behavior**

            Inspired by ant colonies and bee swarms, we study how complex collective behaviors emerge from simple local rules, enabling decentralized self-organization.

            **Key Tech**: Behavior Tree Modeling, Bio-inspired Algorithms (ACO/PSO), Distributed Consensus Protocols, Mean Field Approximation

            [View Details](#swarm-intelligence)
        - name: Intelligent IoT
          icon: network-wired
          icon_pack: fas
          description: |
            **LLM Collaborative Inference**

            Addressing resource constraints on edge devices, we study efficient deployment and privacy-preserving inference of large models in distributed environments.

            **Key Tech**: Model Compression & Quantization, Edge-Cloud Split Inference, Federated Learning, Dynamic Task Offloading

            [View Details](#intelligent-iot)

  - block: markdown
    id: marl-robots
    content:
      title: ""
      text: |
        ---
        ## 🤖 MARL + Robots

        **Multi-Robot Active Collaborative Decision-Making**: Enabling robot swarms to make optimal decisions autonomously in uncertain environments

        > Core Question: How to enable multiple robots to achieve **safe** and **efficient** collaborative decisions through **distributed learning** in environments with **limited communication**, **partial observations**, and **dynamic changes**?

        | Task | Scenarios | Core Challenges |
        |:---:|:---|:---|
        | **Cooperative Localization** | UAV swarms, GPS-denied, cooperative SLAM | Sensor noise · Comm delay · Heterogeneous fusion |
        | **Collaborative Navigation** | Formation control, warehouse AGV, dynamic avoidance | Safety constraints · Deadlock · Scalability |
        | **Cooperative Source Seeking** | Gas leak detection, search & rescue, signal tracking | Sparse observations · Exploration-exploitation · Complexity |

        <details>
        <summary><strong>🔧 Key Technologies</strong></summary>

        - **Factor Graph + Temporal GNN**: Spatio-temporal representation and joint state estimation
        - **Coordination Graph + Credit Assignment**: Value decomposition via factor graph message passing
        - **Safe MARL + PINN + CBF**: Physics-constrained learning with safety guarantees
        - **Sim2Real**: Domain randomization · System ID · Progressive deployment

        </details>

        <details>
        <summary><strong>📚 References</strong></summary>

        - **phMARL** (TRO 2025): Port-Hamiltonian physics-informed MARL
        - **GCBF+** (CoRL 2023): GNN + CBF scalable safe control
        - **MAD-PINN** (2025): PINN for distributed differential games

        </details>

  - block: markdown
    id: swarm-intelligence
    content:
      title: ""
      text: |
        ---
        ## 🐝 Swarm Intelligence

        **Emergent Collective Behavior**: Complex collective behavior emerging from simple individual rules

        > Core Question: How to design simple local rules that enable swarms to exhibit **predictable**, **scalable**, and **robust** collective intelligence **without centralized control**?

        | Task | Scenarios | Core Challenges |
        |:---:|:---|:---|
        | **Emergent Behavior** | Aggregation/dispersion, migration, cooperative hunting | Rule design · Predictability · Stability |
        | **Self-Organization** | Task allocation, formation reconfiguration, load balancing | Local info · Conflict resolution · Convergence |
        | **Swarm Optimization** | Combinatorial optimization, NAS, path planning | High-dim · Multi-modal · Dynamic objectives |

        <details>
        <summary><strong>🔧 Key Technologies</strong></summary>

        - **Behavior Trees**: Modular behavior modeling, LLM integration possible
        - **Bio-inspired Algorithms**: ACO · PSO · Bee algorithms for distributed optimization
        - **Consensus Protocols**: Decentralized consensus with convergence guarantees

        </details>

        <details>
        <summary><strong>📚 References</strong></summary>

        - **MRBTP** (AAAI 2025): Multi-robot behavior tree planning
        - **IKT-BT** (T-Cyber 2025): Indirect knowledge transfer via eavesdropping
        - **Mean Field MARL**: Mean field approximation for large swarms

        </details>

  - block: markdown
    id: intelligent-iot
    content:
      title: ""
      text: |
        ---
        ## 📡 Intelligent IoT

        **LLM Optimization & Collaborative Inference**: Swarm Intelligence applied to edge computing

        > Core Question: How to achieve **efficient**, **privacy-preserving** LLM inference and collaborative learning on **resource-constrained** edge devices?

        | Task | Scenarios | Core Challenges |
        |:---:|:---|:---|
        | **LLM Optimization** | Mobile LLM, embedded AI, real-time inference | Model scale · Compute intensive · Accuracy loss |
        | **Split Inference** | Edge-cloud collaboration, privacy-sensitive apps | Split decision · Comm bottleneck · Privacy leakage |
        | **Federated Learning** | Cross-institutional medical AI, distributed robot learning | Non-IID · Comm efficiency · Byzantine attacks |

        <details>
        <summary><strong>🔧 Key Technologies</strong></summary>

        - **Model Splitting**: Partition large models across devices for collaborative inference
        - **Edge-Cloud Collaboration**: Dynamic task offloading and resource scheduling
        - **Federated Learning**: Data stays local, supports heterogeneous data and devices

        </details>

        <details>
        <summary><strong>🔗 Connection to Swarm Intelligence</strong></summary>

        Intelligent IoT = **Swarm Intelligence of Computing Resources**: Distributed compute nodes achieve efficient inference through collaboration

        </details>

  - block: markdown
    content:
      title: Research Philosophy
      text: |
        **Swarm Intelligence** is the core concept unifying all three directions:

        | Direction | Swarm Aspect |
        |:---|:---|
        | **MARL + Robots** | Swarm Intelligence in the physical world — Multi-robot coordination |
        | **Swarm Intelligence** | Swarm Intelligence in nature — Emergent behavior |
        | **Intelligent IoT** | Swarm Intelligence in computing — Collaborative inference |

        **Common Characteristics**: Distributed Collaboration · Emergent Intelligence · Scalability · Robustness

        ---

        For collaboration inquiries, please [contact us](/contact/).
---
