The project includes two scenarios:
1. Single-tumor
2. Multi-tumor

Each scenario is evaluated over three navigation mechanisms:
1. Hybrid
2. Chemotaxis
3. Random

The agent, which is called the Nanoscale Medical Agent (NMA) works as the system in an environment
that represents a part of diseased tissu, which is called the tumor microenvironment (TME).

The simulation framework contains various files to include functions required to implement the algorithms
in the predefined scenarios, which are described below:

1. "sysEnvClasses.py": This file contains the implementation of these two entities as Classes,
including their properties and functions, in an object-oriented programming (OOP) paradigm.

2. "publicFns.py": This file includes some functions that can be used for visualization and report purposes.

3. "Tumor_Development.py": This file loads the single-tumor and multi-tumor tumor masks and visualize them.

4. "TME_init.py": Using this file, you can initialize the lattice for each single-tumor and multi-tumor environments.

5. "SingleTumor_Hybrid.py": Implementation of the hybrid navigation mechanism in a single-tumor scenarion using ensemble simulations.

6. "SingleTumor_Chemotaxis.py": Implementation of the chemotaxis navigation mechanism in a single-tumor scenarion using ensemble simulations.

7. "SingleTumor_Random.py": Implementation of the random navigation mechanism in a single-tumor scenarion using ensemble simulations.

8. "MultipleTumor_Hybrid.py": Implementation of the hybrid navigation mechanism in a multi-tumor scenarion using ensemble simulations.

9. "MultipleTumor_Chemotaxis.py": Implementation of the chemotaxis navigation mechanism in a multi-tumor scenarion using ensemble simulations.

10. "MultipleTumor_Random.py": Implementation of the random navigation mechanism in a multi-tumor scenarion using ensemble simulations.

11. "Visual_Ensemble.py": This file includes functions that are called separately to generate various meaningful plots for evaluation of the navigation mechanisms.

Additionally, there is a folder "Data" that contains four csv files, consisting tumor masks and oxygen distribution
at a steady-state in single-tumor and multi-tumor scenarios.