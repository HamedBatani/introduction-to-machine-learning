# CHW4 — Notebook navigation

Cell indices refer to the unmodified source notebook, before the added archival note. This guide maps the available prompts, code, and saved textual outputs; see the README for their interpretation.

### solution.ipynb: original cell 0 (markdown)

Opening: `<font face="Times New Roman" size=5>`


### solution.ipynb: original cell 1 (markdown)

## هدف تمرین
### قوانین تحویل
### نمره‌بندی کلی

Opening: `<div dir="rtl">`


### solution.ipynb: original cell 2 (code)

Opening: `# Common imports`

Saved execution count: 2. Outputs: 0.


### solution.ipynb: original cell 3 (markdown)

# Problem 1: Multi-Layer Perceptron on a Real Tabular Dataset — 30 pts

Opening: `# Problem 1: Multi-Layer Perceptron on a Real Tabular Dataset — 30 pts`


### solution.ipynb: original cell 4 (markdown)

## 1.1 Loading, preprocessing, and exploratory analysis — 4 pts
### پاسخ :

Opening: `## 1.1 Loading, preprocessing, and exploratory analysis — 4 pts`


### solution.ipynb: original cell 5 (code)

Opening: `train_df = pd.read_csv(os.path.join(DATA_DIR, "wine_train.csv"))`

Saved execution count: 3. Outputs: 3.

Saved text excerpt:

```text
 Data Dimensions 
train shape: (106, 14)
validation shape: (36, 14)
test shape: (36, 14)

Feature دames 
['alcohol', 'malic_acid', 'ash', 'alcalinity_of_ash', 'magnesium', 'total_phenols', 'flavanoids', 'nonflavanoid_phenols', 'proanthocyanins', 'color_intensity', 'hue', 'od280/od315_of_diluted_wines', 'proline'] 

class Distribution 
target
1    42
0    35
2    29
Name: count, dtype: int64

<Figure size 600x400 with 1 Axes>
<Figure size 600x400 with 1 Axes>
```


### solution.ipynb: original cell 6 (markdown)

## 1.2 Linear baseline — 5 pts
### پاسخ:

Opening: `## 1.2 Linear baseline — 5 pts`


### solution.ipynb: original cell 7 (code)

Opening: `# TODO: train a linear baseline model`

Saved execution count: 8. Outputs: 3.

Saved text excerpt:

```text
train accuracy: 100.00%
validation accuracy: 100.00%
test accuracy: 100.00%


<Figure size 600x400 with 2 Axes>
top 3 features by absolute weight:
color_intensity: 0.6711
flavanoids: 0.6316
alcalinity_of_ash: 0.5465

```


### solution.ipynb: original cell 8 (markdown)

## 1.3 Implementing an MLP from scratch with NumPy — 10 pts

Opening: `## 1.3 Implementing an MLP from scratch with NumPy — 10 pts`


### solution.ipynb: original cell 9 (code)

Opening: `class Dense:`

Saved execution count: 9. Outputs: 0.


### solution.ipynb: original cell 10 (markdown)

## 1.4 Gradient checking — 4 pts
### پاسخ :

Opening: `## 1.4 Gradient checking — 4 pts`


### solution.ipynb: original cell 11 (code)

Opening: `# TODO: implement gradient_check(model, X_batch, y_batch)`

Saved execution count: 10. Outputs: 1.

Saved text excerpt:

```text
layer 2 param b(0,): analytic=-6.311871e-02, numeric=-6.311871e-02, rel_error=3.499742e-09
layer 0 param W(10, 4): analytic=2.175526e-02, numeric=2.175526e-02, rel_error=3.412431e-08
layer 0 param W(6, 4): analytic=1.553398e-01, numeric=1.553398e-01, rel_error=2.222256e-10
layer 0 param W(7, 3): analytic=-9.264309e-03, numeric=-9.264308e-03, rel_error=3.088770e-08
layer 0 param W(4, 1): analytic=-3.214857e-02, numeric=-3.214857e-02, rel_error=6.634868e-09

```


### solution.ipynb: original cell 12 (markdown)

