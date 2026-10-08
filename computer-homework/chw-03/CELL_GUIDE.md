# CHW3 — Notebook navigation

Cell indices refer to the unmodified source notebook, before the added archival note. This guide maps the available prompts, code, and saved textual outputs; see the README for their interpretation.

### solution.ipynb: original cell 0 (markdown)

Opening: `<font face="Times New Roman" size=5>`


### solution.ipynb: original cell 1 (markdown)

Opening: `> - Full Name: **[Full Name]**`


### solution.ipynb: original cell 2 (markdown)

# Problem 1: Linear Regression

Opening: `# Problem 1: Linear Regression`


### solution.ipynb: original cell 3 (markdown)

### Importing needed libraries

Opening: `### Importing needed libraries`


### solution.ipynb: original cell 4 (code)

Opening: `import numpy as np`

Saved execution count: 15. Outputs: 0.


### solution.ipynb: original cell 5 (markdown)

### Loading our housing dataset

Opening: `### Loading our housing dataset`


### solution.ipynb: original cell 6 (code)

Opening: `dataset = pd.read_csv(r'C:\Users\Asus\OneDrive\Desktop\EE_Archive\6th_semester\MachineLearning\CHW\HW3\kc_house_data.csv')`

Saved execution count: 16. Outputs: 0.


### solution.ipynb: original cell 7 (markdown)

### Data Analysis

Opening: `### Data Analysis`


### solution.ipynb: original cell 8 (markdown)

Opening: `using pandas .info() we see we have 18 columns and 21613 records. Pretty much all the features given are already in numeric format.`


### solution.ipynb: original cell 9 (code)

Opening: `X.info()`

Saved execution count: 17. Outputs: 1.

Saved text excerpt:

```text
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 21613 entries, 0 to 21612
Data columns (total 18 columns):
 #   Column         Non-Null Count  Dtype  
---  ------         --------------  -----  
 0   bedrooms       21613 non-null  int64  
 1   bathrooms      21613 non-null  float64
 2   sqft_living    21613 non-null  int64  
 3   sqft_lot       21613 non-null  int64  
 4   floors         21613 non-null  float64
 5   waterfront     21613 non-null  int64  
 6   view           21613 non-null  int64  
 7   condition      21613 non-null  int64  
 8   grade          21613 non-null  int64  
 9   sqft_above     21613 non-null  int64  
 10  sqft_basement  21613 non-null  int64  
 11  yr_built       21613 non-null  int64  
 12  yr_renovated   21613 non-null  int64  
 13  zipcode        21613 non-null  int64  
 14  lat            21613 non-null  float64
 15  long           21613 non-null  float64
```


### solution.ipynb: original cell 10 (code)

Opening: `columns = X.columns`

Saved execution count: 18. Outputs: 1.

Saved text excerpt:

```text
Index(['bedrooms', 'bathrooms', 'sqft_living', 'sqft_lot', 'floors',
       'waterfront', 'view', 'condition', 'grade', 'sqft_above',
       'sqft_basement', 'yr_built', 'yr_renovated', 'zipcode', 'lat', 'long',
       'sqft_living15', 'sqft_lot15'],
      dtype='object')
```


### solution.ipynb: original cell 11 (code)

Opening: `#show first 5 records`

Saved execution count: 19. Outputs: 1.

Saved text excerpt:

```text
   bedrooms  bathrooms  sqft_living  sqft_lot  floors  waterfront  view  \
0         3       1.00         1180      5650     1.0           0     0   
1         3       2.25         2570      7242     2.0           0     0   
2         2       1.00          770     10000     1.0           0     0   
3         4       3.00         1960      5000     1.0           0     0   
4         3       2.00         1680      8080     1.0           0     0   

   condition  grade  sqft_above  sqft_basement  yr_built  yr_renovated  \
0          3      7        1180              0      1955             0   
1          3      7        2170            400      1951          1991   
2          3      6         770              0      1933             0   
3          5      7        1050            910      1965             0   
4          3      8        1680              0      1987             0   

   z
```


### solution.ipynb: original cell 12 (markdown)

Opening: `.describe generates descriptive statistics that summarize the central tendency, dispersion and shape of a dataset's distribution, excluding NaN values.`


### solution.ipynb: original cell 13 (code)

Opening: `X.describe()`

Saved execution count: 20. Outputs: 1.

Saved text excerpt:

