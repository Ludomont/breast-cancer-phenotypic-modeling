# Master's Thesis | Modeling Phenotypic Transitions in Breast Cancer 
**Research Internship at [University Name], Oslo | NEOLETEXE Clinical Trial Analysis**

### Project Overview
This project investigates the escape mechanisms of **ER+ breast cancer cells** under hormonal treatment. While estrogen deprivation initially induces quiescence, a subset of cells eventually resumes proliferation, leading to potential resistance. 

Using single-cell transcriptomic data from **18 patients** (NEOLETEXE trial), I developed a mathematical framework to model the transition between Proliferative (P) and Quiescent (Q) states.

### Mathematical Modeling
The core of the analysis involves a system of Ordinary Differential Equations (ODEs) to capture the dynamics of cell state transitions:

$$\frac{dP}{dT} = (u_p - \alpha)P + \beta Q$$
$$\frac{dQ}{dT} = (u_q - \beta)Q + \alpha P$$

**Parameters:**
*   $\alpha$: Transition rate from Proliferative to Quiescent.
*   $\beta$: Transition rate from Quiescent to Proliferative (Escape/Resistance rate).
*   $u_p$: Net growth rate of proliferative cells.
*   $u_q$: Net death rate of quiescent cells.

### Computational Workflow
*   **scRNA-seq Processing:** QC, normalization, and clustering of patient-derived samples.
*   **State Identification:** Defining P and Q phenotypes based on transcriptomic signatures (e.g., cell cycle scoring).
*   **Parameter Estimation:** Integrating single-cell snapshots with the mathematical model to estimate transition rates ($\alpha, \beta$).
*   **Clinical Correlation:** Linking model parameters to patient response within the NEOLETEXE trial.

### Tools Used
*   **Language:** Python / R
*   **Libraries:** Scanpy/Seurat for scRNA-seq, SciPy/DifferentialEquations.jl for modeling.