## 1.5 Activation, initialization, and regularization experiments — 7 pts
###  پاسخ :

Opening: `## 1.5 Activation, initialization, and regularization experiments — 7 pts`


### solution.ipynb: original cell 13 (code)

Opening: `# TODO: run at least four experiments`

Saved execution count: None. Outputs: 0.


### solution.ipynb: original cell 14 (code)

Opening: `# TODO: run at least four experiments`

Saved execution count: 11. Outputs: 2.

Saved text excerpt:

```text
<Figure size 1200x400 with 2 Axes>
               train acc   val acc  test acc
sigmoid+small   0.933962  0.833333  0.888889
tanh+xavier     1.000000  1.000000  0.972222
relu+he         1.000000  1.000000  1.000000
relu+he+l2      1.000000  1.000000  1.000000

```


### solution.ipynb: original cell 15 (markdown)

### # TODO: write your analysis in a markdown cell below

Opening: `<div dir="rtl">`


### solution.ipynb: original cell 16 (markdown)

# Problem 2: Convolutional Neural Networks on Handwritten Digits — 35 pts + 4 bonus

Opening: `# Problem 2: Convolutional Neural Networks on Handwritten Digits — 35 pts + 4 bonus`


### solution.ipynb: original cell 17 (markdown)

## 2.1 Manual convolution, padding, stride, and receptive field — 6 pts
### پاسخ :

Opening: `## 2.1 Manual convolution, padding, stride, and receptive field — 6 pts`


### solution.ipynb: original cell 18 (code)

Opening: `manual_img = pd.read_csv(os.path.join(DATA_DIR, "manual_digit_8x8.csv"), header=None).values.astype(float)`

Saved execution count: 12. Outputs: 4.

Saved text excerpt:

```text
<Figure size 300x300 with 1 Axes>
<Figure size 900x300 with 3 Axes>
<Figure size 600x300 with 2 Axes>
p=0, s=1 shape: (6, 6)
same padding shape: (8, 8)
p=0, s=2 shape: (3, 3)

for output cell at (1, 1) with padding=0 and stride=1:
the 3x3 receptive field in the input image covers rows 1 to 3 and columns 1 to 3

```


### solution.ipynb: original cell 19 (markdown)

## 2.2 Loading digits and building PyTorch dataloaders — 4 pts

Opening: `## 2.2 Loading digits and building PyTorch dataloaders — 4 pts`


### solution.ipynb: original cell 20 (code)

Opening: `# TODO: import torch and build TensorDataset/DataLoader for train/val/test`

Saved execution count: 13. Outputs: 2.

Saved text excerpt:

```text
--- Tensor Dimensions ---
X_train: (1168, 1, 8, 8), y_train: (1168,)
X_val: (270, 1, 8, 8), y_val: (270,)
X_test: (359, 1, 8, 8), y_test: (359,)

--- Class Balance ---
class 0: 116 samples
class 1: 118 samples
class 2: 115 samples
class 3: 119 samples
class 4: 118 samples
class 5: 118 samples
class 6: 118 samples
class 7: 116 samples
class 8: 113 samples
class 9: 117 samples

<Figure size 500x1000 with 30 Axes>
```


### solution.ipynb: original cell 21 (markdown)

## 2.3 FlattenMLP vs SmallCNN — 10 pts
### پاسخ :
#### چرا CNN حتی در تصاویر کوچک (8x8) نسبت به MLP مزیت دارد؟

Opening: `## 2.3 FlattenMLP vs SmallCNN — 10 pts`


### solution.ipynb: original cell 22 (code)

Opening: `import torch.nn as nn`

Saved execution count: 14. Outputs: 6.

Saved text excerpt:

```text
=== Training FlattenMLP (Trainable Parameters: 6570) ===
Final Results - Train Acc: 100.00%, Val Acc: 96.67%, Test Acc: 96.94%


<Figure size 1000x300 with 2 Axes>
<Figure size 600x400 with 2 Axes>
=== Training SmallCNN (Trainable Parameters: 1898) ===
Final Results - Train Acc: 99.91%, Val Acc: 97.41%, Test Acc: 98.61%


<Figure size 1000x300 with 2 Axes>
<Figure size 600x400 with 2 Axes>
```


