# MNIST LLC Dynamics Experiment

### Overview
This repository contains a replication of Local Learning Coefficient (LLC) dynamics on a simple MLP trained on MNIST. The goal was to validate the "developmental stages" of learning predicted by Singular Learning Theory (SLT).

### The Experiment
* Model: 2-layer MLP (`width=128`, `ReLU`).
* Method: Estimate the local effective dimension ($\widehat{\lambda}$) every 100 steps using SGLD (Stochastic Gradient Langevin Dynamics) via the `devinterp` library.
* Protocol: The model is trained for 2,500 steps (approx. 5 epochs) with a standard SGD optimizer.

### Results
The experiment successfully reproduces the decoupling between Loss and Complexity:
1.  Loss decreases monotonically as expected.
2.  LLC (Complexity) exhibits a sharp drop in the early phase of training, indicating the model collapsed into a simpler, more singular solution before fine-tuning.

### Visualisation
<img width="989" height="590" alt="LLC Experiment Brook (2)" src="https://github.com/user-attachments/assets/0f57f2a4-82d1-405b-a840-415d6b41200c" />
