# CHW5 — Notebook navigation

Cell indices refer to the unmodified source notebook, before the added archival note. This guide maps the available prompts, code, and saved textual outputs; see the README for their interpretation.

### part-1-ensembles.ipynb: original cell 0 (markdown)

Opening: `<img src='sharif.png' alt="SUT logo" width=200 height=200 align=left class="saturate" >`


### part-1-ensembles.ipynb: original cell 1 (markdown)

### Full Name : hamed batani
### Student Number : 402101339

Opening: `### Full Name : hamed batani`


### part-1-ensembles.ipynb: original cell 2 (markdown)

Opening: `<font face="Times New Roman" size=4><div dir=ltr>`


### part-1-ensembles.ipynb: original cell 3 (code)

Opening: `import numpy as np`

Saved execution count: 2. Outputs: 0.


### part-1-ensembles.ipynb: original cell 4 (markdown)

### Data Prepration (10 points)

Opening: `### Data Prepration (10 points)`


### part-1-ensembles.ipynb: original cell 5 (markdown)

Opening: `**What to do here**`


### part-1-ensembles.ipynb: original cell 6 (code)

Opening: `#########################`

Saved execution count: 3. Outputs: 1.

Saved text excerpt:

```text
Train shape: (820, 13), Test shape: (205, 13)
target
 1    421
-1    399
Name: count, dtype: int64

```


### part-1-ensembles.ipynb: original cell 7 (markdown)

### Adaboost Algorithm Implementation (40 points)

Opening: `### Adaboost Algorithm Implementation (40 points)`


### part-1-ensembles.ipynb: original cell 8 (markdown)

Opening: `**What to do here**`


### part-1-ensembles.ipynb: original cell 9 (code)

Opening: `from sklearn.tree import DecisionTreeClassifier`

Saved execution count: 4. Outputs: 0.


### part-1-ensembles.ipynb: original cell 10 (markdown)

### Training and Evaluation (20 points)

Opening: `### Training and Evaluation (20 points)`


### part-1-ensembles.ipynb: original cell 11 (markdown)

Opening: `**What to do here**`


### part-1-ensembles.ipynb: original cell 12 (code)

Opening: `#########################`

Saved execution count: 5. Outputs: 1.

Saved text excerpt:

```text
=== From-scratch AdaBoost ===
Accuracy : 0.8878
Precision: 0.8661
Recall   : 0.9238
F1-score : 0.8940

```


### part-1-ensembles.ipynb: original cell 13 (code)

Opening: `from sklearn.ensemble import AdaBoostClassifier`

Saved execution count: 7. Outputs: 1.

Saved text excerpt:

```text
 Scikit-learn AdaBoost 
Accuracy : 0.8878
Precision: 0.8661
Recall   : 0.9238
F1-score : 0.8940

```


### part-1-ensembles.ipynb: original cell 14 (markdown)

### Early Stopping (15 points)

Opening: `### Early Stopping (15 points)`


### part-1-ensembles.ipynb: original cell 15 (markdown)

Opening: `**What to do here**`


### part-1-ensembles.ipynb: original cell 16 (code)

Opening: `ab = AdaBoost()`

Saved execution count: 8. Outputs: 0.


### part-1-ensembles.ipynb: original cell 17 (code)

Opening: `val_errors = []`

Saved execution count: 10. Outputs: 1.

Saved text excerpt:

```text
<Figure size 800x500 with 1 Axes>
```


### part-1-ensembles.ipynb: original cell 18 (code)

Opening: `best_m = int(np.argmin(val_errors) + 1)`

Saved execution count: 13. Outputs: 1.

Saved text excerpt:

```text
Best number of estimators: 18
Minimum validation error : 0.1024

```


### part-1-ensembles.ipynb: original cell 19 (markdown)

### Weighted Error (10 points)

Opening: `### Weighted Error (10 points)`


### part-1-ensembles.ipynb: original cell 20 (markdown)

Opening: `**What to do here**`


### part-1-ensembles.ipynb: original cell 21 (code)

Opening: `plt.figure(figsize=(8, 5))`

Saved execution count: 15. Outputs: 1.

Saved text excerpt:

