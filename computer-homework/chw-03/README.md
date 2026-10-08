# CHW3 — Regression, Discriminant Analysis, and Bayesian Inverse Problems

I investigated how model assumptions affect regression, classification, and reconstruction. The notebook moves from gradient-based linear regression to regularized fitting, Gaussian generative classifiers, nonconstant observation noise, and an underdetermined inverse problem informed by historical data.

| Section | My implementation and analysis | Available evidence |
|---|---|---|
| 1.1: Simple regression | Implement gradient descent for a single-input housing-price model | Fitted line and optimization outputs |
| 1.2: Multiple regression | Extend regression to several explanatory features | Model coefficients, predictions, and error comparisons |
| 1.3: Regularization | Explore ridge/L2 and lasso/L1 penalties | Changes in fitting behavior and parameter magnitude |
| 2: LDA and QDA | Estimate class statistics and compare shared versus class-specific covariance decision boundaries | Classification plots and noise experiments |
| 2: Gaussian generation | Sample fitted class-conditional distributions and compare generated/original statistics | KL and moment-matching discussion |
| 3.1: Heteroskedastic regression | Model input-dependent noise variance and apply weighted least squares | Data scatter, weighting, fitted parameters |
| 3.2: Complexity and overfitting | Compare model complexity, train/test errors, and weight amplitude | Complexity-versus-MSE plot and written interpretation |
| 3.3: Bayesian inverse problem | Learn a Gaussian prior from historical 50-dimensional signals and reconstruct signals from 20 measurements with a quadratic prior penalty | Objective derivation and reconstruction code; accuracy evaluation needs correction |

For Problem 3.3, the supplied data include `X_true_batch.csv`. The submitted code instead compares reconstructions of the new batch to `X_historical[:20]`. Consequently, the printed MSE of 0.9046 and plots labeled “Original” are **not valid batch-reconstruction accuracy evidence**. Correct evaluation must match each reconstructed measurement to its corresponding true batch signal, check CSV headers and dimensions, and rerun the experiment. The prior-regularized formulation remains visible, but I do not claim successful reconstruction based on that number.

The main published notebook is the student-number version without the `_final` suffix: it contains 42 code cells, saved outputs, and no saved exceptions. The separate `_final` version contains shape errors and is kept in the alternate archive with the original template and exploratory `xxx` version. This selection is based on the files' contents, not their filenames.


## Files and use

[solution.ipynb](solution.ipynb) | [Cell-by-cell guide](CELL_GUIDE.md) | [Archive audit](../../AUDIT.md)

Open Jupyter in this folder so relative paths resolve. The notebook includes course-provided prompts as well as my solutions; assignment wording is not claimed as my authorship. Saved outputs are retained from the source archive.
