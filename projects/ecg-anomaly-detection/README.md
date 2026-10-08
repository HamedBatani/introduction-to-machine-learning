# ECG Time-Series Anomaly Detection with OC-SVM and Hidden Markov Models

I co-developed this two-person Introduction to Machine Learning course project with student 402102079. We investigated one-class anomaly detection for heartbeat sequences, comparing feature-based OC-SVM baselines with a simplified Hidden Markov anomaly-detection (HMAD) model. The project combines optimization theory, probabilistic sequence modeling, numerical inference, and experimental comparison.

**Course grade:** 18.9/20 overall; no separate project grade is asserted. **Team:** students 402101339 (Hamed Batani) and 402102079, as credited in the report. The available files do not specify a precise division of individual tasks, so I describe the project as joint work.

[44-page report](report.pdf) | [Simulation notebook and saved outputs](simulation.ipynb) | [Course-provided project brief](project-brief.pdf)

## Research question

A one-class classifier trained on normal examples can score unusual sequences, but its behavior depends on the representation of temporal structure. We examined whether a sequence-aware model captures information beyond simple summary statistics, and how this comparison changes when the full waveform is used as an OC-SVM feature vector.

## Mathematical and computational work

- **One-class SVM:** study its primal/dual formulation, the role of `nu`, support vectors, and the distinction between a score and a thresholded decision.
- **Representations:** compare flattened 140-sample waveforms, five summary features, and 20 window-based features.
- **Markov and HMM structure:** work with initial-state, transition, and emission probabilities; generate synthetic sequences and score their likelihoods.
- **Stable inference:** implement or examine log-domain Viterbi decoding, demonstrate ordinary-probability underflow on long sequences, and recover hidden paths in synthetic data.
- **HMAD:** study a simplified alternating latent-state/one-class procedure using joint emission/transition information; monitor state changes and convergence behavior.
- **Controlled examples:** compare ordered and shuffled sequences with similar marginal observations to expose the information carried by temporal transitions.
- **Evaluation:** compare ROC-AUC, precision, recall, F1, runtime, and behavior as anomaly fractions change; include a trivial-state baseline.

## Notebook navigation

| Original cells | Experiment | What to inspect |
|---|---|---|
| 2, 4, 6 | OC-SVM baseline, feature comparison, and `nu` sensitivity | Data setup, representation dependence, metric tables |
| 8–11 | Markov likelihood, HMM generation, Viterbi, and underflow | Sequence probabilities and log-space inference |
| 13–14 | Temporal-order and synthetic anomaly experiments | Why identical marginal structure can conceal different transitions |
| 15–16 | HMAD fitting/convergence and prediction | Alternation history, state changes, sequence scores |
| 18 | Inline `HMADClassifier` demonstration | Self-contained educational class; not a verified substitute for the missing helper used elsewhere |
| 20–23 | Dataset verification, preprocessing/runtime, final comparisons | Official split counts, saved results, ROC curves, feature comparison |

The report contains the theoretical responses and interpretation of these experiments. Numbered questions and constraints come from the course-provided brief; our derivations, code, experiments, and report are the submitted project work.

## Dataset and evaluation protocol

We used the ECG5000 archive documented in the supplied dataset README. Each sequence has 140 time steps. The saved verification identifies 500 training examples and 4,500 test examples. Class 1 is treated as normal; classes 2–5 are grouped as anomalous. One-class fitting uses the **292 normal training examples**. The test set contains 2,627 normal and 1,873 anomalous examples.

The recorded protocol fits feature scaling on normal training data and evaluates on the official test split. Anomaly-fraction experiments use constructed cohorts and should be distinguished from results on the complete official test set. ECG5000 is a benchmark derived from a single source record; these experiments do not establish clinical generalization across patients.

## Results recorded in the submitted notebook

These values are **saved historical outputs**, not results freshly rerun during repository preparation.

| Model/representation | ROC-AUC | Precision | Recall | F1 |
|---|---:|---:|---:|---:|
| OC-SVM, flattened waveform | 0.9840 | 0.8314 | 0.9979 | 0.9071 |
| OC-SVM, summary features | 0.9518 | 0.8124 | 0.9274 | 0.8661 |
| OC-SVM, window features | 0.9823 | 0.8319 | 0.9984 | 0.9075 |
| Simplified HMAD | 0.9577 | 0.8419 | 0.9466 | 0.8912 |

The best OC-SVM baseline has higher ROC-AUC and F1 than HMAD in this run. HMAD improves over the summary-feature baseline, but that does not establish superiority over waveform-based OC-SVM. This comparison emphasizes the importance of strong baselines and representation choices when evaluating a more structured model.

## Reproduction status

**The imported helper `ecg5000_hmad.py` is missing from the supplied archive.** Most ECG benchmark cells depend on it, so the repository currently provides an inspectable report/notebook archive rather than a complete executable project. The notebook's inline HMAD class has not been substituted for the missing implementation. Model definitions, feature extraction, preprocessing, and scoring must be recovered from the original helper before exact reproduction can be claimed.

The TRAIN/TEST text data and the original dataset source note are included under `data/ECG5000/`. The source archive also contains equivalent `.arff`/`.ts` exports and a dataset ZIP; these redundant formats were not duplicated here. Once the helper is recovered, place it beside `simulation.ipynb`, start Jupyter from this folder, and verify a clean run using a documented environment. The notebook's initial installation cell is historical; install dependencies explicitly in an isolated environment before running.

## Attribution

The project brief is course-provided material. The report and simulation are joint course submissions. Dataset provenance is retained in [the source note](data/ECG5000/README.md); benchmark data are not our original collection. This is an educational machine-learning project, not a deployed medical detector.
