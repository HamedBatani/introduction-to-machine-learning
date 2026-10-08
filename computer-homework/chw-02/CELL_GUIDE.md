# CHW2 — Notebook navigation

Cell indices refer to the unmodified source notebook, before the added archival note. This guide maps the available prompts, code, and saved textual outputs; see the README for their interpretation.

### solution.ipynb: original cell 0 (markdown)

# Introduction to Machine Learning
### Practical Homework 2
#### Sharif Uni. of Tech. - EE Dep. - 1404-2 Semester
#### Deadline: 1405-02-26

Opening: `# Introduction to Machine Learning`


### solution.ipynb: original cell 1 (markdown)

# Problem 1: Escaping Saddle Points (First-Order vs. Second-Order Methods) - 25 points
## 1.1 The Objective Function

Opening: `# Problem 1: Escaping Saddle Points (First-Order vs. Second-Order Methods) - 25 points`


### solution.ipynb: original cell 2 (code)

Opening: `import torch`

Saved execution count: 50. Outputs: 0.


### solution.ipynb: original cell 3 (markdown)

## 1.2 Implementing First-Order Methods from Scratch

Opening: `## 1.2 Implementing First-Order Methods from Scratch`


### solution.ipynb: original cell 4 (code)

Opening: `import torch`

Saved execution count: 51. Outputs: 0.


### solution.ipynb: original cell 5 (markdown)

## 1.3 Implementing Second-Order Methods (Newton's Method)

Opening: `## 1.3 Implementing Second-Order Methods (Newton's Method)`


### solution.ipynb: original cell 6 (code)

Opening: `import torch`

Saved execution count: 52. Outputs: 0.


### solution.ipynb: original cell 7 (markdown)

## 1.4 Execution & Visualization

Opening: `## 1.4 Execution & Visualization`


### solution.ipynb: original cell 8 (code)

Opening: `import torch`

Saved execution count: 53. Outputs: 2.

Saved text excerpt:

```text
<Figure size 1800x500 with 3 Axes>
gd:       θ = (0.000483, 1.326162), loss = -1.970888
momentum: θ = (0.000002, 1.415245), loss = -1.999996
newton:   θ = (0.000000, 0.000000), loss = -0.000000

```


### solution.ipynb: original cell 9 (markdown)

## 1.5 Analytical Questions

Opening: `## 1.5 Analytical Questions`


### solution.ipynb: original cell 10 (markdown)

# Problem 2: Implementing the Armijo-Goldstein Line Search - 25 points
## 2.1 The Mathematics of Armijo-Goldstein

Opening: `# Problem 2: Implementing the Armijo-Goldstein Line Search - 25 points`


### solution.ipynb: original cell 11 (markdown)

## 2.2 The Ill-Conditioned Landscape

Opening: `## 2.2 The Ill-Conditioned Landscape`


### solution.ipynb: original cell 12 (code)

Opening: `import torch`

Saved execution count: 54. Outputs: 0.


### solution.ipynb: original cell 13 (markdown)

## 2.3 Implementing the Armijo-Goldstein Optimizer

Opening: `## 2.3 Implementing the Armijo-Goldstein Optimizer`


### solution.ipynb: original cell 14 (code)

Opening: `def optimize_armijo(init_theta, max_steps=100, eta_init=1.0, c=0.1, tau=0.5):`

Saved execution count: 55. Outputs: 0.


### solution.ipynb: original cell 15 (markdown)

## 2.4 Comparison: Constant LR vs. Armijo-Goldstein

Opening: `## 2.4 Comparison: Constant LR vs. Armijo-Goldstein`


### solution.ipynb: original cell 16 (code)

Opening: `def optimize_constant_lr(init_theta, lr=0.015, steps=50):`

Saved execution count: 56. Outputs: 2.

Saved text excerpt:

```text
<Figure size 900x500 with 1 Axes>
Armijo final loss : 4.012463  |  function evals: 382
Constant LR final loss: 7.276131  |  function evals: 50

```


### solution.ipynb: original cell 17 (markdown)

## 2.5 Analytical Questions

Opening: `## 2.5 Analytical Questions`


### solution.ipynb: original cell 18 (markdown)

# Problem 3: Expanding Model Capacity (Closing the KL-Divergence Gap) - 25 points
## 3.1 The Mathematics of Positive Semi-Definiteness

Opening: `# Problem 3: Expanding Model Capacity (Closing the KL-Divergence Gap) - 25 points`


### solution.ipynb: original cell 19 (code)

Opening: `import torch`

Saved execution count: 57. Outputs: 0.


### solution.ipynb: original cell 20 (markdown)

## 3.2 Multivariate KL-Divergence from Scratch

