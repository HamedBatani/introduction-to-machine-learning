# CHW2 — Numerical Optimization and Constrained Learning

I compared optimization methods through their trajectories and numerical behavior rather than only writing down update rules. The work examines saddle points, momentum, second-order information, adaptive step sizes, differentiable distribution fitting, and constrained objectives.

| Exercise | My work | Interpretation |
|---|---|---|
| 1: Nonconvex optimization | Implement gradient descent, momentum, and Newton-style updates; use PyTorch automatic differentiation to obtain derivatives | Compare trajectories and sensitivity to starting points near a saddle |
| 2: Backtracking line search | Implement Armijo–Goldstein-style step selection on an ill-conditioned objective | Examine objective decrease and varying step sizes |
| 3: Gaussian KL minimization | Optimize Gaussian parameters with Adam; compare diagonal covariance and a full covariance parameterized through a Cholesky factor | Show how correlation changes the achievable distribution fit while keeping covariance positive definite |
| 4: Constrained optimization | Derive KKT conditions and the analytic feasible solution; implement an increasing-penalty numerical experiment | Contrast exact constraints with finite-penalty optimization |

The final penalty iterate in the saved experiment is approximately `(0.1771, 1.2141)`, rather than the analytic `(1,1)` solution, and has a substantial equality residual. I retain this as an example of a numerical method that needs further convergence work. A large penalty alone is not proof of constraint satisfaction.

There are 17 code cells, no saved error outputs, and one cell without a saved execution count. Running from a clean kernel remains necessary before treating the notebook as fully reproducible. The original notebook is preserved in the archive; the standalone plot files supplied with it are in `Plots/`.


## Files and use

[solution.ipynb](solution.ipynb) | [Cell-by-cell guide](CELL_GUIDE.md) | [Archive audit](../../AUDIT.md)

Open Jupyter in this folder so relative paths resolve. The notebook includes course-provided prompts as well as my solutions; assignment wording is not claimed as my authorship. Saved outputs are retained from the source archive.