```text
           bedrooms     bathrooms   sqft_living      sqft_lot        floors  \
count  21613.000000  21613.000000  21613.000000  2.161300e+04  21613.000000   
mean       3.370842      2.114757   2079.899736  1.510697e+04      1.494309   
std        0.930062      0.770163    918.440897  4.142051e+04      0.539989   
min        0.000000      0.000000    290.000000  5.200000e+02      1.000000   
25%        3.000000      1.750000   1427.000000  5.040000e+03      1.000000   
50%        3.000000      2.250000   1910.000000  7.618000e+03      1.500000   
75%        4.000000      2.500000   2550.000000  1.068800e+04      2.000000   
max       33.000000      8.000000  13540.000000  1.651359e+06      3.500000   

         waterfront          view     condition         grade    sqft_above  \
count  21613.000000  21613.000000  21613.000000  21613.000000  21613.000000   
mean       0.007542      0.234
```


### solution.ipynb: original cell 14 (markdown)

Opening: `We can alse compute correlation between variables and our predictor variable.`


### solution.ipynb: original cell 15 (code)

Opening: `dataset = dataset.drop(['id', 'date'], axis=1)`

Saved execution count: 21. Outputs: 1.

Saved text excerpt:

```text
                  price  bedrooms  bathrooms  sqft_living  sqft_lot    floors  \
price          1.000000  0.308350   0.525138     0.702035  0.089661  0.256794   
bedrooms       0.308350  1.000000   0.515884     0.576671  0.031703  0.175429   
bathrooms      0.525138  0.515884   1.000000     0.754665  0.087740  0.500653   
sqft_living    0.702035  0.576671   0.754665     1.000000  0.172826  0.353949   
sqft_lot       0.089661  0.031703   0.087740     0.172826  1.000000 -0.005201   
floors         0.256794  0.175429   0.500653     0.353949 -0.005201  1.000000   
waterfront     0.266369 -0.006582   0.063744     0.103818  0.021604  0.023698   
view           0.397293  0.079532   0.187737     0.284611  0.074710  0.029444   
condition      0.036362  0.028472  -0.124982    -0.058753 -0.008958 -0.263768   
grade          0.667434  0.356967   0.664983     0.762704  0.113621  0.458183   
sqft_abov
```


### solution.ipynb: original cell 16 (markdown)

Opening: `for gaining better insight, we can visualize the table above.`


### solution.ipynb: original cell 17 (code)

Opening: `plt.subplots(figsize=(5,4))`

Saved execution count: 22. Outputs: 1.

Saved text excerpt:

```text
<Axes: >
```


### solution.ipynb: original cell 18 (markdown)

Opening: `Now that we have gained some insight about our dataset, we can implement linear regression.`


### solution.ipynb: original cell 19 (markdown)

## 1.1  Simple Linear Regression

Opening: `## 1.1  Simple Linear Regression`


### solution.ipynb: original cell 20 (code)

Opening: `x = X[['sqft_living']]`

Saved execution count: 23. Outputs: 0.


### solution.ipynb: original cell 21 (code)

Opening: `plt.figure(figsize=(10, 6))`

Saved execution count: 24. Outputs: 2.

Saved text excerpt:

```text
<Figure size 500x400 with 2 Axes>
<Figure size 1000x600 with 1 Axes>
```


### solution.ipynb: original cell 22 (markdown)

###  Gradient Descent Implementation

Opening: `###  Gradient Descent Implementation`


### solution.ipynb: original cell 23 (markdown)

Opening: `complete the TODO parts to implement linear regression.`


### solution.ipynb: original cell 24 (code)

Opening: `# do not change this cell`

Saved execution count: 25. Outputs: 0.


### solution.ipynb: original cell 25 (markdown)

Opening: `(empty)`


### solution.ipynb: original cell 26 (code)

Opening: `def computeCost(x, y, theta):`

Saved execution count: 26. Outputs: 0.


### solution.ipynb: original cell 27 (code)

Opening: `def gradientDescent(x, y, theta, alpha, iterations):`

Saved execution count: 28. Outputs: 0.


### solution.ipynb: original cell 28 (code)

Opening: `from sklearn.preprocessing import StandardScaler`

Saved execution count: 29. Outputs: 0.


### solution.ipynb: original cell 29 (code)

Opening: `theta_init = np.zeros((2, 1))`

Saved execution count: 30. Outputs: 1.

Saved text excerpt:

```text
Theta found by Gradient Descent: slope = [257719.07230277] and intercept [540064.82548774]

```


### solution.ipynb: original cell 30 (code)

Opening: `predictions = xg_norm.dot(theta)`

Saved execution count: 31. Outputs: 1.

Saved text excerpt:

```text
<Figure size 1000x600 with 1 Axes>
```


