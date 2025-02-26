# NBody-Symbolic-Simulation

A Python-based symbolic N-body simulation using SymPy and Matplotlib. This project computes gravitational interactions for multiple bodies over timesteps using a simplified Velocity Verlet method and outputs the final positions as symbolic equations to a PDF file. It’s optimized for cloud platforms like Kaggle to avoid local resource strain.

## Features
- Symbolic computation of gravitational forces, velocities, and positions.
- Outputs final position equations (\(x, y, z\)) for a specified object to `nbody_positions.pdf`.
- Uses a truncated display (1000 characters per equation) for manageability.
- Includes iteration number in the output PDF.

## Method Used
The simulation employs a **simplified Velocity Verlet integration method**, a symplectic integrator adapted for symbolic computation:
- **Force Calculation**: Uses Newton’s law of gravitation: \( F = G \frac{m_i m_j}{r^3} \cdot \vec{r} \).
- **Velocity Update**: Computes \( \Delta v = \frac{F}{m} \cdot \tau \), then updates velocity as \( v_{\text{new}} = v + \Delta v \).
- **Position Update**: Calculates average velocity \( v_{\text{avg}} = v + 0.5 \cdot \Delta v \), then updates position as \( x_{\text{new}} = x + v_{\text{avg}} \cdot \tau \).
- **Symbolic**: All steps are performed symbolically with SymPy, preserving unsimplified expressions.
- **Simplification**: Uses initial forces only per timestep (no force recalculation at new positions), optimizing for symbolic output over numerical precision.
This method builds complex, iterative equations suitable for analysis or education, executed over \( k \) timesteps.

## Prerequisites
- Python 3.x
- Libraries: `sympy`, `matplotlib`

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Aregay01/NBody-Symbolic-Simulation.git
   cd NBody-Symbolic-Simulation
