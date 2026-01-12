---
title: "PINN + Safe MARL Research Framework"
date: 2025-01-12
type: docs
---

# PINN + Safe Multi-Agent RL Research Framework

## Relationship Between Three Research Directions

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                        PINN + Safe Multi-Agent RL                           │
│                     Safe Multi-Agent Reinforcement Learning                 │
└─────────────────────────────────────────────────────────────────────────────┘
                                      │
            ┌─────────────────────────┼─────────────────────────┐
            │                         │                         │
            ▼                         ▼                         ▼
┌───────────────────┐    ┌───────────────────┐    ┌───────────────────┐
│     PINN-CBF      │    │  Equivariant GNN  │    │  Safe Formation   │
│ Physics-Informed  │    │   Graph Neural    │    │    Coordination   │
│  Safety Control   │    │     Networks      │    │                   │
├───────────────────┤    ├───────────────────┤    ├───────────────────┤
│ • Zubov PDE Solve │    │ • E(n) Symmetry   │    │ • CBF Filtering   │
│ • Auto CBF Learn  │    │ • Trans/Rot Inv   │    │ • Formation Keep  │
│ • Physics Embed   │    │ • Agent Permut    │    │ • Collision Avoid │
└─────────┬─────────┘    └─────────┬─────────┘    └─────────┬─────────┘
          │                        │                        │
          │  Safety Constraints    │   Policy Network       │
          └────────────┬───────────┴───────────┬────────────┘
                       │                       │
                       ▼                       ▼
          ┌─────────────────────────────────────────────┐
          │         Unified Coordination Framework      │
          │     Multi-Agent Coordination System         │
          ├─────────────────────────────────────────────┤
          │  Input: Multi-agent states (pos, vel, geo)  │
          │  Output: Safe actions (CBF-constrained)     │
          └─────────────────────────────────────────────┘
                                 │
                                 ▼
          ┌─────────────────────────────────────────────┐
          │              Applications                   │
          ├──────────┬──────────┬──────────┬───────────┤
          │UAV Swarm │ Multi-Bot│   V2X    │  Swarm    │
          │Formation │ Cooperate│Connected │ Logistics │
          └──────────┴──────────┴──────────┴───────────┘
```

## System Data Flow

```
┌──────────────────────────────────────────────────────────────────────────┐
│                        System Data Flow Architecture                      │
└──────────────────────────────────────────────────────────────────────────┘

  Environment                 Policy Learning              Safe Execution
 ┌────────┐                ┌──────────┐                ┌──────────┐
 │ Agent  │  Observation   │          │    Action      │          │
 │ States ├───────────────►│  MARL    ├───────────────►│  CBF-QP  │
 │  x_i   │                │  Policy  │   a_nominal    │  Filter  │
 └────────┘                │   π(s)   │                │          │
     │                     └────┬─────┘                └────┬─────┘
     │                          │                           │
     │    ┌─────────────────────┘                           │
     │    │                                                 │
     │    ▼                                                 ▼
     │ ┌─────────────────┐                    ┌─────────────────────┐
     │ │  Equivariant    │                    │   Safety Filter     │
     │ │     GNN         │                    │                     │
     │ │                 │                    │  min ||a - a_nom||² │
     │ │ • Message Pass  │                    │  s.t. ḣ + αh ≥ 0   │
     │ │ • Geo Encoding  │                    │                     │
     │ │ • Equiv Aggreg  │                    └──────────┬──────────┘
     │ └─────────────────┘                               │
     │                                                   │
     │         ┌─────────────────────────────────────────┘
     │         │
     │         ▼
     │    ┌──────────┐
     └───►│ PINN-CBF │
          │          │
          │ Learning:│
          │ ∇h·f = -φ(x)(1-h)√(1+||∇h||²)  ◄── Zubov PDE
          │                                │
          │ Output: h(x) Control Barrier   │
          └──────────┬─────────────────────┘
                     │
                     │  Provides safety constraint h(x)
                     │
                     ▼
              ┌────────────┐
              │ Safe Action│
              │   a_safe   │
              └────────────┘
