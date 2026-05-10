# Imperial ML/AI Programme Module Map

This file maps the Imperial College Business School *Professional Certificate in Machine Learning and Artificial Intelligence* syllabus to the supporting preparation work in this repo.

The aim is not to duplicate the course material. The aim is to keep a practical bridge between:

- mathematical intuition
- Python / NumPy / pandas fluency
- Jupyter notebook practice
- machine learning concepts
- capstone readiness

## Repo Learning Principle

For each module, create or update at least one notebook that answers:

> What is the mathematical idea, how do I express it in Python, and why does it matter for ML?

Suggested notebook pattern:

```text
Concept
Intuition
Manual calculation
Python / NumPy implementation
ML relevance
Tiny exercise
Reflection notes
```

## Phase 1 — Foundations of ML and AI

| Module | Course topic | Maths focus | Python focus | Suggested repo artefact |
|---|---|---|---|---|
| 0 | Programme Orientation and Programming Tools | None | Environment, Jupyter, repo hygiene | `notes/setup-notes.md` |
| 1 | Mathematical Concepts in ML/AI | Vectors, matrices, transformations, eigenvalues, derivatives, partial derivatives, chain rule, norms, gradient descent | NumPy arrays, matrix ops, plotting, from-scratch optimisation | `notebooks/01_linear_algebra_numpy/` and `notebooks/02_calculus_optimisation/` |
| 2 | Introduction to Machine Learning | Functions, variables, inputs/outputs, regression vs classification | pandas basics, missing data handling, simple ML workflow | `notebooks/05_ml_fundamentals/01_missing_data_and_ml_workflow.ipynb` |
| 3 | Probability for Machine Learning | Probability, independence, Bayes' rule, binomial distribution, CLT, normal distribution | NumPy random simulations, Monte Carlo, frequencies, summary stats | `notebooks/03_probability_numpy/` |
| 4 | Statistics for Machine Learning | Mean, median, variance, standard deviation, outliers, correlation, regression, bootstrapping, MLE | pandas summaries, scipy/sklearn basics, bootstrap resampling | `notebooks/04_statistics_pandas/` |
| 5 | Generalisation Theory and the Bias–Variance Trade-Off | Candidate functions, sample size, train/validation/test split, bias vs variance | Validation experiments, parameter sweeps, plotting underfit/overfit | `notebooks/05_ml_fundamentals/02_bias_variance_validation.ipynb` |
| 6 | Basics of Predictive Performance Evaluation | MAE, MSE, RMSE, confusion matrix, classification metrics | Implement metrics manually, then compare with scikit-learn | `notebooks/05_ml_fundamentals/03_metrics_from_scratch.ipynb` |
| 7 | Advanced Predictive Performance Evaluation | Class imbalance, stratified sampling, oversampling, undersampling, k-fold cross-validation | `train_test_split`, `StratifiedKFold`, resampling, validation loops | `notebooks/05_ml_fundamentals/04_cross_validation_and_imbalance.ipynb` |

## Phase 2 — ML Methods

| Module | Course topic | Maths focus | Python focus | Suggested repo artefact |
|---|---|---|---|---|
| 8 | Nearest Neighbour Methods | Distance functions, normalisation, decision boundaries, curse of dimensionality | KNN classifier/regressor, scaling, categorical encoding | `notebooks/06_knn_distance_geometry/` |
| 9 | Decision Trees: Part One | Misclassification rate, entropy, Gini index, information gain | Decision tree classifier, impurity criteria, visualisation | `notebooks/07_decision_trees/01_impurity_and_splits.ipynb` |
| 10 | Decision Trees: Part Two | Pruning, tree complexity, variance control | Tree depth, min samples, pruning experiments | `notebooks/07_decision_trees/02_pruning_and_generalisation.ipynb` |
| 11 | Naïve Bayes | Conditional probability, independence assumptions, Bayes' rule | Naïve Bayes classifier, text/count examples | `notebooks/08_bayesian_methods/01_naive_bayes.ipynb` |
| 12 | Bayesian Optimisation | Search spaces, acquisition functions, optimisation under uncertainty | Hyperparameter search, simple Bayesian optimisation demo | `notebooks/08_bayesian_methods/02_bayesian_optimisation.ipynb` |
| 13 | Logistic Regression | Log odds, sigmoid, likelihood, decision boundary | Logistic regression from sklearn and partial from-scratch implementation | `notebooks/09_linear_models/01_logistic_regression.ipynb` |
| 14 | Support Vector Machines | Margins, separating hyperplanes, kernels | Linear SVM, kernel SVM, scaling effects | `notebooks/09_linear_models/02_support_vector_machines.ipynb` |

## Phase 3 — Deep Learning, Neural Networks and More

