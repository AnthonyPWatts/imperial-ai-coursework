# Notebook Index

This folder contains the more structured, module-aligned notebooks for the Imperial College Business School **Professional Certificate in Machine Learning and Artificial Intelligence** preparation work.

The rough split is:

- `maths-refresh/` — quick pre-course drills and rough practice
- `notebooks/` (this folder) — cleaner, module-aligned notebooks worth keeping
- `course-labs/` — course-provided or course-style lab work
- `scratch/` — disposable experiments

## Working Rule

A notebook is not “done” until it includes:

- the core idea in plain English
- a small manual or visual example
- a Python / NumPy / pandas implementation
- a short note explaining why the concept matters for ML
- at least one tiny exercise or variation

## Notebook Status Key

| Status | Meaning |
|---|---|
| Planned | File/folder identified but not started |
| Draft | First working version exists |
| Review | Needs checking, cleanup, clearer explanation or better examples |
| Complete | Good enough for future reference |
| Superseded | Kept for history, but replaced by a better notebook |

## Foundations Sequence

| Area | Notebook | Status | Purpose |
|---|---|---:|---|
| Linear algebra | `01_linear_algebra_numpy/01_vectors_shapes_norms.ipynb` | Draft | Vectors, array shapes, dimensions, norms and basic NumPy representation |
| Linear algebra | `01_linear_algebra_numpy/02_dot_products_and_projection.ipynb` | Draft | Dot products, projection, cosine similarity and geometric interpretation |
| Linear algebra | `01_linear_algebra_numpy/03_matrices_as_transformations.ipynb` | Draft | Matrices as transformations, matrix multiplication and visual intuition |
| Linear algebra | `01_linear_algebra_numpy/04_eigenvectors_eigenvalues.ipynb` | Draft | Eigenvectors, eigenvalues, transformation stability and PCA groundwork |
| Calculus / optimisation | `02_calculus_optimisation/01_gradient_descent_from_scratch.ipynb` | Draft | Loss functions, gradients, learning rate and optimisation from scratch |
| Probability | `03_probability_numpy/01_coin_flips_and_monte_carlo.ipynb` | Draft | Random simulation, frequencies, Monte Carlo thinking and NumPy randomness |
| Statistics | `04_statistics_pandas/01_summary_statistics_and_outliers.ipynb` | Draft | Mean, median, variance, standard deviation, outliers and pandas summaries |
| ML fundamentals | `05_ml_fundamentals/01_train_validation_test_split.ipynb` | Draft | Train/validation/test split, generalisation and model evaluation workflow |

## Plannned Next Notebooks

Useful additions after the initial foundation set.

| Area | Notebook | Status | Purpose |
|---|---|---:|---|
| Calculus / optimisation | `02_calculus_optimisation/02_learning_rate_experiments.ipynb` | Planned | Show how learning rate affects convergence, oscillation and divergence |
| Probability | `03_probability_numpy/02_bayes_rule_examples.ipynb` | Planned | Bayes' rule using small numerical examples and simulations |
| Statistics | `04_statistics_pandas/02_bootstrapping.ipynb` | Planned | Bootstrap resampling, confidence intervals and uncertainty of estimates |
| ML fundamentals | `05_ml_fundamentals/02_bias_variance_validation.ipynb` | Planned | Underfitting, overfitting, bias-variance trade-off and validation curves |
| KNN / geometry | `06_knn_distance_geometry/01_distance_metrics_and_scaling.ipynb` | Planned | Euclidean/Manhattan distance, feature scaling and why KNN cares |
| Decision trees | `07_decision_trees/01_impurity_and_splits.ipynb` | Planned | Gini, entropy, information gain and decision-tree split logic |

## Folder Map

```text
notebooks/
  01_linear_algebra_numpy/
    01_vectors_shapes_norms.ipynb
    02_dot_products_and_projection.ipynb
    03_matrices_as_transformations.ipynb
    04_eigenvectors_eigenvalues.ipynb

  02_calculus_optimisation/
    01_gradient_descent_from_scratch.ipynb
    02_learning_rate_experiments.ipynb

  03_probability_numpy/
    01_coin_flips_and_monte_carlo.ipynb
    02_bayes_rule_examples.ipynb

  04_statistics_pandas/
    01_summary_statistics_and_outliers.ipynb
    02_bootstrapping.ipynb

  05_ml_fundamentals/
    01_train_validation_test_split.ipynb
    02_bias_variance_validation.ipynb

  06_knn_distance_geometry/
    01_distance_metrics_and_scaling.ipynb

  07_decision_trees/
    01_impurity_and_splits.ipynb
```

## Notebook Template

Use this structure for new notebooks:

```markdown
# Notebook Title

## Purpose

What this notebook is trying to make clear.

## Concept

Plain-English explanation of the maths or ML idea.

## Tiny Manual Example

A small hand-checkable example before code.

## Python Implementation

NumPy / pandas / scikit-learn implementation.

## Visualisation

A simple plot if it helps.

## Why This Matters for ML

Where this concept reappears in the Imperial syllabus.

## Exercises

Small variations to test understanding.