```

## Technical Comparison

| Dimension | PINN-CBF | Equivariant GNN | Safe Formation |
|-----------|----------|-----------------|----------------|
| **Goal** | Learn safety constraints | Encode geometric symmetry | Coordinate control |
| **Theory** | Zubov PDE + PINN | Group Theory + GNN | CBF-QP + MARL |
| **Input** | Dynamics f(x,u) | Relative pos/vel | State + nominal action |
| **Output** | CBF function h(x) | Equivariant features | Safe action a_safe |
| **Innovation** | Auto CBF design | Sample efficiency | Safety guarantee |
| **Scalability** | Offline training | Zero-shot transfer | Real-time compute |

## Integration Roadmap

```
                    Phase 1                 Phase 2                 Phase 3
                  Foundation              Integration              Validation
                 ┌─────────┐             ┌─────────┐             ┌─────────┐
    PINN-CBF    │ Zubov   │            │         │            │         │
    Direction    │  PDE    ├────────────►         │            │         │
                │ Solver  │            │  PINN   │            │ Complete│
                └─────────┘            │   +     │            │ System  │
                                       │  GNN    ├────────────► Simul   │
                ┌─────────┐            │   +     │            │   +     │
   Equivariant  │ E(n)-   │            │  MARL   │            │  Real   │
     GNN        │ EGNN    ├────────────►         │            │  World  │
    Direction   │ Arch    │            │ Integr  │            │  Test   │
                └─────────┘            │         │            │         │
                                       └─────────┘            └─────────┘
                ┌─────────┐                  ▲
     Safe       │ CBF-QP  │                  │
   Formation    │Optimizer├──────────────────┘
    Direction   └─────────┘

                   Theory           ───────►        Application
```

## Core Algorithm Pseudocode

```python
class PINN_Safe_MARL_System:
    """Unified Framework: PINN-CBF + Equivariant GNN + Safe Formation"""

    def __init__(self, n_agents, state_dim, action_dim):
        # Module 1: PINN-CBF (offline training)
        self.pinn_cbf = PINN_CBF(
            dynamics_model=f,           # System dynamics
            pde_type='zubov',           # Zubov PDE
            safe_set_def=safe_region    # Safe region definition
        )

        # Module 2: Equivariant GNN Policy
        self.policy = EquivariantGNN(
            node_dim=state_dim,
            edge_dim=4,                 # Relative pos + vel
            hidden_dim=64,
            num_layers=3,
            equivariance='E(n)'         # Translation + rotation equiv
        )

        # Module 3: CBF Safety Filter
        self.safety_filter = CBF_QP_Filter(
            cbf_function=self.pinn_cbf,
            alpha=1.0                   # CBF class-K function param
        )

    def get_safe_action(self, states, graph):
        """
        Input: states (n_agents, state_dim), graph (adjacency)
        Output: safe_actions (n_agents, action_dim)
        """
        # Step 1: Equivariant GNN computes nominal actions
        nominal_actions = self.policy(states, graph)

        # Step 2: CBF safety filtering
        safe_actions = []
        for i in range(n_agents):
            # Get agent i's CBF value and gradient
            h_i, grad_h_i = self.pinn_cbf(states[i])

            # QP optimization: min ||a - a_nom||² s.t. ḣ + αh ≥ 0
            a_safe = self.safety_filter.filter(
                nominal_action=nominal_actions[i],
                state=states[i],
                cbf_value=h_i,
                cbf_gradient=grad_h_i
            )
            safe_actions.append(a_safe)

        return torch.stack(safe_actions)
```

## Related Papers

| Direction | Key Paper | Code |
|-----------|-----------|------|
| PINN-CBF | Neural CBF from Zubov PDE (2024) | - |
| Equivariant GNN | LEGO: Equivariant Graph Network (NeurIPS 2024) | [GitHub](https://github.com/dchen48/LEGO) |
| Safe MARL | GCBF+ (ICRA 2024) | [MIT-REALM](https://github.com/MIT-REALM/gcbf-pytorch) |
| Combined | Physics-Informed Safe Control (ICML 2025) | - |

---

*Last updated: 2025-01-12*