### solution.ipynb: original cell 31 (code)

Opening: `plt.figure(figsize=(10, 6))`

Saved execution count: 32. Outputs: 1.

Saved text excerpt:

```text
<Figure size 1000x600 with 1 Axes>
```


### solution.ipynb: original cell 32 (markdown)

## 1.2 Multiple Linear Regression

Opening: `## 1.2 Multiple Linear Regression`


### solution.ipynb: original cell 33 (code)

Opening: `from sklearn.linear_model import LinearRegression`

Saved execution count: 33. Outputs: 2.

Saved text excerpt:

```text
Intercept: 6643873.527879483
Coefficients:
  bedrooms: -34335.4187
  bathrooms: 44564.5289
  sqft_living: 109.0158
  sqft_lot: 0.0888
  floors: 7003.1295
  waterfront: 562413.0700
  view: 53641.1070
  condition: 24526.7101
  grade: 94567.8917
  sqft_above: 70.0227
  sqft_basement: 38.9931
  yr_built: -2680.7689
  yr_renovated: 20.4156
  zipcode: -552.2530
  lat: 595968.1221
  long: -194585.7240
  sqft_living15: 21.2143
  sqft_lot15: -0.3258

MSE:  45173046132.79
RMSE: 212539.52
R²:   0.7012

<Figure size 800x500 with 1 Axes>
```


### solution.ipynb: original cell 34 (markdown)

## 1.3 Linear Regression with Regularization

Opening: `## 1.3 Linear Regression with Regularization`


### solution.ipynb: original cell 35 (markdown)

### Types of Regularization
#### 1. Ridge Regression (L2 Regularization):
#### 2. Lasso Regression (L1 Regularization):

Opening: `In traditional linear regression, we try to find the best-fitting line by minimizing the cost function . However, when dealing with complex data, overfitting can occur, especially when the model is too complex or when th`


### solution.ipynb: original cell 36 (markdown)

Opening: `Explain **When to Use Ridge Regression and Lasso Regression**.`


### solution.ipynb: original cell 37 (markdown)

Opening: `Also explain **the effect of the regularization parameter**: `


### solution.ipynb: original cell 38 (markdown)

Opening: `Complete the code below for the linear regression class.`


### solution.ipynb: original cell 39 (code)

Opening: `class LinearRegression:`

Saved execution count: 36. Outputs: 0.


### solution.ipynb: original cell 40 (code)

Opening: `# Do not change this cell`

Saved execution count: 39. Outputs: 0.


### solution.ipynb: original cell 41 (markdown)

Opening: `Apply train-test split.`


### solution.ipynb: original cell 42 (code)

Opening: `X_fit, X_val, y_fit, y_val = train_test_split(X, y, test_size=0.2, random_state=42)`

Saved execution count: 40. Outputs: 0.


### solution.ipynb: original cell 43 (markdown)

Opening: `Visualize your data points.`


### solution.ipynb: original cell 44 (code)

Opening: `fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(14, 5))`

Saved execution count: 41. Outputs: 1.

Saved text excerpt:

```text
<Figure size 1400x500 with 2 Axes>
```


### solution.ipynb: original cell 45 (markdown)

Opening: `Train your model and  evaluate your model using MMSE, $R^2$ criterions, how well is your model trained?`


### solution.ipynb: original cell 46 (code)

Opening: `def mse(y, predictions):`

Saved execution count: 43. Outputs: 0.


### solution.ipynb: original cell 47 (code)

Opening: `model = LinearRegression(lr=0.01, n_iters=1000, penalty='l2', lambda_=0.1)`

Saved execution count: 44. Outputs: 3.

Saved text excerpt:

```text
101.13803939898942

<Figure size 1000x500 with 1 Axes>
Train MSE: 101.1380
Train R²:  0.9800

```


### solution.ipynb: original cell 48 (code)

Opening: `y_pred_val = model.predict(X_val)`

Saved execution count: 45. Outputs: 2.

Saved text excerpt:

```text
<Figure size 1000x500 with 1 Axes>
Validation MSE: 77.9137
Validation R²:  0.9815
77.91367703665051
77.91367703665051

```


### solution.ipynb: original cell 49 (markdown)

### Ridge Regression:

Opening: `### Ridge Regression:`


### solution.ipynb: original cell 50 (code)

Opening: `lambdas = [0.001, 0.01, 0.1, 1, 10, 100]`

Saved execution count: 46. Outputs: 2.

Saved text excerpt:

```text
<Figure size 1000x500 with 1 Axes>
Train MSE: 285.3865
Train R²:  0.9434

```


