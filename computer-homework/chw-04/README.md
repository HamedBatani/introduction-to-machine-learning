# CHW4 — Neural Networks, Convolution, Kernels, and Gaussian Processes

I worked across parametric neural models and kernel methods, implementing core computations and examining the assumptions behind their performance. This assignment is particularly relevant to my machine-learning interests because it connects mathematical differentiation, numerical verification, model design, uncertainty, and robustness.

| Question | My work | Evidence |
|---|---|---|
| 1.1–1.2 | Inspect and standardize breast-cancer data using training statistics; establish a linear baseline | Exploratory plots, accuracy, confusion matrix, coefficient analysis |
| 1.3 | Implement a multi-layer perceptron and binary cross-entropy/backpropagation with NumPy | Layer computation and training loop |
| 1.4 | Compare analytic derivatives with finite differences for sampled parameters | Reported gradient-check relative errors |
| 1.5 | Compare activation, initialization, and regularization choices | Training curves and experiment table |
| 2.1 | Implement 2D convolution with padding/stride and analyze receptive fields | Manual-image filters and output comparisons |
| 2.2–2.3 | Build PyTorch loaders for 8×8 digits; compare FlattenMLP and SmallCNN | Model definitions, training/evaluation loops, results |
| 2.4–2.5 | Design BetterCNN under a 100,000-parameter limit; inspect errors | Parameter counts, accuracy comparison, confusion matrix, high-confidence errors |
| 2.6 bonus | Evaluate shifted, noisy, and low-contrast digit test sets and discuss augmentation | Distribution-shift results and augmentation code |
| 3.1 | Implement linear, polynomial, RBF, and custom kernels; examine Gram eigenvalues | Numerical PSD checks; finite-sample checks alone are not a universal kernel proof |
| 3.2 | Compare kernel SVMs on Wine data; select RBF settings with validation data and visualize 2D boundaries | Validation search and classifier comparisons |
| 3.3–3.4 | Fit Gaussian processes on a BMI/diabetes progression task using RBF and Rational Quadratic kernels; compare neural/kernel approaches | Predictive means, uncertainty bands, written discussion |
| 3.5 bonus | Explore approximate kernels through Nyström features | Approximation and scaling comparison |
| 3.6 bonus | Add a pool point chosen by maximum predictive standard deviation and refit the GP | Before/after uncertainty plots |

The supplied metadata identifies the breast-cancer, digits, wine, and diabetes datasets as scikit-learn teaching datasets. These exercises are benchmark learning experiments, not clinical validations.

The student notebook has saved outputs and no saved exceptions; one code cell has no saved execution count. The original student template is in the alternate archive. All supplied split files and dataset metadata are retained under `data/`. Model comparisons and recorded metrics should be interpreted as results of the saved run until a fresh, version-controlled execution is performed.


## Files and use

[solution.ipynb](solution.ipynb) | [Cell-by-cell guide](CELL_GUIDE.md) | [Archive audit](../../AUDIT.md)

Open Jupyter in this folder so relative paths resolve. The notebook includes course-provided prompts as well as my solutions; assignment wording is not claimed as my authorship. Saved outputs are retained from the source archive.
