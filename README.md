# Hybrid mechanistic and neural network-based modeling of tissue morphogenesis

Single Genotype Circuit Model tries to combine the simple Notch signaling with the cellular Potts model (CPM) to make a spatiotemporal model for cellular self-organization which consider a mixture of cells of a single genotype. These cells can become ‘activated’ through lateral inhibition and eventually self-organize into a stable two-layer structure. This model has been described with 4 ODEs, which are trying to predict each cell’s behavior in time concerning its neighborhood. This can be done by calculating 4 following four parameters for all cells in each stage: Notch level (N ), Notch intracellular domain (I), E-cad production (E), and Delta level (D).
However, concerning the huge amount of cells and also nonlinear equations, this calculation can be costly in some cases. In this study, we tried to replace numerical ODE solver methods with neural network-based methods to improve the efficiency of the simulation. First, we focused on the BayesFlow framework and tried to explain how we use this framework to estimate the time series according to the initial conditions and other parameters in the ODE system. Then, we also tried other types of neural networks for solving this problem. In the end, there were significant results that can give us some hope for improving the simulation’s speed in this model.

This repository contains our code and data for the team project started in April 2023 at Technische Universität Dresden under the supervision of Dr. Lutz Brusch and Robert Müller.



## Authors and acknowledgment
Sina Salehi https://gitlab.com/Sinasall
Michael Hanna 
Supervision: Dr. Lutz Brusch and Robert Müller


