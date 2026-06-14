# DeepRL-Structural-Health-Monitoring

This project investigates the application of Deep Reinforcement Learning (DRL) for damage detection and active vibration control in a 5-DOF shear building model.

The main goal is to evaluate how agents like SAC, TD3, and DDPG handle continuous state-action spaces in structural engineering tasks, specifically for estimating stiffness reduction and suppressing seismic-like vibrations.



## Results & Analysis

The training curves for the three implemented algorithms are shown below. Note that SAC and TD3 show more stable convergence compared to DDPG in this environment.

| DDPG | SAC | TD3 |
|------|-----|-----|
| ![DDPG](DDPG_Training_Curve.png) | ![SAC](SAC_Training_Curve.png) | ![TD3](TD3_Training_Curve.png) |

### Active Control Performance
The TD3 agent was used to generate control forces. The plot below compares the uncontrolled vs. controlled structural response:

![Active Control](TD3_Active_Control_Response.png)

### Baseline Comparison
A classical sensitivity-based approach (NExT-PCA) was used as a benchmark for damage estimation:

![Classic Method](Classic_Method_Results.png)



## Repository Content & Status

- **Code:** All RL environments and training scripts are implemented in the provided Jupyter Notebooks.
- **Data:** The simulation dataset (100 scenarios) is available in `RL_Dataset.zip`.
- **Note:** This repository represents ongoing research. Some specific hyperparameter configurations and internal utility scripts are withheld as the work is being prepared for journal submission.

All core logic and training pipelines were developed by the author.


## References
This study builds upon the framework by Chen and Xu (2008) regarding integrated SHM and semi-active control. Detailed references are available in `docs/references.md`.