### solution.ipynb: original cell 51 (code)

Opening: `for lam in lambdas:`

Saved execution count: 59. Outputs: 4.

Saved text excerpt:

```text
<Figure size 1000x500 with 1 Axes>
Validation MSE: 230.3129
Validation R²:  0.9453

<Figure size 1000x500 with 1 Axes>
Best λ: 1

```


### solution.ipynb: original cell 52 (markdown)

### Lasso Regression:

Opening: `### Lasso Regression:`


### solution.ipynb: original cell 53 (code)

Opening: `lambdas = [0.001, 0.01, 0.1, 1, 10, 100]`

Saved execution count: 60. Outputs: 2.

Saved text excerpt:

```text
<Figure size 1000x500 with 1 Axes>
Train MSE: 157.6083
Train R²:  0.9688

```


### solution.ipynb: original cell 54 (code)

Opening: `for lam in lambdas:`

Saved execution count: 61. Outputs: 4.

Saved text excerpt:

```text
<Figure size 1000x500 with 1 Axes>
Validation MSE: 123.8484
Validation R²:  0.9706

<Figure size 1000x500 with 1 Axes>
Best λ: 1

```


### solution.ipynb: original cell 55 (markdown)

# Problem 2 : Discriminant Analysis and Generative Modeling

Opening: `# Problem 2 : Discriminant Analysis and Generative Modeling`


### solution.ipynb: original cell 56 (markdown)

## Introduction

Opening: `## Introduction`


### solution.ipynb: original cell 57 (markdown)

### Import Libraries

Opening: `### Import Libraries`


### solution.ipynb: original cell 58 (code)

Opening: `import numpy as np`

Saved execution count: 54. Outputs: 0.


### solution.ipynb: original cell 59 (markdown)

### Data Loading and Visualization 

Opening: `### Data Loading and Visualization `


### solution.ipynb: original cell 60 (code)

Opening: `dataset = pd.read_csv(r'C:\Users\Asus\OneDrive\Desktop\EE_Archive\6th_semester\MachineLearning\CHW\HW3\discriminant_data.csv')`

Saved execution count: 55. Outputs: 2.

Saved text excerpt:

```text
          x         y  label
0  1.638965  1.500701      0
1  0.677570  2.200600      0
2  2.319851  2.085714      0
3  0.248644  1.016079      0
4  2.135297  2.677857      0
(300, 3)
label
0    100
1    100
2    100
Name: count, dtype: int64

<Figure size 800x600 with 1 Axes>
```


### solution.ipynb: original cell 61 (markdown)

## Discriminant Analysis Implementation

Opening: `## Discriminant Analysis Implementation`


### solution.ipynb: original cell 62 (markdown)

### LDA

Opening: `### LDA`


### solution.ipynb: original cell 63 (code)

Opening: `def fit_lda(X, y):`

Saved execution count: 56. Outputs: 2.

Saved text excerpt:

```text
LDA Accuracy: 1.0000

<Figure size 800x600 with 1 Axes>
```


### solution.ipynb: original cell 64 (markdown)

### QDA

Opening: `### QDA`


### solution.ipynb: original cell 65 (code)

Opening: `def fit_qda(X, y):`

Saved execution count: 57. Outputs: 2.

Saved text excerpt:

```text
QDA Accuracy: 1.0000

<Figure size 800x600 with 1 Axes>
```


### solution.ipynb: original cell 66 (markdown)

## Robustness to Noise

Opening: `## Robustness to Noise`


### solution.ipynb: original cell 67 (code)

Opening: `def add_noise(X, y, seed=42):`

Saved execution count: 58. Outputs: 0.


### solution.ipynb: original cell 68 (markdown)

Opening: `Re-train your LDA and QDA models on the noisy dataset and visualize the new boundaries. Observe how the decision regions warp in response to the outliers.`


### solution.ipynb: original cell 69 (code)

Opening: `X_noisy, y_noisy = add_noise(X, y)`

Saved execution count: 59. Outputs: 2.

Saved text excerpt:

```text
<Figure size 1400x600 with 2 Axes>
LDA Accuracy with Noise: 0.8914
QDA Accuracy with Noise: 0.8943

```


### solution.ipynb: original cell 70 (markdown)

## Generative Modeling

Opening: `## Generative Modeling`


### solution.ipynb: original cell 71 (code)

Opening: `def generate_data(means, covs, n_samples_per_class=10):`

Saved execution count: 60. Outputs: 1.

Saved text excerpt:

```text
<Figure size 1400x600 with 2 Axes>
```


### solution.ipynb: original cell 72 (markdown)