Opening: `## 3.2 Multivariate KL-Divergence from Scratch`


### solution.ipynb: original cell 21 (code)

Opening: `def kl_divergence_full(mu_q, Sigma_q, mu_p, Sigma_p):`

Saved execution count: 58. Outputs: 0.


### solution.ipynb: original cell 22 (markdown)

## 3.3 Optimization with Adam

Opening: `## 3.3 Optimization with Adam`


### solution.ipynb: original cell 23 (code)

Opening: `from torch.optim import Adam`

Saved execution count: 59. Outputs: 1.

Saved text excerpt:

```text
learned mu     : [ 2.0000136 -0.9999859]
target mu      : [ 2. -1.]

learned Sigma  :
 [[2.0000007 1.5000001]
 [1.5000001 2.5      ]]
target Sigma   :
 [[2.  1.5]
 [1.5 2.5]]

final kl loss  : 0.000000

```


### solution.ipynb: original cell 24 (markdown)

## 3.4 Verification and Visualization

Opening: `## 3.4 Verification and Visualization`


### solution.ipynb: original cell 25 (code)

Opening: `# Create grid for plotting`

Saved execution count: 11. Outputs: 0.


### solution.ipynb: original cell 26 (code)

Opening: `x, y = torch.meshgrid(torch.linspace(-3, 7, 100), torch.linspace(-5, 5, 100), indexing='ij')`

Saved execution count: 60. Outputs: 1.

Saved text excerpt:

```text
<Figure size 1300x500 with 2 Axes>
```


### solution.ipynb: original cell 27 (markdown)

## 3.5 Analytical Questions

Opening: `## 3.5 Analytical Questions`


### solution.ipynb: original cell 28 (markdown)

# Problem 4: Computational KKT Conditions & Penalty Methods - 25 points
## 4.1 Analytical KKT Derivation

Opening: `# Problem 4: Computational KKT Conditions & Penalty Methods - 25 points`


### solution.ipynb: original cell 29 (markdown)

Opening: `**Write your analytical KKT derivation here. Double click to edit.**`


### solution.ipynb: original cell 30 (markdown)

## 4.1 Analytical KKT Derivation
### Problem Setup
### 1. Generalized Lagrangian
### 2. KKT Conditions
### 3. Solution via Case Analysis on Complementary Slackness
#### Case 1 — Inequality constraint **inactive**: $\lambda = 0$
#### Case 2 — Inequality constraint **active**: $g(\theta) = 0$, so $\theta_1^2 + \theta_2 = 2$
### Final Solution

Opening: `## 4.1 Analytical KKT Derivation`


### solution.ipynb: original cell 31 (markdown)

## 4.2 The Exterior Penalty Method

Opening: `## 4.2 The Exterior Penalty Method`


### solution.ipynb: original cell 32 (code)

Opening: `import torch`

Saved execution count: 12. Outputs: 0.


### solution.ipynb: original cell 33 (code)

Opening: `import torch`

Saved execution count: 61. Outputs: 0.


### solution.ipynb: original cell 34 (markdown)

## 4.3 Iterative Optimization

Opening: `## 4.3 Iterative Optimization`


### solution.ipynb: original cell 35 (code)

Opening: `from torch.optim import Adam`

Saved execution count: 62. Outputs: 1.

Saved text excerpt:

```text
rho=     1 | theta=(-1.55698, -0.51847) | h=-5.59e+00 | g=-9.43e-02
rho=    10 | theta=(-1.08703, -0.04971) | h=-4.19e+00 | g=-8.68e-01
rho=   100 | theta=(-0.62904, 0.40804) | h=-2.81e+00 | g=-1.20e+00
rho=  1000 | theta=(-0.19391, 0.84312) | h=-1.51e+00 | g=-1.12e+00
rho= 10000 | theta=(0.17710, 1.21410) | h=-3.95e-01 | g=-7.55e-01

final solution: theta1=0.177102, theta2=1.214100
analytical KKT: theta1=1.000000, theta2=1.000000

```


### solution.ipynb: original cell 36 (markdown)

## 4.4 Evaluation and Visualization

Opening: `## 4.4 Evaluation and Visualization`


### solution.ipynb: original cell 37 (code)

Opening: `grid_x, grid_y = torch.meshgrid(torch.linspace(-3, 3, 200), torch.linspace(-2, 3, 200), indexing='ij')`

Saved execution count: 63. Outputs: 1.

Saved text excerpt:

```text
<Figure size 1000x800 with 2 Axes>
```


### solution.ipynb: original cell 38 (markdown)

## 4.5 Analytical Questions

Opening: `## 4.5 Analytical Questions`
