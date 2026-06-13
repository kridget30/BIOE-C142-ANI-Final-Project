# BIOE C142 Final Project: ANI-Style Neural Network Potential

This repository contains my BIOE C142 final project on training an ANI-style supervised artificial neural network model to predict DFT molecular energies.

## Project Overview

The project uses TorchANI and PyTorch to train an atom-wise neural network potential inspired by ANI-1. Molecular coordinates and atom types are converted into atomic environment vectors (AEVs), and separate neural networks are used for H, C, N, and O atoms. Atomic energy contributions are summed to predict total molecular energy.

## Final Model

Final selected architecture:

- Hidden layers: `[256, 128]`
- Activation: ReLU
- Batch size: 2048
- Learning rate: 1e-4
- Epochs: 50
- L2 regularization: 1e-5
- Optimizer: Adam
- Loss: MSE

## Final Results

Final held-out test performance:

- Test MAE: 1.2397 kcal/mol
- Test RMSE: 1.9238 kcal/mol

## Environment & Computing
This project was trained and executed on the **Savio** high-performance computing cluster using the course-provided environment.

## Repository Structure

```text
notebooks/
  project_ckpt5_final.ipynb        Final executable notebook

reports/
  final_report.pdf                 Final written report
  checkpoint3_hyperparameter_tuning.pdf
  checkpoint4_production_cv.pdf
  checkpoint5_final_results.pdf

figures/
  Report figures, if exported separately

requirements.txt                   Python dependencies


```markdown
The checkpoint PDFs are included to document the model development process, including hyperparameter tuning, production-mode testing, cross-validation, and final held-out test evaluation.