---
title: Research
type: landing

sections:
  - block: markdown
    content:
      title: ""
      text: |
        ## Group Focus

        We study **swarm robot active navigation** under cross-domain partial observability: how robots infer structured posteriors over environment, links, roles, and domain parameters from local observations; how they jointly choose executable collaboration edges and actions; and how task–collaboration structure is preserved, adapted, and recovered from simulation to reality.

        > **Factor graphs to understand an uncertain world; GraphSwarm to form collaboration structure; offline–online multi-agent learning for verifiable Sim2Real active navigation.**

        ---

        > **News** | ICASSP 2026 · Hierarchical MARL for Task Allocation
        > Heng Zhang, Shihong Duan, Yadong Wan · Barcelona · [DOI](https://doi.org/10.1109/ICASSP55912.2026.11462585)

  - block: features
    content:
      title: Main Work
      text: Four layers on the current evidence chain (semantic SLAM / VLA are later extensions)
      items:
        - name: Structured Inference
          icon: project-diagram
          icon_pack: fas
          description: |
            **Dynamic probabilistic factor graphs**

            Posterior inference over states, maps, links, roles, and domain parameters—with explicit variables, potentials, and algorithms.

            [Details](#inference)
        - name: Collaboration Emergence
          icon: sitemap
          icon_pack: fas
          description: |
            **GraphSwarm**

            Formation, maintenance, failure, and recovery of executable collaboration structures (sensing / communication / task edges).

            [Details](#graphswarm)
        - name: Offline–Online Decision
          icon: robot
          icon_pack: fas
          description: |
            **DT + Graph-MARL**

            Offline long-horizon behavior priors with online distributed residual adaptation for seeking, allocation, and active exploration.

            [Details](#decision)
        - name: Verifiable Transfer
          icon: exchange-alt
          icon_pack: fas
          description: |
            **Sim2Real**

            Physics calibration of domain factors; validate transfer across scale, communication, and real platforms—not simulation success alone.

            [Details](#sim2real)

  - block: markdown
    id: inference
    content:
      title: ""
      text: |
        ---
        ## Structured Inference · Dynamic Probabilistic Factor Graphs

        Factor graphs are used for **posterior inference** in partially observed swarms—not as a label for arbitrary relation graphs or attention maps.

        | Latent | Meaning |
        |:---|:---|
        | \(X_t\) | Robot states |
        | \(M_t\) | Map / targets / environment |
        | \(C_t\) | Communication reliability |
        | \(R_t\) | Roles or collaboration intent |
        | \(\Theta_t\) | Dynamics, observation, and communication domain parameters |

        Related publications: [Factor Graph Guided Deep Reinforcement Learning for Uncertainty Aware SLAM Exploration](/publication/factor-graph-slam/)

  - block: markdown
    id: graphswarm
    content:
      title: ""
      text: |
        ---
        ## Collaboration Emergence · GraphSwarm

        The scientific object is **executable collaboration structure**: actions jointly change pose, future observation quality, communication topology, and task collaboration.

        | Graph | Question |
        |:---|:---|
        | Sensing \(G^{\mathrm{sen}}\) | Who observes whom / with what quality |
        | Communication \(G^{\mathrm{com}}\) | Who can reliably talk to whom |
        | Task \(G^{\mathrm{task}}\) | Who collaborates on which subtasks |

        **Selected outputs**: source navigation with CG-MCTS (IROS 2026, accepted); factor-graph / coordination structures for cooperative localization and tracking (JSAC / IoT-J, 2024)


  - block: markdown
    id: decision
    content:
      title: ""
      text: |
        ---
        ## Offline–Online Decision · DT + Graph-MARL

        Decision Transformers supply measurable long-horizon priors; Graph-MARL performs online distributed adaptation under graph constraints—not two parallel theory tracks.

        Related publications: [Subgoal-Based Hierarchical Reinforcement Learning for Multiagent Collaboration](/publication/subgoal-collaboration/) · [Distributed task allocation](/publication/icassp-2026-hierarchical-marl/)

  - block: markdown
    id: sim2real
    content:
      title: ""
      text: |
        ---
        ## Verifiable Transfer · Sim2Real

        PINN / system identification updates domain-related dynamics and observation factors. We prioritize interaction structure and observation/communication factor shifts; dynamics shift enters as physical calibration.

        Related publications: [Domain adaptation for visual navigation](/publication/sim2real-navigation/) · [Learning-Based Multi-Robot Active SLAM: A Conceptual Framework and Survey](/publication/active-slam-survey/)

  - block: markdown
    content:
      title: Scope
      text: |
        - Graph-Semantic SLAM / VLA, general emergence theory, and industrial IoT are **not** current co-equal scientific problems.
        - Wireless channels and embedded sensing are **supporting capabilities** for swarm communication and deployment.
        - Non-triviality comes from the scientific object, mechanisms, and identifiable / transfer bounds—not stacked networks and losses.
---