```text
<Figure size 800x500 with 1 Axes>
```


### part-1-ensembles.ipynb: original cell 22 (markdown)

### Question : Why does the weighted error tend to increase as the number of estimators increase? (5points)

Opening: `### Question : Why does the weighted error tend to increase as the number of estimators increase? (5points)`


### part-1-ensembles.ipynb: original cell 23 (markdown)

Opening: `**Answer** :`


### part-1-ensembles.ipynb: original cell 24 (markdown)

### Bagging Algorithm Implementation (Bonus Section)

Opening: `___`


### part-1-ensembles.ipynb: original cell 25 (markdown)

Opening: `**What to do here**`


### part-1-ensembles.ipynb: original cell 26 (code)

Opening: `class Bagging:`

Saved execution count: 16. Outputs: 0.


### part-1-ensembles.ipynb: original cell 27 (markdown)

Opening: `**Training and Evaluation**`


### part-1-ensembles.ipynb: original cell 28 (code)

Opening: `#########################`

Saved execution count: 17. Outputs: 1.

Saved text excerpt:

```text
=== From-scratch Bagging ===
Accuracy : 1.0000
Precision: 1.0000
Recall   : 1.0000
F1-score : 1.0000

```


### part-1-ensembles.ipynb: original cell 29 (code)

Opening: `from sklearn.ensemble import BaggingClassifier`

Saved execution count: 18. Outputs: 1.

Saved text excerpt:

```text
=== Scikit-learn Bagging ===
Accuracy : 1.0000
Precision: 1.0000
Recall   : 1.0000
F1-score : 1.0000

```


### part-1-ensembles.ipynb: original cell 30 (markdown)

Opening: `**Bagging vs. AdaBoost — number of estimators**`


### part-1-ensembles.ipynb: original cell 31 (code)

Opening: `B_max = 100`

Saved execution count: 20. Outputs: 1.

Saved text excerpt:

```text
Bagging  - best B: 34, min error: 0.0000
AdaBoost - best M: 18, min error: 0.1024

```


### part-1-ensembles.ipynb: original cell 32 (markdown)

Opening: `**Discussion.** Bagging mainly attacks the **variance** term of the bias-variance decomposition by averaging many independent, low-bias/high-variance trees — this is why letting each tree grow to full depth (unlike AdaBo`


### part-1-ensembles.ipynb: original cell 33 (markdown)

## Grading Rubric & Score

Opening: `___`


### part-1-ensembles.ipynb: original cell 34 (markdown)

Opening: `| Section | Points | What full marks require |`


### part-1-ensembles.ipynb: original cell 35 (markdown)

## Review Questions
### 1. Why must the weak learner accept a `sample_weight` argument rather than being retrained on a re-sampled dataset each round?
### 2. Why does alpha_m become negative when err_m > 0.5, and why is that a problem?
### 3. Discrete AdaBoost vs. Real AdaBoost — practical difference and when to prefer each
### 4. Why does AdaBoost use shallow stumps while Bagging/Random Forests use deep trees, in terms of bias-variance decomposition?
### 5. Why does Bagging's variance-reduction benefit shrink when trees are highly correlated, and how does Random Forest address this?

Opening: `## Review Questions`


### part-2-pca-clustering.ipynb: original cell 0 (markdown)

Opening: `<img src='sharif.png' alt="SUT logo" width=200 height=200 align=left class="saturate" >`


### part-2-pca-clustering.ipynb: original cell 1 (markdown)

### Full Name :
### Student Number :

Opening: `### Full Name :`


### part-2-pca-clustering.ipynb: original cell 2 (code)

Opening: `#import libraries`

Saved execution count: 2. Outputs: 0.


### part-2-pca-clustering.ipynb: original cell 3 (markdown)

Opening: `<font color=red size=3>`


### part-2-pca-clustering.ipynb: original cell 4 (markdown)

## Overview

Opening: `## Overview`


### part-2-pca-clustering.ipynb: original cell 5 (markdown)

## Data Preprocessing (15 points)

Opening: `## Data Preprocessing (15 points)`


### part-2-pca-clustering.ipynb: original cell 6 (code)

Opening: `df = pd.read_csv("dataset.csv")`

