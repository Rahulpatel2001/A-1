# Linear Regression Assignment

## Student Information
- **Name:** [RAHUL KUDURU]
- **Student ID:** [700763240]
- **Course:** [MACHINE LEARNING]
- **Date:** [09/08/2025]

---

## Assignment Overview
This assignment covers:
1. Function approximation by hand.
2. Random guessing practice.
3. First gradient descent iteration.
4. Comparison of random guessing vs. gradient descent.
5. Recognizing underfitting and overfitting.
6. Comparing machine learning models (bias-variance tradeoff).
7. Programming problem: Implement Linear Regression using Gradient Descent and compare with the closed-form solution.

---

## Tasks Summary

### 1. Function Approximation by Hand
- Dataset: (x,y) = {(1,1),(2,2),(3,2),(4,5)}
- Model θ=(1,0):
  - MSE = 4.50
- Model θ=(0.5,1):
  - MSE = 0.75
- **Conclusion:** Model (0.5,1) fits better (lower MSE).

### 2. Random Guessing Practice
- J(0.1,0.2) = 0.290
- J(0.5,0.9) = 0.080
- True minimum at (0.3,0.7).
- (0.5,0.9) is closer to the minimum.
- **Conclusion:** Random guessing is inefficient because it wastes computation without using gradient information to improve guesses systematically.

### 3. First Gradient Descent Iteration
- Dataset: (1,3),(2,4),(3,6),(4,5)
- Start θ=(0,0), α=0.01
- Residual sums: ∑r = 18.0, ∑xr = 49.0
- Gradient = [ -7. -21.]
- Updated θ = [0.09  0.245]
- Cost J before update = 21.50
- Cost J after update = 15.26

### 4. Random Guessing vs Gradient Descent
- Dataset: (1,2),(2,2),(3,4),(4,6)
- Random guesses:
  - θ=(0.2,0.5): J = 5.515
  - θ=(0.9,0.1): J = 7.935
- Gradient Descent (after first step): J = 10.509
- **Conclusion:** Gradient Descent performed better than random guessing because it reduces error systematically.

### 5. Recognizing Underfitting/Overfitting
- Training error high + test error high → **Underfitting**.
- Happens because the model is too simple or features are insufficient.
- Fixes:
  - Use more complex model (e.g., polynomial regression, more parameters).
  - Improve features (feature engineering, transformations).

### 6. Comparing Models
- Model A: Overfitting (low train error, high test error).
- Model B: Underfitting (high train and test error).
- **Bias-Variance Tradeoff:**
  - Overfitting → low bias, high variance.
  - Underfitting → high bias, low variance.
- Recommendations:
  - For Model A: add regularization, reduce complexity, get more training data.
  - For Model B: increase complexity, add features, reduce bias.

### 7. Programming Problem
- Implemented Linear Regression with Gradient Descent vs Closed-Form solution.
- Dataset generated with y = 3 + 4x + ε, x∈[0,5], n=200.
- **Closed-Form Solution:**
  - Estimated slope and intercept printed by code.
  - Fitted line plotted.
- **Gradient Descent:**
  - θ initialized to [0,0], learning rate 0.05, 1000 iterations.
  - Loss curve plotted.
  - Final slope and intercept printed by code.
- **Comparison:**
  - Gradient Descent converged to nearly the same solution as the closed form.

---

## How to Run
1. Clone this repository:
   ```bash
   git clone <your_repo_link>
   cd <repo_folder>
   ```
2. Run the Python file:
   ```bash
   python linear_regression_gd_vs_closed_form.py
   ```
3. Check the generated plots inside the `plots/` folder.

---

## Deliverables
- Python code: `linear_regression_gd_vs_closed_form.py`
- README file with explanation and student info
- Plots:
  - Raw data + fitted lines
  - Gradient Descent loss curve

---

## Notes
- Code is fully commented for clarity.
- Gradient Descent and Closed-Form gave almost identical results, proving correctness.
