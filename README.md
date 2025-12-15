# 2D Transient Heat Transfer Solver (FDM)

## 🚀 Overview
This project is a high-performance computational physics engine designed to simulate **2D transient heat conduction** in semiconductor materials.

Built with **Modern C++**, it utilizes the **Finite Difference Method (FDM)** to solve the heat diffusion equation numerically. The project includes a **Python automation wrapper** to handle batch simulations and **Matplotlib** for generating real-time thermal heatmaps.

## ⚡ Key Features
* **C++ Computation Engine:** Optimized for speed using STL and Object-Oriented Design (OOD).
* **Numerical Method:** Implements Explicit Finite Difference scheme for 2D grids.
* **Python Automation:** Wrapper script using `subprocess` to automate parameter sweeping (e.g., testing different thermal conductivities).
* **Visualization:** Automated heatmap generation for temperature distribution analysis.

## 📐 Mathematical Model
The solver discretizes the standard Heat Equation:

$$\frac{\partial T}{\partial t} = \alpha \left( \frac{\partial^2 T}{\partial x^2} + \frac{\partial^2 T}{\partial y^2} \right)$$

Where:
* $T$: Temperature
* $t$: Time
* $\alpha$: Thermal Diffusivity ($k / \rho c_p$)

The domain is discretized into a grid $(i, j)$, and the time evolution is calculated iteratively.

## 🛠️ Tech Stack
* **Core Engine:** C++ (GCC Compiler)
* **Scripting:** Python 3.x
* **Libraries:** NumPy, Matplotlib, Pandas
* **Build Tool:** Make / CMake

## 📂 Project Structure
```bash
Cpp-Thermal-Solver/
├── src/
│   ├── main.cpp          # Entry point
│   ├── solver.cpp        # FDM Algorithm implementation
│   ├── grid.h            # Mesh grid class definition
├── scripts/
│   ├── run_simulation.py # Python wrapper for batch execution
│   ├── plot_results.py   # Heatmap visualization
├── data/                 # Output CSV files
└── README.md