Saved execution count: 3. Outputs: 1.

Saved text excerpt:

```text
  CUST_ID      BALANCE  BALANCE_FREQUENCY  PURCHASES  ONEOFF_PURCHASES  \
0  C10001    40.900749           0.818182      95.40              0.00   
1  C10002  3202.467416           0.909091       0.00              0.00   
2  C10003  2495.148862           1.000000     773.17            773.17   
3  C10004  1666.670542           0.636364    1499.00           1499.00   
4  C10005   817.714335           1.000000      16.00             16.00   

   INSTALLMENTS_PURCHASES  CASH_ADVANCE  PURCHASES_FREQUENCY  \
0                    95.4      0.000000             0.166667   
1                     0.0   6442.945483             0.000000   
2                     0.0      0.000000             1.000000   
3                     0.0    205.788017             0.083333   
4                     0.0      0.000000             0.083333   

   ONEOFF_PURCHASES_FREQUENCY  PURCHASES_INSTALLMENTS_FREQUENCY  \
0  
```


### part-2-pca-clustering.ipynb: original cell 7 (markdown)

Opening: `Display dataset information.`


### part-2-pca-clustering.ipynb: original cell 8 (code)

Opening: `df.info()`

Saved execution count: 4. Outputs: 2.

Saved text excerpt:

```text
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 8950 entries, 0 to 8949
Data columns (total 18 columns):
 #   Column                            Non-Null Count  Dtype  
---  ------                            --------------  -----  
 0   CUST_ID                           8950 non-null   object 
 1   BALANCE                           8950 non-null   float64
 2   BALANCE_FREQUENCY                 8950 non-null   float64
 3   PURCHASES                         8950 non-null   float64
 4   ONEOFF_PURCHASES                  8950 non-null   float64
 5   INSTALLMENTS_PURCHASES            8950 non-null   float64
 6   CASH_ADVANCE                      8950 non-null   float64
 7   PURCHASES_FREQUENCY               8950 non-null   float64
 8   ONEOFF_PURCHASES_FREQUENCY        8950 non-null   float64
 9   PURCHASES_INSTALLMENTS_FREQUENCY  8950 non-null   float64
 10  CASH_ADVANCE_FREQUENCY          
```


### part-2-pca-clustering.ipynb: original cell 9 (markdown)

Opening: `Which column do you think might be the most irrelevant for PCA and clustering?`


### part-2-pca-clustering.ipynb: original cell 10 (code)

Opening: `# Exclude irrelevant feature`

Saved execution count: 5. Outputs: 0.


### part-2-pca-clustering.ipynb: original cell 11 (markdown)

Opening: `how do you handle missing data, and why did you choose this method?`


### part-2-pca-clustering.ipynb: original cell 12 (code)

Opening: `#Fill missing data`

Saved execution count: 6. Outputs: 0.


### part-2-pca-clustering.ipynb: original cell 13 (markdown)

Opening: `plot the correlation matrix and identify redundant features.remove them from the dataframe.`


### part-2-pca-clustering.ipynb: original cell 14 (code)

Opening: `# Plot the correlation matrix`

Saved execution count: 7. Outputs: 1.

Saved text excerpt:

```text
<Figure size 1400x1200 with 2 Axes>
```


### part-2-pca-clustering.ipynb: original cell 15 (code)

Opening: `# Identify and remove redundant features. use 0.8 threshold.`

Saved execution count: 8. Outputs: 1.

Saved text excerpt:

```text
Redundant features to drop: ['ONEOFF_PURCHASES', 'PURCHASES_INSTALLMENTS_FREQUENCY']
(8950, 15)

```


### part-2-pca-clustering.ipynb: original cell 16 (markdown)

## Standardize the Data (5 points)

Opening: `## Standardize the Data (5 points)`


### part-2-pca-clustering.ipynb: original cell 17 (code)

Opening: `# todo`

Saved execution count: 9. Outputs: 1.

Saved text excerpt:

