# Hybrid Chemotaxis–Entropy Navigation for Nanoscale Medical Agents

This repository contains the implementation of a simulation framework for evaluating navigation strategies of a **Nanoscale Medical Agent (NMA)** in a **Tumor Microenvironment (TME)**.

The project is developed based on our research on hybrid navigation mechanisms combining **chemotaxis** and **information-theoretic (entropy-based)** decision-making.

---

## 📌 Overview

The NMA operates as an autonomous agent within a discretized TME and aims to locate and treat tumor regions by sensing oxygen concentration (hypoxia).

The framework evaluates navigation performance under different environmental conditions and strategies.

---

## 🧪 Scenarios

The project includes two types of tumor environments:

1. **Single-Tumor TME**
2. **Multi-Tumor TME**

---

## 🚀 Navigation Mechanisms

Each scenario is evaluated using three navigation strategies:

1. **Hybrid (Chemotaxis + Entropy)**
2. **Chemotaxis-based**
3. **Random Walk**

---

## 🧠 Key Concept

- **Chemotaxis**: Moves toward lower oxygen concentration (hypoxic regions)
- **Entropy-based navigation**: Explores regions with higher uncertainty
- **Hybrid mechanism**: Dynamically switches between exploration and exploitation

---

## 📂 Project Structure

### Core Modules

- **`sysEnvClasses.py`**  
  Defines the main system entities (NMA and TME) using object-oriented design.

- **`publicFns.py`**  
  Utility functions for visualization and reporting.

---

### Environment & Initialization

- **`Tumor_Development.py`**  
  Loads and visualizes tumor masks (single and multi-tumor).

- **`TME_init.py`**  
  Initializes the lattice-based TME environments.

---

### Single-Tumor Simulations

- **`SingleTumor_Hybrid.py`**  
- **`SingleTumor_Chemotaxis.py`**  
- **`SingleTumor_Random.py`**  

Each script runs ensemble simulations for the respective navigation strategy.

---

### Multi-Tumor Simulations

- **`MultipleTumor_Hybrid.py`**  
- **`MultipleTumor_Chemotaxis.py`**  
- **`MultipleTumor_Random.py`**

---

### Visualization

- **`Visual_Ensemble.py`**  
  Generates plots and evaluation metrics across simulation runs.

---

## 📊 Data

The `Data/` folder contains:

- Tumor masks (single & multi-tumor)
- Steady-state oxygen distributions

All data are stored in CSV format and are used to initialize the simulation environments.

---

## ⚙️ Simulation Details

- Discrete 2D lattice representation of TME
- Oxygen diffusion modeled prior to navigation
- Ensemble-based evaluation for statistical robustness
- Separate time scales for diffusion and agent movement

---

## ▶️ How to Run

1. Initialize the environment:
   ```bash
   python TME_init.py