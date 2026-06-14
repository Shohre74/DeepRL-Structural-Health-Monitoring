# DeepRL-Structural-Health-Monitoring

This project implements a Deep Reinforcement Learning (DRL) framework for damage detection and active vibration control in building structures. The simulation environment is based on a 5-degree-of-freedom (5-DOF) shear building model.

The repository evaluates three actor-critic algorithms—**SAC, TD3, and DDPG**—to identify floor-wise stiffness reduction and generate optimal control forces under dynamic loads.



## Performance & Training Results

The training stability and convergence of the implemented DRL agents were evaluated over 100 simulation scenarios.

| DDPG Agent | SAC Agent | TD3 Agent |
| :---: | :---: | :---: |
| ![DDPG](figures/DDPG_Training_Curve.png) | ![SAC](figures/SAC_Training_Curve.png) | ![TD3](figures/TD3_Training_Curve.png) |

### Active Vibration Control
A TD3-based controller was trained to minimize structural displacement. The following plot shows the comparison between the uncontrolled and controlled responses of the 5-DOF system:

![Control Response](figures/TD3_Active_Control_Response.png)

### Classical Baseline
A classical sensitivity-based approach (NExT-PCA) was implemented to provide a performance benchmark for the RL-based damage detection.

![Classic Result](figures/Classic_Method_Results.png)



## Repository Status & Notes

- **Implementation:** All RL environments, training logic, and data processing scripts were developed by the author.
- **Academic Use:** This work is currently being prepared for journal submission. To maintain the integrity of the upcoming publication, certain hyperparameters and secondary utility scripts have been excluded from this public version.
- **Reproducibility:** The core notebooks and the primary dataset (`RL_Dataset.zip`) are included to demonstrate the research workflow.


## Project Structure
- `notebooks/`: Jupyter notebooks for training and evaluation.
- `data/`: Dataset files and [dataset_description.md](notebooks/Dataset_description.md).
- `figures/`: Training curves and result visualizations.
- `docs/`: Academic [references](docs/references.md) and documentation.

**Contact:** [Shohre74](https://github.com/Shohre74)
