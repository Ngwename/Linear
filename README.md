# Linear Regression from Scratch using Normal Equation and Gradient Descent

Te project uses two approaches: 

1. **Closed form Solution**— solves for the best coefficients directly using linear algebra(The normal equation - β̂ = (XᵀX)⁻¹ Xᵀ y).  
2. **Gradient Descent** — Iteratively updates parameters to minimize Mean Square Error.

The dataset is randomly generated with NumPy using a fixed random seed for reproducibility.


## What This Code Does

### 1) Generate a Dataset
- Creates 200 random `x` values in the range `[0, 1)`
- Generates `y` using the relationship:

\[
y = 3 + 4x + \{noise}
\]

- Adds Gaussian noise to simulate real-world data

### 2) Fit Using the Normal Equation (Closed Form)
- Adds a bias term (intercept) to `x`:
  - `X_b = [1, x]`
- Computes:

\[
\theta_normal = (X^T X)^{-1} X^T y
\]

- Plots the fitted regression line against the data points.

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

Install dependencies:

```bash
pip install numpy matplotlib