```text
    BALANCE  BALANCE_FREQUENCY  PURCHASES  INSTALLMENTS_PURCHASES  \
0 -0.731989          -0.249434  -0.424900               -0.349079   
1  0.786961           0.134325  -0.469552               -0.454576   
2  0.447135           0.518084  -0.107668               -0.454576   
3  0.049099          -1.016953   0.232058               -0.454576   
4 -0.358775           0.518084  -0.462063               -0.454576   

   CASH_ADVANCE  PURCHASES_FREQUENCY  ONEOFF_PURCHASES_FREQUENCY  \
0     -0.466786            -0.806490                   -0.678661   
1      2.605605            -1.221758                   -0.678661   
2     -0.466786             1.269843                    2.673451   
3     -0.368653            -1.014125                   -0.399319   
4     -0.466786            -1.014125                   -0.399319   

   CASH_ADVANCE_FREQUENCY  CASH_ADVANCE_TRX  PURCHASES_TRX  CREDIT_LIMIT  \

```


### part-2-pca-clustering.ipynb: original cell 18 (markdown)

Opening: `Why is it important to standardize the data before applying PCA?`


### part-2-pca-clustering.ipynb: original cell 19 (markdown)

Opening: `What is differnce between Normalizer and StandardScaler classes. which is better for PCA?`


### part-2-pca-clustering.ipynb: original cell 20 (markdown)

## Principal Component Analysis (PCA) (35 points)

Opening: `## Principal Component Analysis (PCA) (35 points)`


### part-2-pca-clustering.ipynb: original cell 21 (code)

Opening: `import numpy as np`

Saved execution count: 10. Outputs: 0.


### part-2-pca-clustering.ipynb: original cell 22 (markdown)

### Visualizing the Cumulative Variance

Opening: `### Visualizing the Cumulative Variance`


### part-2-pca-clustering.ipynb: original cell 23 (code)

Opening: `pca_full = CustomPCA(n_components=df_scaled.shape[1])`

Saved execution count: 11. Outputs: 2.

Saved text excerpt:

```text
<Figure size 1000x600 with 1 Axes>
Number of components needed for 75% variance: 6
Cumulative variance ratios: [0.2541083  0.47661703 0.56375628 0.63899948 0.70469992 0.76058004
 0.8140162  0.85745353 0.89487545 0.92550348 0.94569795 0.96250476
 0.97837154 0.99000092 1.        ]

```


### part-2-pca-clustering.ipynb: original cell 24 (markdown)

Opening: `Build a new DataFrame with the first slected components. save it to a new CSV file named 'pca_output.csv'`


### part-2-pca-clustering.ipynb: original cell 25 (code)

Opening: `#Build a new DataFrame with the first slected components`

Saved execution count: 13. Outputs: 1.

Saved text excerpt:

```text
        PC1       PC2       PC3       PC4       PC5       PC6
0  1.731242  0.824084 -0.384320 -0.451623 -0.087766  0.438057
1  0.301398 -2.533638  0.621582 -0.939313 -0.794456  0.060615
2 -1.194199  0.887568 -1.184455  1.129115 -1.152626 -1.869029
3  0.930140  0.030106 -0.111213 -1.309452 -0.505452 -0.834667
4  1.499511  0.517780 -0.794300 -0.125376 -0.253049  0.326998
```


### part-2-pca-clustering.ipynb: original cell 26 (markdown)

Opening: `We expect these new features to be orthogonal to each other. Check this and show the correlation between the features.`


### part-2-pca-clustering.ipynb: original cell 27 (code)

Opening: `# todo`

Saved execution count: 14. Outputs: 2.

Saved text excerpt:

```text
              PC1           PC2           PC3           PC4           PC5  \
PC1  1.000000e+00 -1.162981e-16 -3.262809e-16 -1.895886e-17  6.271043e-17   
PC2 -1.162981e-16  1.000000e+00 -1.170345e-16  1.694715e-16  1.900074e-17   
PC3 -3.262809e-16 -1.170345e-16  1.000000e+00 -8.782405e-16 -2.272486e-16   
PC4 -1.895886e-17  1.694715e-16 -8.782405e-16  1.000000e+00 -1.379438e-16   
PC5  6.271043e-17  1.900074e-17 -2.272486e-16 -1.379438e-16  1.000000e+00   
PC6  3.224728e-16 -2.889582e-16 -2.134155e-16  4.275015e-17 -1.124632e-16   

              PC6  
PC1  3.224728e-16  
PC2 -2.889582e-16  
PC3 -2.134155e-16  
PC4  4.275015e-17  
PC5 -1.124632e-16  
PC6  1.000000e+00  

<Figure size 800x600 with 2 Axes>
```