## Quantitative Evaluation of Generative Models
### 6.1. Information Theoretic Metric: KL Divergence
### 6.2. Statistical Moment Matching

Opening: `## Quantitative Evaluation of Generative Models`


### solution.ipynb: original cell 73 (code)

Opening: `def calculate_kl_divergence(original, generated, bins=20):`

Saved execution count: 61. Outputs: 0.


### solution.ipynb: original cell 74 (markdown)

Opening: `Generate samples using the parameters obtained from your model trained on the original dataset. Use the functions above to report the KL Divergence and statistical errors.`


### solution.ipynb: original cell 75 (code)

Opening: `gen_clean = generate_data(means_q, covs_q, n_samples_per_class=100)`

Saved execution count: 62. Outputs: 1.

Saved text excerpt:

```text
 Clean Dataset 
KL Divergence:      4.4959
Mean Error:         0.0362
Covariance Error:   0.5788

 Noisy Dataset 
KL Divergence:      8.1467
Mean Error:         0.1125
Covariance Error:   0.5865

```


### solution.ipynb: original cell 76 (markdown)

Opening: `Does the inclusion of noise increase the KL Divergence? Based on the Mean and Covariance error metrics, which parameter ($\mu$ or $\Sigma$) is more heavily distorted by the presence of outliers? Explain why this happens `


### solution.ipynb: original cell 77 (markdown)

## Theorical Questions
### Q1. LDA vs. QDA:
### Q2. Robustness and Noise:
### Q3. Generative Modeling:
### Q4. Metrics:

Opening: `## Theorical Questions`


### solution.ipynb: original cell 78 (markdown)

# Problem 3: Some Minor Questions...

Opening: `# Problem 3: Some Minor Questions...`


### solution.ipynb: original cell 79 (markdown)

### Problem 3.1: Heteroskedastic Regression

Opening: `### Problem 3.1: Heteroskedastic Regression`


### solution.ipynb: original cell 80 (code)

Opening: `# Problem 3.1`

Saved execution count: 5. Outputs: 3.

Saved text excerpt:

```text
<Figure size 900x500 with 1 Axes>
WLS Parameters: θ₀=3.6637, θ₁=0.6170, θ₂=1.9542

<Figure size 900x500 with 1 Axes>
```


### solution.ipynb: original cell 81 (markdown)

### my proposed functional forms for μ(x) and σ²(x)
### Why Weighted Least Squares (WLS)?
### estimated Parameters

Opening: `### my proposed functional forms for μ(x) and σ²(x)`


### solution.ipynb: original cell 82 (markdown)

### Problem 3.2: Overfitting and Weight Amplitude

Opening: `### Problem 3.2: Overfitting and Weight Amplitude`


### solution.ipynb: original cell 83 (code)

Opening: `# Problem 3.2`

Saved execution count: 6. Outputs: 2.

Saved text excerpt:

```text
Features:  3 | Train MSE: 0.2947 | Test MSE: 0.2239 | L2-norm: 4.8566
Features: 10 | Train MSE: 0.2736 | Test MSE: 0.2705 | L2-norm: 4.7701
Features: 25 | Train MSE: 0.1910 | Test MSE: 0.3931 | L2-norm: 4.8120
Features: 50 | Train MSE: 0.0504 | Test MSE: 1.2304 | L2-norm: 5.0782

<Figure size 1300x500 with 2 Axes>
```


### solution.ipynb: original cell 84 (markdown)

## Problem 3.2: what i see

Opening: `## Problem 3.2: what i see`


### solution.ipynb: original cell 85 (markdown)

### Problem 3.3: The Bayesian Inverse Problem

Opening: `### Problem 3.3: The Bayesian Inverse Problem`


### solution.ipynb: original cell 86 (code)

Opening: `# Problem 3.3`

Saved execution count: 14. Outputs: 2.

Saved text excerpt:

```text
X_hist shape:        (1000, 50)
Y_batch shape (fix): (20, 20)
A shape:             (20, 50)
Reconstructed shape: (20, 50)
Average Reconstruction MSE across batch: 0.904600

<Figure size 1400x600 with 6 Axes>
```


### solution.ipynb: original cell 87 (markdown)

### cost Function design
### Why the prior is necessary
### reconstruction effectiveness

Opening: `### cost Function design`


### solution.ipynb: original cell 88 (code)

Opening: `import matplotlib.pyplot as plt`

Saved execution count: 65. Outputs: 1.

Saved text excerpt:

```text
Active figures: []
Figure managers: []
Figures in garbage collector: 5

```
