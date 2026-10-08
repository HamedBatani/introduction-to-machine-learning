# CHW5 — Ensemble Learning, Dimensionality Reduction, and Clustering

I implemented and compared supervised ensembles and unsupervised representations in two notebooks. The first develops AdaBoost's weighted learning procedure and adds bagging; the second explores how preprocessing and PCA affect clustering structure.

### Part 1 — AdaBoost and bagging

| Section | My implementation | Evidence |
|---|---|---|
| Data preparation | Load the supplied heart-disease benchmark, map labels to −1/+1, and form a stratified 80/20 split | Shapes and class counts |
| AdaBoost | Implement weighted error, vote weights, exponential sample reweighting, ensemble fitting, and prediction | Custom algorithm; decision-stump fitting uses scikit-learn |
| Reference comparison | Compare the custom ensemble with scikit-learn AdaBoost using classification metrics | Saved accuracy 0.8878 and F1 0.8940 for both in the displayed run |
| Early stopping | Evaluate truncated ensembles across estimator counts | Error curve; selection uses the test split, so it is exploratory rather than unbiased test evaluation |
| Weighted error | Track weak-learner weighted errors and explain concentration on difficult examples | Plot and written analysis |
| Bagging extension | Bootstrap samples, train an ensemble, aggregate predictions, and compare with reference ensembles | Implementation and metric comparisons |

The custom AdaBoost implementation uses scikit-learn trees as base learners; “from scratch” refers to the boosting procedure, not the tree algorithm. The original notebook contains an authored grading rubric claiming 100/100. This is a self-assessment rather than a verified instructor grade and is labeled accordingly in the displayed version.

### Part 2 — PCA and clustering

| Section | My work | Evidence |
|---|---|---|
| Preprocessing | Remove `CUST_ID`, impute missing values, inspect correlations, and remove highly correlated features using a 0.8 threshold | Tables and correlation matrix |
| Standardization | Scale the features before covariance-based dimension reduction | Standardized array and statistics |
| PCA | Implement covariance eigendecomposition, order components, inspect cumulative explained variance, and project observations | Variance curve, projected data, PCA correlation plot |
| K-means | Implement centroid initialization/update and assignment; examine within-cluster sums of squares across candidate counts | Elbow plot and cluster visualization |
| Hierarchical clustering | Apply complete-linkage clustering and inspect a dendrogram | Threshold-based labels and paired component plots |

Some preprocessing explanation fields and the name/student-number fields in Part 2 are blank, although corresponding code and outputs are present. The notebooks do not establish real-world customer-segmentation validity. Exact duplicate copies found in the original `IML_CHW5` directory have been consolidated; its supporting datasets and logo are retained beside the two notebooks. Supplied exports and plots are in `csv/` and `Plots/`.


## Files and use

[part-1-ensembles.ipynb](part-1-ensembles.ipynb) | [part-2-pca-clustering.ipynb](part-2-pca-clustering.ipynb) | [Cell-by-cell guide](CELL_GUIDE.md) | [Archive audit](../../AUDIT.md)

Open Jupyter in this folder so relative paths resolve. The notebook includes course-provided prompts as well as my solutions; assignment wording is not claimed as my authorship. Saved outputs are retained from the source archive.
