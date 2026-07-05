# Formative 3: Probability Distributions, Bayesian Probability, and Gradient Descent

## Team Members

* Constantine Akas Chidiebere
* Regina Anthony Majura
* Keyla Nyacyesa Bineza
* Ndunge Mutheu Mbithi 

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

## Part 1: Expectation-Maximization (EM) Algorithm

### Dataset

We used the Galton Parent and Child Heights Dataset, which contains height measurements for parents and their children.

Key columns explored:

* Father Height
* Mother Height
* Child Height
* Gender
* Midparent Height

For this project, we combined father heights and child heights into a single dataset and intentionally removed the labels to simulate a mixture of two unknown populations.


# Problem Statement

The objective was to determine whether a set of height observations could be separated into two hidden groups using the Expectation-Maximization (EM) Algorithm.

Instead of using the original labels, the model was required to discover the hidden populations through probability distributions.



# Why We Did Not Split the Dataset at the Mean

A simple approach would be to calculate the global mean and split the dataset into two groups.

However, this approach is inappropriate because the two height distributions overlap significantly.

Individuals with heights near the center of the distribution could belong to either population.

A hard split would therefore introduce classification errors.

The EM algorithm solves this problem by assigning probabilities to each observation rather than forcing observations into a single group.


 # Data Visualization

A histogram of the combined height data was created to visualize the distribution of heights.

The visualization revealed:

* Significant overlap between populations
* Multiple peaks within the distribution
* No obvious threshold for separating groups

This justified the use of a probabilistic clustering approach.


### EM Algorithm Implementation

The EM algorithm was implemented completely from scratch in Python.

#### Step 1: Initialization

Initial parameter estimates:

| Parameter | Value  |
| --------- | ------ |
| μ1        | 66.000 |
| μ2        | 70.000 |
| σ1        | 3.311  |
| σ2        | 3.311  |
| π1        | 0.500  |
| π2        | 0.500  |



### Step 2: Expectation Step (E-Step)

For each height observation, the algorithm computed:

* P(Group 1 | Height)
* P(Group 2 | Height)

These posterior probabilities are called responsibilities.

Responsibilities determine how strongly each observation belongs to each Gaussian distribution.

---

#### Step 3: Maximization Step (M-Step)

Using the responsibilities calculated during the E-Step, the algorithm updated:

* Mean (μ)
* Standard Deviation (σ)
* Mixing Coefficient (π)

The updated parameters were then used in the next iteration.

---

### Optimization Tracking Table

| Iteration | μ1     | μ2     | σ1    | σ2    | π1    | π2    | Log-Likelihood |
| --------- | ------ | ------ | ----- | ----- | ----- | ----- | -------------- |
| 0         | 66.000 | 70.000 | 3.311 | 3.311 | 0.500 | 0.500 | N/A            |
| 1         | 66.403 | 69.519 | 3.115 | 2.718 | 0.497 | 0.503 | -4873.516      |
| 2         | 66.373 | 69.530 | 3.199 | 2.599 | 0.494 | 0.506 | -4869.372      |

---

### Convergence Analysis

The log-likelihood improved from:

-4873.516 → -4869.372

This indicates that the model was finding parameters that better explained the observed data.

The means also stabilized between iterations, suggesting that the EM algorithm was approaching convergence.

---

### Classification Demonstration

After training, the model can classify any height by computing posterior probabilities.

Example:

For a given height, the model outputs:

* Probability of belonging to Group 1
* Probability of belonging to Group 2

The observation is assigned to the group with the higher probability.

This probabilistic approach is more reliable than a simple mean-based split because it accounts for overlap between distributions.

---

### Key Learning Outcomes

Through this section we learned:

* How Gaussian Mixture Models represent hidden populations.
* Why probabilistic clustering is superior to hard thresholding.
* How the Expectation-Maximization algorithm alternates between estimating probabilities and updating parameters.
* How log-likelihood can be used to monitor convergence and model performance.


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

Tasks:

* Prediction calculation
* Mean Squared Error computation
* Chain Rule derivation
* Gradient calculations
* Parameter updates
* Iteration tracking

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

├── data/
│ └── IMDB Dataset.csv

└── part3/
│ └── Iteration 0.pdf
│ └── Iteration 1 (Constantine).pdf
│ └── Iteration3.pdf
│ └── Number 1.pdf
│ └── Number 2 (1).pdf
│ └──Number 7.pdf



---

## Current Progress

Completed:

* Part 1 (EM Algorithm)
* Part 2 (Bayesian Probability)
* Part 3 (Manual Gradient Descent)
* Part 4 (Gradient Descent in Code)

---

## How to Run

1. Clone the repository.
2. Install required dependencies.
3. Open the Jupyter Notebook.
4. Run cells sequentially from top to bottom.


