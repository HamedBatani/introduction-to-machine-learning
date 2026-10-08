# Archive audit and reproduction notes

This audit records the supplied archive as of 9 October 2026. It is a file, code, and saved-output review; it is not an official grading report or a proof that every derivation is correct. Original Desktop files were left unchanged.

## Missing or incorrectly filed material

1. **THW3 solution missing.** The file in `HW/THW/HW3/ML_THW5_402101339.PDF` is byte-identical to the real THW5 solution. It is retained once under THW5, not represented as a THW3 submission.
2. **ECG project helper missing.** The simulation imports `ecg5000_hmad.py`, but the module is absent from the supplied ML directory. Consequently, the main ECG experiments cannot currently be executed end to end from this repository. The inline `HMADClassifier` demonstration is not treated as an interchangeable replacement for the missing helper. The report, notebook, and saved results remain available.
3. **Original environment unspecified.** There is no complete environment lockfile. Dependencies are inferred from imports, not claimed to reproduce the original runtime exactly.
4. **Separate CHW question sheets.** CHW prompts are embedded in the notebooks. Separate original templates exist for CHW3 and CHW4; corresponding standalone templates were not found for CHW1, CHW2, or CHW5. This does not mean their embedded prompts are absent.

## Findings that affect interpretation

| Work | Finding | Treatment |
|---|---|---|
| CHW1, Problem 1.2 | Assignment explicitly says the problem was deleted | Not counted as missing work |
| CHW1, Gaussian fusion written response | One response ends mid-sentence | Retained; written explanation needs completion |
| CHW1, discrete ML/MAP | Renormalized gradient updates are used; normalization is not an exact Euclidean simplex projection | Described as the submitted numerical implementation; no guarantee of an exact constrained optimum |
| CHW1, “MiniGPT” | Implementation uses count-based context models, not a transformer | Described as statistical missing-token prediction |
| CHW2, penalty experiment | Saved iterate near (0.1771, 1.2141) does not satisfy the equality constraint or reach the analytic (1,1) solution | Preserved as a nonconverged experiment, not successful constrained optimization |
| CHW3, Problem 3.3 | Reconstructed new measurements are compared against the first historical signals rather than supplied `X_true_batch.csv` | The saved MSE 0.9046 and associated “Original” plots are not valid reconstruction accuracy evidence; evaluation needs correction and rerunning |
| CHW3 alternate `final` notebook | Saved ValueErrors from incompatible array shapes, and unexecuted cells | Kept as an alternate snapshot, not the main displayed notebook |
| CHW5, boosting early stopping | Estimator count is selected using `X_test`/`y_test`; no separate validation split is used there | Selected error is exploratory, not an unbiased held-out test estimate |
| CHW5, Part 2 | Full-name/student-number fields and some written preprocessing answers are blank | Code and outputs retained; written answers need completion |
| CHW5, Part 1 | A notebook-authored “100/100” rubric statement is not evidence of an instructor-assigned grade | Original retained in archive; displayed copy labels this as a self-assessment, not an official grade |
| ECG project | Best saved baseline ROC-AUC exceeds simplified HMAD ROC-AUC | No claim that HMAD outperformed the best OC-SVM baseline |
| Scanned THW solutions | Handwritten scans, variable legibility; no official grading annotations verified | Page counts and question coverage are documented; mathematical correctness/completeness is not certified |

## Publication changes and provenance

- Added English explanations and question/experiment maps outside the submitted files.
- Preserved source PDFs without modification.
- Copied main notebooks with an archival note and relative input/output paths. Saved execution counts and outputs remain historical; no fresh notebook execution is claimed.
- Left numerical methods and substantive answers unchanged rather than silently rewriting a submission.
- Consolidated exact duplicate CHW5 notebooks and the misplaced THW5 scan.
- Kept CHW3 variants and CHW4 original template in `archive/alternate-notebooks.zip`.
- Preserved original main notebooks in `archive/original-notebooks.zip`.
- Published ECG TRAIN/TEST text files needed by the notebook; redundant `.arff`, `.ts`, and original dataset ZIP remain in the source archive and are listed in the inventory.
- Excluded macOS resource-fork files and `.DS_Store` metadata.

`source-inventory.json` records source paths, byte counts, and SHA-256 hashes. `publication-manifest.json` maps copied/adapted files to their originals. These records establish file provenance; they do not establish authorship or official grades.
