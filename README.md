# Neural-ODE-Population-Dynamics

This project implements Neural Ordinary Differential Equations (Neural ODEs) to model population dynamics governed by differential equations, such as logistic growth and the Lotka–Volterra predator-prey system.

---

## 🧠 Motivation

Classical ODE systems are limited by known, fixed dynamics. Neural ODEs allow **learning dynamics directly from time series data** using differentiable solvers.

We test this on:
- 1D logistic growth
- 2D predator-prey interaction

---

## ⚙️ Model

We solve systems of the form:

$$
\frac{dx}{dt} = f_\theta(x(t), t)
$$

where $f_\theta$ is a neural network trained via backpropagation through an ODE solver (e.g., RK4 or adaptive solvers).

---

## 📦 Implementation

- Built with **PyTorch** and **`torchdiffeq`**
- Fully differentiable training loop
- Mean squared error loss on trajectories
- Batch training with mini-sequences
- Visualization of learned vector fields

---

## 🔬 Results

- Neural ODE learns accurate trajectories from noisy observations
- Recovers fixed points and periodic behavior in 2D systems
- Matches analytical solutions for logistic dynamics

---

## 📁 Files

| File             | Description                                |
|------------------|--------------------------------------------|
| `ONN.ipynb`      | Full implementation of Neural ODEs         |
| `generate_data.py` | Functions to create synthetic trajectories |
| `train_model.py` | Training loop using torchdiffeq solvers    |
| `plot_dynamics.py` | Phase portraits, predictions, ground truth |

---

## 📚 References

- Chen et al. (2018), *Neural Ordinary Differential Equations*
- Rubanova et al. (2019), *Latent ODEs for Irregular Time Series*
- Rackauckas et al. (2020), *Universal Differential Equations*

---

## 👤 Author

**Felipe Bedoya**  
PhD Candidate, Bayesian & Quantitative Modeling  
📧 fb31@rice.edu  
🔗 [GitHub](https://github.com/FbStatsQuant)
