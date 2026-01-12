# Hybrid Mechanistic and Neural Network-Based Modeling of Tissue Morphogenesis

## Overview

The **Single Genotype Circuit Model** combines Notch signaling with the Cellular Potts Model (CPM) to create a spatiotemporal framework for cellular self-organization. This approach models tissue morphogenesis by considering a mixture of mechanistic biological processes and data-driven learning.

However, traditional numerical ODE solvers become computationally expensive when dealing with large cell populations and nonlinear equations. This project addresses this challenge by **replacing numerical ODE solvers with neural network-based approximations**, combining the interpretability of mechanistic models with the efficiency of deep learning.


##  Project Goals

- Accelerate simulations of tissue morphogenesis using neural network surrogates
- Maintain biological interpretability while improving computational efficiency
- Provide a framework for hybrid mechanistic-ML modeling in developmental biology

<img width="500" height="400" alt="Screenshot 2026-01-12 235619" src="https://github.com/user-attachments/assets/e4e4644a-d445-4bc3-9980-5015ff417003" />

##  Repository Structure

```
Mechanistic-BayseFlowNN/
├── Codes/                              # Main implementation notebooks
│   ├── 1D_ResNet.ipynb                # ResNet architecture for 1D signal prediction
│   ├── Simple_NN.ipynb                # Basic neural network implementation
│   ├── ODE_Solver.ipynb               # Traditional ODE solver baseline
│   ├── JANA_Likelihood_Next_Step. ipynb               # Likelihood estimation for next-step prediction
│   ├── JANA_Likelihood_With_Recurrent_Memmory.ipynb # Recurrent memory-based likelihood model
│   ├── JANA_Liklihood_For_Signal_Prediction.ipynb   # Signal prediction likelihood
│   ├── JANA_Pstrior_Estimation. ipynb                # Posterior estimation using BayesFlow
│   └── Likelihood_Next_Step.ipynb                   # Alternative likelihood implementation
├── Checkpoint/                         # Model checkpoints and saved weights
├── Simulated_Data/                     # Generated simulation data
└── README.md                           # This file
```

##  Getting Started

### Prerequisites

```bash
# Core dependencies (adjust based on your actual requirements)
pip install numpy scipy matplotlib
pip install torch torchvision  # or tensorflow
pip install jupyter notebook
pip install bayesflow  # if using BayesFlow framework
```

### Running the Code

1. **Clone the repository:**
   ```bash
   git clone https://github.com/mikeHayah/Mechanistic-BayseFlowNN.git
   cd Mechanistic-BayseFlowNN
   ```

2. **Start with the ODE Solver baseline:**
   ```bash
   jupyter notebook Codes/ODE_Solver.ipynb
   ```

3. **Explore neural network alternatives:**
   - `Simple_NN.ipynb` - Basic neural network approach
   - `1D_ResNet.ipynb` - ResNet architecture for improved performance

4. **Bayesian inference and parameter estimation:**
   - `JANA_Pstrior_Estimation.ipynb` - Posterior distribution estimation
   - `JANA_Likelihood_*` notebooks - Various likelihood estimation approaches

##  Methods

### Mechanistic Component
- **Notch Signaling Model**: Lateral inhibition pathway governing cell fate decisions
- **Cellular Potts Model (CPM)**: Energy-based framework for cell shape and movement
- **ODE System**: Coupled differential equations describing protein dynamics

### Neural Network Component
- **ResNet Architecture**: Deep residual networks for capturing temporal dynamics
- **Recurrent Models**: Memory-based architectures for sequential prediction
- **Likelihood Approximation**: Neural density estimation for Bayesian inference

### Bayesian Framework
- **Parameter Estimation**:  Posterior inference using simulation-based methods
- **BayesFlow Integration**: Amortized Bayesian inference framework
- **Uncertainty Quantification**: Probabilistic predictions with confidence intervals

##  Key Features

- Fast surrogate models replacing expensive ODE solvers
- Jupyter notebooks for interactive exploration


##  Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

##  Citation

If you use this code in your research, please cite:

```bibtex
@misc{mechanistic-bayesflownn,
  author = {Sina Salehi and Michael Hanna},
  title = {Hybrid Mechanistic and Neural Network-Based Modeling of Tissue Morphogenesis},
  year = {2023},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/mikeHayah/Mechanistic-BayseFlowNN}}
}
```

##  Authors and Acknowledgments

**Authors:**
- **Sina Salehi** - [GitLab](https://gitlab.com/Sinasall)
- **Michael Hanna** - [GitHub](https://github.com/mikeHayah)

**Supervision:**
- **Dr. Lutz Brusch**
- **Robert Müller**

**Affiliation:**  
Technische Universität Dresden  
Project initiated:  April 2023

##  License

This project is open source under the MIT License.  Please add an appropriate license file if you plan to specify usage terms.

---

**Keywords:** Tissue Morphogenesis, Neural Networks, Bayesian Inference, Cellular Potts Model, Notch Signaling, BayesFlow, Deep Learning, Computational Biology
