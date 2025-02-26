# NBody-Symbolic-Simulation

A Python-based symbolic N-body simulation using SymPy and Matplotlib. This project computes gravitational interactions for multiple bodies over timesteps using a simplified Velocity Verlet method and outputs the final positions as symbolic equations to a PDF file. It’s optimized for cloud platforms like Kaggle to avoid local resource strain.

## Features
- Symbolic computation of gravitational forces, velocities, and positions.
- Outputs final position equations (\(x, y, z\)) for a specified object to `nbody_positions.pdf`.
- Uses a truncated display (1000 characters per equation) for manageability.
- Includes iteration number in the output PDF.

## Prerequisites
- Python 3.x
- Libraries: `sympy`, `matplotlib`

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Aregay01/NBody-Symbolic-Simulation.git
   cd NBody-Symbolic-Simulation
