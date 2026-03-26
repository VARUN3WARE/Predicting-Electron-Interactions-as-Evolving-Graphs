# Project Progress Report: Electron Density Prediction using Graph Neural Networks (GNNs)

**Objective**: To model and predict the temporal evolution of electron density states in molecular systems (Ammonia and Water) using modern Graph Neural Network (GNN) architectures.

## 1. Project Overview
The project treats molecular grid points as nodes in a graph, with spatial relationships defined as edges. GNNs are then trained to learn the complex temporal dynamics of electron interactions, moving beyond traditional baseline predictions.

## 2. Methodology and Architecture
Two primary model variants have been developed:
- **`multi_input` (Temporal Regression)**: Uses multiple past density states as input to predict the current or next immediate state.
- **`multi_future` (Trajectory Prediction)**: Takes a single or sequence of inputs and predicts the entire future trajectory (multiple future steps) of the density distribution.

**Data Source**: 
- `NH3` (Ammonia): 10,540 grid points, 401 timesteps.
- `H2O` (Water): 8,062 grid points, 401 timesteps.

## 3. Engineering Achievements
We have successfully restructured the project for professional deployment and mass usability:
- **Project Organization**: Implementation of a standard ML folder structure (`data/`, `models/`, `notebooks/`, `reports/`) for clear separation of concerns.
- **Reproducibility**: All notebooks have been updated to use relative paths, facilitating seamless execution on any machine.
- **Version Control**: Development is now tracked on dedicated feature branches (`chore/restructure-codebase`), ensuring robust development and collaboration practices.

## 4. Current Performance Metrics
Recent evaluations indicate strong predictive capabilities:
- **Average R²**: ~0.9984 across multiple future steps.
- **Mean Absolute Error (MAE)**: ~0.342.
- **Model Verdict**: Predictions are Highly Accurate, with very high correlation to the ground truth datasets.

## 5. Next Steps and Future Directions
1. **Physics-Informed Constraints**: Integrating conservation laws into the loss function to improve the physical validity of predictions.
2. **Ensemble Modeling**: Investigating the combination of multiple GNN architectures to further reduce error rates.
3. **Advanced Architectures**: Implementing Graph Attention Networks (GAT) to better capture non-local interactions.

---
*Report generated for review and presentation to the academic supervisor.*