### solution.ipynb: original cell 23 (markdown)

## 2.4 Design a BetterCNN under a parameter budget — 9 pts
### پاسخ :

Opening: `## 2.4 Design a BetterCNN under a parameter budget — 9 pts`


### solution.ipynb: original cell 24 (code)

Opening: `# TODO: define BetterCNN with fewer than 100,000 trainable parameters`

Saved execution count: 15. Outputs: 1.

Saved text excerpt:

```text
=== Architecture Comparison Table ===
       Model  Trainable Params Train Acc Val Acc Test Acc
0   SmallCNN              1898    99.83%  97.41%   98.61%
1  BetterCNN             24170   100.00%  97.04%   98.61%

```


### solution.ipynb: original cell 25 (markdown)

## 2.5 Error analysis — 6 pts

Opening: `## 2.5 Error analysis — 6 pts`


### solution.ipynb: original cell 26 (markdown)

## 2.5 Error analysis — 6 pts
### پاسخ :

Opening: `## 2.5 Error analysis — 6 pts`


### solution.ipynb: original cell 27 (code)

Opening: `import torch.nn.functional as F`

Saved execution count: 16. Outputs: 3.

Saved text excerpt:

```text
<Figure size 600x600 with 2 Axes>
Total misclassified images on test set: 5

--- High Confidence Errors ---
Error 1: True Label = 3, Predicted Label = 8, Confidence = 82.86%
Error 2: True Label = 9, Predicted Label = 5, Confidence = 53.97%
Error 3: True Label = 5, Predicted Label = 9, Confidence = 53.97%
Error 4: True Label = 3, Predicted Label = 8, Confidence = 52.19%
Error 5: True Label = 5, Predicted Label = 2, Confidence = 49.42%

<Figure size 1200x600 with 10 Axes>
```


### solution.ipynb: original cell 28 (markdown)

## 2.6 Bonus: Robustness under distribution shift — 4 bonus pts
### پاسخ :

Opening: `## 2.6 Bonus: Robustness under distribution shift — 4 bonus pts`


### solution.ipynb: original cell 29 (code)

Opening: `# BONUS TODO: evaluate your best CNN on shifted/noisy/low-contrast test sets`

Saved execution count: 20. Outputs: 1.

Saved text excerpt:

```text
=== Robustness Results (BetterCNN) ===
Accuracy on Shifted Test Set: 95.26%
Accuracy on Noisy Test Set: 77.99%
Accuracy on Low Contrast Test Set: 14.48%
Augmentation Strategy Implemented:
- Manual Contrast Adjustment: Directly addresses Low Contrast vulnerability.
- Manual Random Shift: Boosts spatial invariance against distribution shifts.

```


### solution.ipynb: original cell 30 (markdown)

# Problem 3: Kernel Methods — 35 pts + 6 bonus

Opening: `# Problem 3: Kernel Methods — 35 pts + 6 bonus`


### solution.ipynb: original cell 31 (markdown)

## 3.1 Gram matrix and PSD check — 8 pts
### پاسخ :

Opening: `## 3.1 Gram matrix and PSD check — 8 pts`


### solution.ipynb: original cell 32 (code)

Opening: `import os`

Saved execution count: 22. Outputs: 1.

Saved text excerpt:

```text
=== Gram Matrix & PSD Verification Table ===
           Kernel Name Symmetry Error Min Eigenvalue Is PSD?
                Linear       0.00e+00      -0.000000     Yes
    Polynomial (deg=2)       0.00e+00       0.009440     Yes
    Polynomial (deg=3)       0.00e+00      48.553154     Yes
      RBF (gamma=0.01)       0.00e+00       0.000204     Yes
       RBF (gamma=0.1)       0.00e+00       0.043141     Yes
       RBF (gamma=1.0)       0.00e+00       0.736876     Yes
Custom (Rational Quad)       0.00e+00       0.546587     Yes

```


### solution.ipynb: original cell 33 (markdown)

