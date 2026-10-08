# Introduction to Machine Learning — Hamed Batani

I completed Introduction to Machine Learning in the Department of Electrical Engineering at Sharif University of Technology, taught by Dr. Sajad Amini. My final course grade was **18.9/20**. This repository brings together my computational and theoretical coursework and a two-person course project on ECG time-series anomaly detection.

My work connects probabilistic inference and mathematical optimization with practical learning algorithms. I implemented components of Bayesian estimation, decision trees, linear regression, neural networks, boosting, dimensionality reduction, and clustering, and compared models through numerical experiments and written analysis. The ECG project extends this work to one-class learning, hidden-state sequence models, and anomaly detection.

## Start with the project

**[ECG anomaly detection: OC-SVM and Hidden Markov models](projects/ecg-anomaly-detection/)** — a 44-page report and simulation notebook comparing waveform representations and sequence-aware anomaly detection. The project was completed jointly by students 402101339 and 402102079; it is presented here as collaborative work.

## Computational homework

CHW means computational homework. Each folder includes an explanation of my work, a question-by-question guide, the notebook with its saved outputs, and the supplied data or supporting figures available in my archive.

| Assignment | Focus | Main evidence |
|---|---|---|
| [CHW1](computer-homework/chw-01/) | Bayesian updates, Gaussian estimation and sensor fusion, decision trees, conditional independence, statistical language models | Implementations, derivations, plots, missing-token evaluation |
| [CHW2](computer-homework/chw-02/) | First/second-order optimization, line search, Gaussian KL minimization, constrained optimization | Trajectories, convergence experiments, KKT analysis |
| [CHW3](computer-homework/chw-03/) | Linear regression, regularization, LDA/QDA, generative models, heteroskedastic regression, inverse problems | Regression and classification experiments; Gaussian-prior reconstruction |
| [CHW4](computer-homework/chw-04/) | NumPy MLP, PyTorch CNN, kernel SVM, Gaussian processes | Backpropagation, gradient checks, architecture comparisons, robustness and uncertainty experiments |
| [CHW5](computer-homework/chw-05/) | AdaBoost and bagging, PCA, K-means, hierarchical clustering | Two notebooks, ensemble comparisons, variance and clustering analysis |

## Theoretical homework

THW means theoretical homework. These folders distinguish the course-provided question sheets from my handwritten solutions.

| Assignment | Main topics | Available work |
|---|---|---|
| [THW1](theoretical-homework/thw-01/) | Gaussian conditional distributions, sensor fusion, Bayesian decision theory | Question sheet + 23-page solution scan |
| [THW2](theoretical-homework/thw-02/) | Matrix analysis, optimization, convexity, KKT, low-rank approximation | Question sheet + 19-page solution scan |
| [THW3](theoretical-homework/thw-03/) | Logistic and linear regression, generative classifiers, ridge duality | Question sheet; corresponding solution is missing from the supplied archive |
| [THW4](theoretical-homework/thw-04/) | Perceptron convergence, convolution and backpropagation, positive-definite kernels | Question sheet + 14-page solution scan |
| [THW5](theoretical-homework/thw-05/) | SVM, PCA, boosting, Fisher kernels, EM/ELBO | Question sheet + 10-page solution scan |

## Reading and reproduction

GitHub can display the notebooks and their saved plots without executing them. To run an assignment locally, install the packages in `requirements.txt`, open Jupyter from that assignment's folder, and run its cells in order. The package list is an unpinned dependency guide, not a recovered lockfile. Results can vary with versions and random seeds.

The published computational notebooks have local file paths made relative and a short archival note added. Their original calculations and saved outputs have been retained. Unmodified notebook snapshots and alternate versions are preserved in [archive](archive/). No saved result is presented as a newly reproduced result.

The ECG notebook currently depends on a missing `ecg5000_hmad.py` helper module. Other technical limitations, incomplete written responses, and the incorrect duplicate THW3 solution are documented in [AUDIT.md](AUDIT.md). I keep these notes alongside the work so that readers can distinguish available evidence from what still needs completion.

## Attribution

Course question sheets, notebook prompts, provided datasets, and template illustrations are educational materials supplied for the course. My contributions are the submitted solutions, implementations, experiments, analyses, and jointly completed project. Existing assistance disclosures in the notebooks are retained. Dataset source information is recorded in [DATA_SOURCES.md](DATA_SOURCES.md). No blanket license is applied to third-party course material or datasets.