| Module | Course topic | Maths focus | Python focus | Suggested repo artefact |
|---|---|---|---|---|
| 15 | Neural Networks and Deep Learning: Part One | Perceptrons, activations, weighted sums, loss | Simple neural net concepts, maybe sklearn MLP first | `notebooks/10_neural_networks/01_neural_network_basics.ipynb` |
| 16 | Neural Networks and Deep Learning: Part Two | Backpropagation, gradients, optimisation, regularisation | Small PyTorch or TensorFlow model, training loop concepts | `notebooks/10_neural_networks/02_training_loops_and_backprop.ipynb` |
| 17 | Neural Networks and Deep Learning: Part Three: CNNs | Convolution, filters, feature maps, pooling | Basic CNN notebook using an image dataset | `notebooks/10_neural_networks/03_convolutional_neural_networks.ipynb` |
| 18 | Hyperparameters and Hyperparameter Tuning | Search strategy, validation, performance trade-offs | Grid search, random search, cross-validation | `notebooks/11_model_selection/01_hyperparameter_tuning.ipynb` |
| 19 | Foundations of Generative AI and Large Language Models | Tokens, embeddings, probability distributions, attention intuition | Small experiments with tokenisation and embeddings | `notebooks/12_generative_ai/01_llm_foundations.ipynb` |
| 20 | Advanced Generative AI and Large Language Models | Prompting, RAG concepts, evaluation, risks | API/local model experiments, structured prompts, retrieval toy example | `notebooks/12_generative_ai/02_llm_applications.ipynb` |
| 21 | Transparency and Interpretability | Feature importance, model explanation, local vs global explanations | Permutation importance, SHAP/LIME-style concepts if appropriate | `notebooks/13_interpretability/01_model_explainability.ipynb` |
| 22 | Unsupervised Learning: Part One: Clustering Techniques | Distance, centroids, variance, cluster separation | k-means, hierarchical clustering, scaling effects | `notebooks/14_unsupervised_learning/01_clustering.ipynb` |
| 23 | Unsupervised Learning: Part Two: Principal Component Analysis | Eigenvectors, eigenvalues, covariance, projection | PCA from sklearn and partial NumPy implementation | `notebooks/14_unsupervised_learning/02_principal_component_analysis.ipynb` |
| 24 | Reinforcement Learning | States, actions, rewards, policies, value functions | Small grid-world or bandit simulation | `notebooks/15_reinforcement_learning/01_rl_basics.ipynb` |
| 25 | Capstone Project | Integrated modelling, evaluation, explanation, trade-offs | End-to-end project workflow | `capstone/` |

## Preparation Priority

Before the course starts, focus on these areas first:

1. **Linear algebra with NumPy**
   - vectors
   - dot product
   - norms
   - matrix multiplication
   - transformations
   - eigenvalues and eigenvectors

2. **Scientific Python workflow**
   - Jupyter
   - NumPy array shapes
   - pandas DataFrames
   - matplotlib
   - scikit-learn `fit` / `predict` pattern

3. **Optimisation intuition**
   - loss functions
   - gradients
   - learning rate
   - gradient descent from scratch

4. **Probability and statistics**
   - random simulation
   - Bayes' rule
   - binomial distribution
   - normal distribution
   - CLT
   - bootstrapping

## First Notebook Sequence

Create these before going deep into the course:

```text
notebooks/01_linear_algebra_numpy/01_vectors_shapes_norms.ipynb
notebooks/01_linear_algebra_numpy/02_dot_products_and_projection.ipynb
notebooks/01_linear_algebra_numpy/03_matrices_as_transformations.ipynb
notebooks/01_linear_algebra_numpy/04_eigenvectors_eigenvalues.ipynb
notebooks/02_calculus_optimisation/01_gradient_descent_from_scratch.ipynb
notebooks/03_probability_numpy/01_coin_flips_and_monte_carlo.ipynb
notebooks/04_statistics_pandas/01_summary_statistics_and_outliers.ipynb
notebooks/05_ml_fundamentals/01_train_validation_test_split.ipynb
```

## Cross-Module Concept Index

| Concept | First appears | Reappears in |
|---|---:|---|
| Vectors | Module 1 | KNN, SVM, neural networks, embeddings, PCA |
| Matrices | Module 1 | regression, neural networks, CNNs, PCA |
| Eigenvalues/eigenvectors | Module 1 | PCA |
| Norms | Module 1 | distance metrics, loss functions, regularisation |
| Gradient descent | Module 1 | logistic regression, neural networks, deep learning |
| Bayes' rule | Module 3 | Naïve Bayes, Bayesian optimisation |
| Normal distribution | Module 3 | statistics, model assumptions, uncertainty |
| Correlation/regression | Module 4 | predictive modelling, feature analysis |
| Bias-variance | Module 5 | model selection, KNN, trees, hyperparameter tuning |
| Confusion matrix | Module 6 | classification evaluation throughout |
| Cross-validation | Module 7 | hyperparameter tuning, model comparison |
| Distance metrics | Module 8 | KNN, clustering, embeddings |
| Entropy/Gini | Module 9 | decision trees, feature splitting |
| PCA | Module 23 | dimensionality reduction, visualisation, preprocessing |

## Personal Working Rule

Do not move a concept to “understood” until there is:

- a handwritten or typed explanation
- a small manual example
- a NumPy or pandas implementation
- one note explaining where it appears in ML

## Status Checklist

- [ ] Repo structure created
- [ ] First LA notebook created
- [ ] NumPy array shape notes written
- [ ] Gradient descent notebook created
- [ ] Probability simulation notebook created
- [ ] Statistics notebook created
- [ ] First sklearn workflow notebook created
- [ ] Capstone folder created
