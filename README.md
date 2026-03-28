# Breast Cancer Phenotypic Transitions | Master's Thesis at OCBE, University of Oslo
**Modeling ER+ cancer cell dynamics under hormonal treatment (NEOLETEXE Trial)**

This repository contains the computational framework used to model the escape mechanisms of breast cancer cells from quiescence to a proliferative state.

### Repository Structure
*   `simulate_data.ipynb`: Script for generating synthetic data based on the P-Q transition model.
*   `optimization_simulate_data.ipynb`: Implementation of optimization algorithms to test the model's ability to recover parameters from simulated datasets.
*   `optimization_experimental_data.ipynb`: Application of the mathematical model to real-world patient data from the NEOLETEXE trial.
*   `*.csv` files: Datasets containing volume measurements and clinical data points used for model calibration.

### The Mathematical Model
The transition between Proliferative (P) and Quiescent (Q) cell populations is modeled using the following system of ODEs:

$$\frac{dP}{dT} = (u_p - \alpha)P + \beta Q$$
$$\frac{dQ}{dT} = (u_q - \beta)Q + \alpha P$$

The goal of the optimization scripts is to estimate the transition rates ($\alpha$ and $\beta$) to identify patients at higher risk of developing resistance (high $\beta$).
