# Linear Regression from Scratch using Normal Equation and Gradient Descent

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![NumPy](https://img.shields.io/badge/NumPy-Required-orange.svg)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Required-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## Table of Contents

- [What This Code Does](#what-this-code-does)
- [Generate a Dataset](#1-generate-a-dataset)
- [Fit Using the Normal Equation](#2-fit-using-the-normal-equation-closed-form)
- [Fit Using Gradient Descent](#3-fit-using-gradient-descent)
- [Requirements](#requirements)

---

Te project uses two approaches:

1. **Closed form Solution** — solves for the best coefficients directly using linear algebra  
   (The normal equation - $\hat{\beta} = (X^{T}X)^{-1} X^{T} y$)

2. **Gradient Descent** — Iteratively updates parameters to minimize Mean Square Error.

The dataset is randomly generated with NumPy using a fixed random seed for reproducibility.

---

## What This Code Does

### 1) Generate a Dataset

- Creates 200 random `x` values in the range `[0, 1)`
- Generates `y` using the relationship:

$$
y = 3 + 4x + \{noise}
$$

- Adds Gaussian noise to simulate real-world data

---

### 2) Fit Using the Normal Equation (Closed Form)

- Adds a bias term (intercept) to `x`:

  ```
  X_b = [1, x]
  ```

- Computes:

$$
\theta_{normal} = (X^{T} X)^{-1} X^{T} y
$$

- Plots the fitted regression line against the data points.

---

### 3) Fit Using Gradient Descent

- Starts parameters at `[0, 0]`
- Uses a learning rate of `0.05`
- Runs 1000 iterations:

  - Computes predictions  
  - Calculates **MSE Loss**  
  - Computes gradients  
  - Updates parameters  

- Plots:
  - Gradient descent regression line
  - MSE vs Iterations curve

---

## Requirements

- Python 3.8+
- NumPy
- Matplotlib

  Edward Ng'wena
  700792495

<details>
<summary>Install dependencies</summary>

```bash
pip install numpy matplotlib
```

</details>
