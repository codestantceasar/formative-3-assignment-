# Formative 3: Probability Distributions, Bayesian Probability, and Gradient Descent

## Team Members

* Constantine Akas
* [Member 2]
* [Member 3]
* [Member 4]

---

## Project Overview

This project explores:

1. Expectation-Maximization (EM) Algorithm for Gaussian Mixture Models
2. Bayesian Probability using the IMDb Movie Reviews Dataset
3. Manual Gradient Descent Calculations
4. Gradient Descent Implementation in Python

The objective is to understand probability distributions, Bayesian inference, and optimization techniques used in machine learning.

---

## Part 1: Expectation-Maximization (EM)

Dataset:

* Galton Parent and Child Heights Dataset

Tasks Completed:

* Dataset loading and exploration
* Mixture dataset creation
* Histogram visualization
* EM Algorithm implementation from scratch
* Expectation Step (E-Step)
* Maximization Step (M-Step)
* Log-Likelihood calculation
* Optimization tracking table
* Convergence analysis

---

## Part 2: Bayesian Probability

Dataset:

* IMDb Movie Reviews Dataset

Tasks:

* Keyword selection
* Prior probability calculation
* Likelihood calculation
* Marginal probability calculation
* Posterior probability calculation using Bayes' Theorem

---

## Part 3: Manual Gradient Descent

Model: ŷ = (m1·x1) × (m2·x2) + b (multiplicative form, computed via matrix operations)

Tasks Completed:

* Predicted value (ŷ) calculation for both data points
* Error calculation (e = ŷ - y)
* Full derivation of MSE cost function gradient using chain rule
* Gradients derived: dJ/dm1, dJ/dm2, dJ/db1, dJ/db2
* 4 iterations of gradient descent (Iteration 0–3), one per group member
* Intermediate results (predictions, errors, gradients, updated parameters) shown after every iteration
* Trend analysis: confirmed decreasing error and cost function (convergence)
---

## Part 4: Gradient Descent in Code

Tasks:

* Derivative computation using SciPy
* Gradient Descent implementation
* Error tracking
* Parameter tracking
* Visualization using Matplotlib

---

## Technologies Used

* Python
* NumPy
* Pandas
* SciPy
* Matplotlib
* Jupyter Notebook
* GitHub

---

## Repository Structure

Formative3/

├── notebook/

│ └── Formative3.ipynb

├── README.md

├── images/

├── manual_calculations/

├── presentation/

└── contributions/

---

## Current Progress

Completed:

 * Part 1 (EM Algorithm)
 * Part 3 (Manual Gradient Descent)
 
In Progress:

* Part 2 (Bayesian Probability)
* Part 4 (Gradient Descent in Code)



---

## How to Run

1. Clone the repository.
2. Install required dependencies.
3. Open the Jupyter Notebook.
4. Run cells sequentially from top to bottom.

Example:

pip install numpy pandas scipy matplotlib kagglehub

jupyter notebook
