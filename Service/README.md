# PEM Fuel Cell Prognostics Using Attention-Enhanced LSTM Networks

This repository contains Jupyter notebooks implementing data-driven prognostic models for PEM fuel-cell degradation prediction under various operating conditions. The proposed framework combines Long Short-Term Memory (LSTM) networks with a self-attention mechanism to capture temporal dependencies and degradation patterns from operational data.

## Prognostic Approaches

### Voltage-Based Prognostics

This approach is designed for steady-state operating conditions, where the fuel cell operates under a constant load and degradation primarily appears as a gradual voltage decrease over time. The model learns degradation behaviour directly from historical voltage measurements by constructing time-lagged sequences and forecasting future voltage trajectories. Since voltage is closely related to fuel-cell performance under steady-state operation, it serves as a reliable health indicator without requiring additional operational measurements.

### Multi-Variable Prognostics

This approach incorporates operational variables describing the fuel-cell operating state, including electrical load, reactant flow rates, pressures, temperatures, and operating time. By leveraging a richer representation of the system, the model can account for the influence of operating conditions on voltage behaviour and degradation mechanisms. This configuration is particularly relevant under dynamic operating conditions, where voltage variations may arise from both degradation and changes in operating conditions.

## Case Studies

| Notebook           | Operating Regime         | Input Variables               | Prediction Objective                       |
| ------------------ | ------------------------ | ----------------------------- | ------------------------------------------ |
| `PM200.ipynb`      | Steady-state degradation | Voltage                       | Multi-step voltage forecasting             |
| `BZ100_Sig1.ipynb` | Steady-state operation   | Voltage + operating variables | Voltage degradation prediction             |
| `BZ100_Sig2.ipynb` | Quasi-dynamic operation  | Voltage + operating variables | Voltage degradation prediction             |
| `Alice_Sig1.ipynb` | Cyclic load operation    | Operating variables           | Voltage prediction under cyclic loads      |
| `Alice_Sig2.ipynb` | Start–stop operation     | Operating variables           | Voltage prediction under start–stop cycles |



## Deep Learning Architecture

The predictive model combines LSTM layers and a self-attention mechanism. The LSTM component captures sequential degradation dynamics and temporal dependencies, while the attention mechanism identifies the most informative patterns within the historical data. Together, these components provide a robust framework for modelling fuel-cell performance degradation under diverse operating conditions.

## Repository Structure

```text
.
├── PM200.ipynb
├── BZ100_Sig1.ipynb
├── BZ100_Sig2.ipynb
├── Alice_Sig1.ipynb
├── Alice_Sig2.ipynb
└── README.md
```

## Funding

This work was supported by the EnerTEF Project (Testing and Experimentation Facility for Hydrogen Technologies) under the European Union Horizon Europe Programme.

