---
title: Research
type: landing

sections:
  - block: markdown
    content:
      title: Research Areas
      subtitle: Swarm Intelligence & Multi-Agent Systems
      text: |
        ## Research Architecture

        ```
        ┌────────────────────────────────────────┐      ┌────────────────────────────────┐
        │           Core Technologies            │      │       Learning Paradigms       │
        ├────────────────────────────────────────┤      ├────────────────────────────────┤
        │                                        │      │                                │
        │  MARL + Robots    Swarm Intelligence   │      │  PINN         Federated RL     │
        │  ────────────     ──────────────────   │      │  Physics-Inf  Distributed      │
        │                                        │      │                                │
        │  • Factor Graph   • Bio-inspired       │ ───► │  Human-in-Loop    Sim2Real     │
        │    Probabilistic    ACO/PSO/Bee        │      │  Interactive      Transfer     │
        │                                        │      │                                │
        │  • Equivariant    • Consensus          │      └────────────────────────────────┘
        │    GNN              Distributed        │
        │                                        │
        │  • Manifold       • Mean Field         │
        │    Safety/CBF       Large-scale        │
        │                                        │
        └────────────────────────────────────────┘
        ```

        ---

  - block: markdown
    content:
      title: "MARL + Robots"
      text: |
        | Research Tasks | Core Problems |
        |:---|:---|
        | **Cooperative Localization**: Multi-robot/UAV distributed localization, SLAM | Sensor noise, communication delay, data fusion |
        | **Collaborative Navigation**: Path planning, obstacle avoidance, formation control | Dynamic environments, safety constraints, real-time |
        | **Cooperative Source Seeking**: Target search, signal source localization, environmental monitoring | Sparse observations, uncertainty, Sim2Real |

        **Key Technologies:** MARL + Optimization Algorithms

  - block: features
    content:
      title: ""
      items:
        - name: Factor Graph
          icon: project-diagram
          icon_pack: fas
          description: |
            Probabilistic inference and optimization based on factor graphs, combined with Self-Attention Factor Graph Neural Networks (SA-FGNN) for multi-agent cooperative localization and target tracking.
        - name: Equivariant GNN
          icon: brain
          icon_pack: fas
          description: |
            E(n)-equivariant graph neural networks encoding multi-agent geometric relations, ensuring policy symmetry under translation, rotation, and permutation.
        - name: Manifold
          icon: globe
          icon_pack: fas
          description: |
            Manifold geometry-based safety constraint modeling, combined with CBF for safe control and geometric optimization.

  - block: markdown
    content:
      title: "Swarm Intelligence"
      text: |
        | Research Tasks | Core Problems |
        |:---|:---|
        | **Emergent Behavior**: Complex collective behavior from simple rules | Behavior design, predictability, stability analysis |
        | **Self-Organization**: Decentralized swarm decision-making and task allocation | Local communication, global convergence, scalability |
        | **Swarm Optimization**: Large-scale agent collaborative search and optimization | Computational complexity, convergence speed, multi-objective trade-offs |

        **Key Technologies:** Behavior Trees + Bio-inspired Algorithms

  - block: features
    content:
      title: ""
      items:
        - name: Behavior Trees
          icon: sitemap
          icon_pack: fas
          description: |
            Modular behavior modeling framework supporting complex behavior composition, reuse, and dynamic switching for interpretable emergent behavior design.
        - name: Bio-inspired Algorithms
          icon: bug
          icon_pack: fas
          description: |
            Nature-inspired methods including ACO, PSO, and Bee algorithms for distributed optimization and emergent behavior.
        - name: Consensus Protocols
          icon: sync-alt
          icon_pack: fas
          description: |
            Distributed consensus algorithms for self-organization, stigmergy-based coordination, and global convergence.

  - block: markdown
    content:
      title: "Learning Paradigms"
      text: |
        **Cross-domain learning methods and training frameworks**:

  - block: features
    content:
      title: ""
      items:
        - name: PINN (Physics-Informed NN)
          icon: atom
          icon_pack: fas
          description: |
            Embedding physical laws (PDE/ODE) into neural networks for data-efficient dynamics modeling and safety constraint learning (Zubov PDE to CBF).
        - name: Federated RL
          icon: network-wired
          icon_pack: fas
          description: |
            Distributed, privacy-preserving multi-agent training framework supporting heterogeneous data and decentralized learning.
        - name: Human-in-Loop
          icon: user-cog
          icon_pack: fas
          description: |
            Interactive learning with human-machine collaboration, optimizing swarm control policies through human feedback.
        - name: Sim2Real Transfer
          icon: exchange-alt
          icon_pack: fas
          description: |
            Domain randomization and domain adaptation techniques for policy transfer from simulation to real robots.

  - block: markdown
    content:
      title:
      text: |
        ---

        ## Research Philosophy

        - **Bio-Inspired**: Drawing from nature's swarm systems
        - **Scalable**: From small teams to large-scale swarms
        - **Robust**: Decentralized, fault-tolerant design
        - **Adaptive**: Self-organizing in dynamic environments

        ---

        For collaboration inquiries, please [contact us](/contact/).
---
