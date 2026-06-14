# SHM Simulation Dataset: Technical Overview

This dataset was developed as part of my research into Structural Health Monitoring (SHM) and Active Vibration Control. The primary goal was to create a reliable foundation for training Deep Reinforcement Learning (DRL) agents to recognize and quantify structural degradation.

### Overview of the Data
The dataset includes 100 simulation scenarios, each representing a different structural state. These are provided in CSV format, with a corresponding labels.json file that links each scenario to its specific damage location and severity.

### Model and Physics
The simulations are based on a 5-Degree-of-Freedom (5-DOF) shear building model, following the benchmark parameters established by Chen and Xu (2008). 

To ensure the simulation remains physically grounded:
* Each floor is modeled with a mass of 1000 kg.
* The healthy stiffness for each story is set at 250,000 N/m.
* I incorporated Rayleigh damping with a 5% ratio for the first two vibration modes to better mimic real-world structural behavior.

### Data Organization
Inside the RL_Dataset.zip file, scenarios are numbered from 000 to 099. Each file captures 10 seconds of structural response with a sampling rate of 0.01 seconds.

Each CSV file contains the following sensor data:
1. Time: The simulation timestamp.
2. Disp_X: Story displacement.
3. Vel_X: Story velocity.
4. Acc_X: Story acceleration (the main observation input for the RL agents).

### Damage Simulation Logic
I modeled structural damage by introducing a reduction in stiffness (k) at various levels. 
* The dataset covers a range of conditions, from a fully healthy state to scenarios with 10% to 50% stiffness loss.
* I included both single-floor damage and more complex multi-floor damage cases to test the limits of the detection algorithms.

### Research Application
This dataset serves as the environment for my work with SAC, TD3, and DDPG algorithms. By processing these structural responses, the agents are trained to perform three critical tasks: identifying the presence of damage, localizing the affected floor, and quantifying the extent of the stiffness reduction.
