# CNC_001_ASS_5_ECO
This is an **ASS** (Agentic Society Simulation) project that simulates a society with five different types of agents and how they interact with each other.

# 🪐 Silicon Brain Trust: Agentic Society Simulation

An experimental **Agent-Based Simulation (ABS)** built on Python and **Mesa 3.x**. This project models a complex adaptive society of autonomous agents interacting in a 2D environment, examining the dynamic emergence of social structures, wealth dynamics, and evolutionary equilibria.

---

## 💡 Overview

Unlike standard Multi-Agent Reinforcement Learning (MARL) environments designed for goal-oriented optimization, this simulation focuses on **emergent social behavior**. 

Agents operate under natural constraints—competing for resources, establishing social alliances, forming hereditary bonds, and expanding spatial boundaries. Rather than training a static policy, the system observes how social stratification, ethical norms, and power structures naturally evolve over thousands of iterations.

---

## 🧬 Key Mechanics

* **Agent Attributes (Genetics):** Every agent is initialized with unique trait vectors:
  * `Intelligence` — Enhances resource collection efficiency and technological expansion.
  * `Influence` — Governs social persuasion and territory/aura radius.
  * `Morality` — Controls cooperation limits and altruism vs. exploitation trade-offs.
  * `Aggression` — Boosts resource acquisition and raiding range at the cost of legal/retaliatory penalties.

* **Social Dynamics & Alliances:**
  * **Marriage & Partnerships:** Pair-bonding pools agents' resources and increases overall survival resilience ($1.2\times - 1.5\times$ efficiency boost).
  * **Clans & Coalitions:** Bounded alliances (up to 8 agents) share complementary skill ceilings while navigating organizational overhead.
  * **Feudal Followings:** Lower-attribute agents can pay resource dividends to powerful leaders in exchange for protection and aura bonuses.

* **Evolution & Expansion:**
  * **Heredity & Decay:** Offspring inherit parental traits with random mutations upon generation boundaries.
  * **Spatial Breakthroughs:** Ultra-high intelligence agents can forego immediate consumption to expand the physical grid bounds ($100 \times 100 \rightarrow 101 \times 101$), alleviating Malthusian population traps.

---

## 🛠️ Architecture & Tech Stack

Designed to run lightweight on **ARM64 (Raspberry Pi CM4 / uConsole)** for code development, while scaling seamlessly to **x86_64 / GPU environments** for high-throughput multi-core simulations.

* **Framework:** [Mesa 3.x](https://github.com/projectmesa/mesa) (Agent-Based Modeling)
* **Data & Analytics:** NumPy, Pandas, NetworkX (Graph Theory)
* **Visualization:** JupyterLab, Solara, Matplotlib / Seaborn
* **Memory Model:** Lightweight Episodic Memory Matrices with exponential decay (no heavy LLM inference bottlenecks required).

---

## 🚀 Quick Start

```bash
# Clone the repository
git clone [https://github.com/your-username/silicon-brain-trust-sim.git](https://github.com/your-username/silicon-brain-trust-sim.git)
cd silicon-brain-trust-sim

# Create and activate virtual environment
python3 -m venv sim_env
source sim_env/bin/activate

# Install dependencies
pip install mesa numpy pandas matplotlib seaborn networkx jupyterlab

# Launch JupyterLab
jupyter lab
