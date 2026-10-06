# Environment-Assisted Quantum Transport (ENAQT) in Biomolecular Chains

This repository models non-trivial quantum dynamics inside biological energy transport networks (such as photosynthetic chromophores and cytoskeletal protein polymers) using Open Quantum System dynamics in Python (`QuTiP`).

## Core Concept
In biological environments, warm and noisy surroundings are typically thought to destroy quantum coherence. However, **Environment-Assisted Quantum Transport (ENAQT)** demonstrates that controlled environmental noise (dephasing) can actively assist energy transport by breaking static quantum bottlenecks and destructive interference traps.

## Simulation Pipeline
- **System Model:** 3-site tight-binding Hamiltonian with an energetic barrier at the bridge site ($E_1 = 3.5 J$).
- **Master Equation:** Solves the Lindblad Master Equation to account for open system coupling to a thermal bath ($\gamma$).
- **Sink Capture:** Integrated yield evaluation at the acceptor site using collapse operators ($L_{sink} = \sqrt{\gamma_{sink}} \vert{}2\rangle\langle 2\vert{}$).

## Results
The simulation identifies a clear non-monotonic ENAQT "Goldilocks" peak where environmental dephasing ($\gamma \approx 2.30$) optimizes energy transfer efficiency across the barrier.

## How to Run
1. Open `ENAQT_Simulation.ipynb` directly in Google Colab.
2. Install dependencies: `pip install qutip matplotlib numpy`
3. Execute all cells to generate the ENAQT parameter sweep graph.
