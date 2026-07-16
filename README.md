# Research Papers and ML Algorithm Scratch Implementations

Core machine learning algorithms implemented from scratch in Python (NumPy/Pandas) to build intuition for the math and mechanics that libraries like scikit-learn abstract away.

## Contents

| # | Notebook | Algorithm | Highlights |
|---|----------|-----------|------------|
| 01 | `Linear_Regression_Scratch` | Linear Regression | Two implementations — batch **gradient descent** and the closed-form **normal equation** — with a custom R² scoring function |
| 02 | `Logistic_Regression_Scratch` | Logistic Regression | Binary classifier built with a numerically stable sigmoid (clipped to avoid overflow) and gradient-based training |
| 03 | `K_Nearest_Neighbors_(KNN)_Scratch` | K-Nearest Neighbors | Classifier using Euclidean distance and majority-vote prediction via `scipy.stats.mode` |
| 04 | `Gradient_Boosting_Regressor_Scratch` | Gradient Boosting Regressor | Additive boosting loop that fits sequential regression trees to residuals, built on top of `sklearn`'s `DecisionTreeRegressor` |
| 05 | `Principal_Component_Analysis_(PCA)_Scratch` | PCA | Dimensionality reduction via mean-centering, covariance, and eigendecomposition, with results validated against `sklearn.decomposition.PCA` |
| 06 | `K_Means_Scratch` | K-Means Clustering | Centroid-based clustering with random initialization, tested on synthetic `make_blobs` data |

## Approach

Each notebook implements the algorithm as a standalone class (`.fit()` / `.predict()` interface, mirroring the scikit-learn API) before, where applicable, comparing results against the library implementation to sanity-check correctness.

## Stack

`numpy` · `pandas` · `scipy` · `matplotlib` · `seaborn` · `scikit-learn` (for benchmarking and utilities like `make_blobs`, `DecisionTreeRegressor`)

## Note

Despite the repo name, the current notebooks are algorithm-from-scratch implementations rather than research paper reproductions — this README reflects the repo as it stands today and will be updated as paper-based implementations are added.

## Usage

Each notebook is self-contained — open in Jupyter or Google Colab and run top to bottom. Note that `05.Principal_Component_Analysis_(PCA)_Scratch.ipynb` includes a Google Colab-specific data mount step; swap in a local file path to run outside Colab.