## 3.2 SVM with linear, polynomial, and RBF kernels — 12 pts
### پاسخ:

Opening: `## 3.2 SVM with linear, polynomial, and RBF kernels — 12 pts`


### solution.ipynb: original cell 34 (code)

Opening: `import numpy as np`

Saved execution count: 24. Outputs: 2.

Saved text excerpt:

```text
--- Base Models on Full Features ---
Linear SVM - Val Acc: 100.00%, Support Vectors: 19
Polynomial SVM (deg=3) - Val Acc: 88.89%, Support Vectors: 61

--- Grid Search for RBF SVM ---
   C  Gamma Val Accuracy  Total Support Vectors
 0.1   0.01       44.44%                    104
 0.1   0.10      100.00%                    101
 0.1   1.00       38.89%                    106
 1.0   0.01      100.00%                     62
 1.0   0.10      100.00%                     58
 1.0   1.00       63.89%                    106
10.0   0.01      100.00%                     32
10.0   0.10      100.00%                     53
10.0   1.00       69.44%                    106

<Figure size 1500x400 with 3 Axes>
```


### solution.ipynb: original cell 35 (markdown)

## 3.3 Gaussian Process Regression on Diabetes data — 10 pts
### پاسخ :

Opening: `## 3.3 Gaussian Process Regression on Diabetes data — 10 pts`


### solution.ipynb: original cell 36 (code)

Opening: `from sklearn.gaussian_process import GaussianProcessRegressor`

Saved execution count: 29. Outputs: 2.

Saved text excerpt:

```text
<Figure size 1400x500 with 2 Axes>
--- Gaussian Process Regressor Comparison ---
RBF Kernel Log-Marginal-Likelihood: -161.0494
Rational Quadratic Kernel Log-Marginal-Likelihood: -146.9756

```


### solution.ipynb: original cell 37 (markdown)

## 3.4 Written comparison — 5 pts
### پاسخ :
#### ۱. مدل‌های MLP (پرسیپترون چندلایه): قدرت مدل‌سازی و نیاز به تنظیمات آموزش
#### ۲. مدل‌های CNN (شبکه‌های عصبی کانولوشنی): استفاده از ساختار مکانی تصویر
#### ۳. روش‌های مبتنی بر کرنیل (Kernel Methods): وابستگی به نمونه‌ها، اثر کرنیل و هزینه محاسباتی

Opening: `## 3.4 Written comparison — 5 pts`


### solution.ipynb: original cell 38 (markdown)

## 3.5 Bonus: Scalability and approximate kernels — 3 bonus pts
### پاسخ :

Opening: `## 3.5 Bonus: Scalability and approximate kernels — 3 bonus pts`


### solution.ipynb: original cell 39 (code)

Opening: `import time`

Saved execution count: 31. Outputs: 1.

Saved text excerpt:

```text
=== Scalability & Approximate Kernels Comparison ===
 Train Size Exact RBF Acc Exact RBF Time(s) Linear Acc Linear Time(s) Approx Kernel Acc Approx Time(s)
         31        97.22%            0.0035    100.00%         0.0050            97.22%         0.0060
         63       100.00%            0.0020    100.00%         0.0020           100.00%         0.0060
        106       100.00%            0.0020    100.00%         0.0020           100.00%         0.0070

```


### solution.ipynb: original cell 40 (markdown)

## 3.6 Bonus: Active sampling with Gaussian Process — 3 bonus pts
### پاسخ تشریحی و تحلیلی بخش 3.6 (بر اساس نتایج واقعی آزمایش):

Opening: `## 3.6 Bonus: Active sampling with Gaussian Process — 3 bonus pts`


### solution.ipynb: original cell 41 (code)

Opening: `# BONUS TODO: perform one active-sampling step based on predictive standard deviation`

Saved execution count: 32. Outputs: 2.

Saved text excerpt:

```text
=== Active Sampling Information ===
Chosen point feature value (BMI): 0.1274
Maximum standard deviation at this point: 73.2743

<Figure size 1400x500 with 2 Axes>
```


### solution.ipynb: original cell 42 (markdown)

Opening: `(empty)`