### part-2-pca-clustering.ipynb: original cell 28 (markdown)

## KMeans (45 points)

Opening: `## KMeans (45 points)`


### part-2-pca-clustering.ipynb: original cell 29 (code)

Opening: `import numpy as np`

Saved execution count: 15. Outputs: 0.


### part-2-pca-clustering.ipynb: original cell 30 (markdown)

### Elbow Method

Opening: `### Elbow Method`


### part-2-pca-clustering.ipynb: original cell 31 (code)

Opening: `# Initialize an empty list to store the WCSS values for each number of clusters`

Saved execution count: 16. Outputs: 0.


### part-2-pca-clustering.ipynb: original cell 32 (code)

Opening: `# Plot the Elbow curve using Matplotlib`

Saved execution count: 17. Outputs: 1.

Saved text excerpt:

```text
<Figure size 1000x600 with 1 Axes>
```


### part-2-pca-clustering.ipynb: original cell 33 (markdown)

Opening: `Apply the optimal KMeans clustering on the PCA-transformed data, and assign cluster labels to each observation. Add a new column named segment to the df_pca DataFrame to store these labels.`


### part-2-pca-clustering.ipynb: original cell 34 (code)

Opening: `# Apply KMeans on PCA-reduced data with the optimal number of clusters based on the elbow method`

Saved execution count: 18. Outputs: 1.

Saved text excerpt:

```text
<__main__.CustomKMeans at 0x20a56a87da0>
```


### part-2-pca-clustering.ipynb: original cell 35 (code)

Opening: `# Add a new column 'segment' to pca data frame and assign the cluster labels to each observation`

Saved execution count: 19. Outputs: 1.

Saved text excerpt:

```text
        PC1       PC2       PC3       PC4       PC5       PC6  segment
0  1.731242  0.824084 -0.384320 -0.451623 -0.087766  0.438057        5
1  0.301398 -2.533638  0.621582 -0.939313 -0.794456  0.060615        1
2 -1.194199  0.887568 -1.184455  1.129115 -1.152626 -1.869029        8
3  0.930140  0.030106 -0.111213 -1.309452 -0.505452 -0.834667        5
4  1.499511  0.517780 -0.794300 -0.125376 -0.253049  0.326998        5
```


### part-2-pca-clustering.ipynb: original cell 36 (markdown)

Opening: `visualize the clustering by plotting the pairwise relationships of the PCA-reduced features, color-coded by the cluster assignments.`


### part-2-pca-clustering.ipynb: original cell 37 (code)

Opening: `# todo`

Saved execution count: 20. Outputs: 1.

Saved text excerpt:

```text
<Figure size 1564.36x1500 with 42 Axes>
```


### part-2-pca-clustering.ipynb: original cell 38 (markdown)

Opening: `So, when we employ PCA prior to using K-means we can visually separate almost the entire data set. That was one of the biggest goals of PCA - to reduce the number of variables by combining them into bigger, more meaningf`


### part-2-pca-clustering.ipynb: original cell 39 (markdown)

### Hierarchical Clustering

Opening: `### Hierarchical Clustering`


### part-2-pca-clustering.ipynb: original cell 40 (code)

Opening: `# Perform Hierarchical Clustering on the pca dataset`

Saved execution count: 21. Outputs: 1.

Saved text excerpt:

```text
<Figure size 1400x700 with 1 Axes>
```


### part-2-pca-clustering.ipynb: original cell 41 (markdown)

Opening: `"Use scipy.cluster.hierarchy.fcluster to assign clusters from the dendrogram with a specified number of 5 clusters. Then visualize the results using pairplots.`


### part-2-pca-clustering.ipynb: original cell 42 (code)

Opening: `# Choose threshold and assign clusters`

Saved execution count: 22. Outputs: 1.

Saved text excerpt:

```text
<Figure size 1595.36x1500 with 42 Axes>
```
