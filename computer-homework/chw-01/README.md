# CHW1 — Bayesian Estimation, Sensor Fusion, and Statistical Learning

I explored how probabilistic models turn observations into estimates and predictions. My notebook implements sequential Bayesian updates, Gaussian missing-value estimation, entropy-based decision trees, precision-weighted sensor fusion, conditional-independence tests, and count-based missing-token prediction.

| Question | What I implemented or analyzed | Evidence to inspect |
|---|---|---|
| 1.1: Beta–Bernoulli updating | Sequentially update Beta parameters from binary observations and plot changing densities and CDFs | Prior/posterior curves and update code |
| 1.2 | The assignment explicitly deletes this question | Embedded prompt; not an omitted solution |
| 1.3: ML versus MAP for a discrete variable | Count dice outcomes, numerically update probabilities with renormalization, and compare likelihood and prior-informed estimates | Estimated probabilities, objective code, prior-strength experiment |
| 1.4: Multivariate Gaussian estimation | Estimate Gaussian statistics from increasing amounts of training data; condition on observed coordinates to impute missing test entries | MSE versus sample count and Hinton diagrams |
| 1.5: Decision tree | Implement entropy, information gain, threshold search, and recursive tree nodes for animal-species classification | Printed tree, confusion matrix, 2D surfaces, 3D feature visualization |
| 1.6: Linear Gaussian sensor fusion | Estimate sensor means/covariances and combine Gaussian information; compare fusion order and omission of individual sensors | Covariance ellipses, fusion progression, uncertainty plots |
| Part 2: Bayesian network | Discretize stock variables, implement chi-square conditional-independence tests, and construct a candidate dependency graph | Statistical tests and graph visualization; causal orientation is not validated against a ground-truth causal system |
| Part 3: Missing-token prediction | Compare bigram, trigram, and surrounding-word frequency models, including sparse-context behavior | Saved accuracies: 23.0%, 18.2%, and 29.6%, respectively |

The assignment's “MiniGPT” name refers here to statistical language modeling; my implementation is not a GPT architecture or deep language model. The surrounding-word comparison illustrates why right-hand context helps a fill-in-the-blank task and why longer contexts can suffer from sparse counts.

The notebook's seven code cells have saved execution counts and no saved error outputs. This is archival evidence, not confirmation of a fresh run. One sensor-fusion prose answer ends mid-sentence, and the discrete ML/MAP update uses renormalization rather than an exact simplex projection; these are recorded in the audit.


## Files and use

[solution.ipynb](solution.ipynb) | [Cell-by-cell guide](CELL_GUIDE.md) | [Archive audit](../../AUDIT.md)

Open Jupyter in this folder so relative paths resolve. The notebook includes course-provided prompts as well as my solutions; assignment wording is not claimed as my authorship. Saved outputs are retained from the source archive.
