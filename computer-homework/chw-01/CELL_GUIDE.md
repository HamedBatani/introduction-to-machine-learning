# CHW1 — Notebook navigation

Cell indices refer to the unmodified source notebook, before the added archival note. This guide maps the available prompts, code, and saved textual outputs; see the README for their interpretation.

### solution.ipynb: original cell 0 (markdown)

# Introduction to Machine Learning - Dr. Sajjd Amini
### Practical Homework 1
#### Sharif Uni. of Tech. - EE Dep. - 1404-2 Semester
#### Deadline: Ordibehesht 19th 1404 | May 9th 2026

Opening: `# Introduction to Machine Learning - Dr. Sajjd Amini`


### solution.ipynb: original cell 1 (markdown)

## Part 0: Information

Opening: `<hr>`


### solution.ipynb: original cell 2 (markdown)

## Part 1: Minor Problems
#### 40 Points in total

Opening: `<hr>`


### solution.ipynb: original cell 3 (markdown)

#### **Problem 1.1**: Beta Distribution Update - Bernoulli Likelihood (5 Points) <br>

Opening: `#### **Problem 1.1**: Beta Distribution Update - Bernoulli Likelihood (5 Points) <br>`


### solution.ipynb: original cell 4 (code)

Opening: `import json`

Saved execution count: 14. Outputs: 2.

Saved text excerpt:

```text
<Figure size 640x480 with 1 Axes>
 Prior CDF at x=0.5: 0.4557
posterior CDF at x=0.5: 0.0517

```


### solution.ipynb: original cell 5 (markdown)

#### **Problem 1.2 was deleted **

Opening: `<hr>`


### solution.ipynb: original cell 6 (markdown)

#### **Problem 1.3**: Discrete Random Variable - ML vs MAP update (5 Points) <br>

Opening: `<hr>`


### solution.ipynb: original cell 7 (code)

Opening: `import json`

Saved execution count: 28. Outputs: 2.

Saved text excerpt:

```text
<Figure size 1500x500 with 3 Axes>
mle: [0.226, 0.2209, 0.1886, 0.1286, 0.1145, 0.1214]
map: [0.2517, 0.2195, 0.1804, 0.1268, 0.1082, 0.1134]
Sum of MLE probabilities: 1.000000
Sum of MAP probabilities: 1.000000

```


### solution.ipynb: original cell 8 (markdown)

#### **Problem 1.4**: MVN and Hinton Diagram (10 Points) <br>

Opening: `<hr>`


### solution.ipynb: original cell 9 (code)

Opening: `import numpy as np`

Saved execution count: 6. Outputs: 5.

Saved text excerpt:

```text
Training data: 400 samples, 10 dimensions
Test data: 10 vectors
Samples: 20, MSE: 0.482967
Samples: 40, MSE: 0.451888
Samples: 60, MSE: 0.452729
Samples: 80, MSE: 0.451032
Samples: 100, MSE: 0.460023
Samples: 120, MSE: 0.472365
Samples: 140, MSE: 0.481589
Samples: 160, MSE: 0.484005
Samples: 180, MSE: 0.492203
Samples: 200, MSE: 0.487138
Samples: 220, MSE: 0.474368
Samples: 240, MSE: 0.474362
Samples: 260, MSE: 0.473915
Samples: 280, MSE: 0.472128
Samples: 300, MSE: 0.477498
Samples: 320, MSE: 0.475305
Samples: 340, MSE: 0.470481
Samples: 360, MSE: 0.470440
Samples: 380, MSE: 0.475014
Samples: 400, MSE: 0.473487

<Figure size 1000x600 with 1 Axes>

--- Explanation of Error Plot ---
Trend: MSE decreases as more training samples are used, showing improved imputation accuracy.
Error Floor: MSE approaches a minimum value (floor) as the model converges to true distribution.
Reason: With more 
```


### solution.ipynb: original cell 10 (markdown)

Opening: `Explanation of Error Plot :`


### solution.ipynb: original cell 11 (markdown)

#### **Problem 1.5**: Decision Tree (10 Points) <br><br>

Opening: `<hr>`


### solution.ipynb: original cell 12 (code)

Opening: `import numpy as np`

Saved execution count: 9. Outputs: 6.

Saved text excerpt:

```text
Training data columns : ['Speed', 'Depth', 'Weight', 'Species']
Test data columns:  ['Speed', 'Depth', 'Weight', 'Species']

First few rows of training data:
       Speed      Depth    Weight Species
0   6.436620  13.141169  6.233031       C
1   8.161396  16.405673  5.760266       C
2  23.929454   8.372315  6.635047       A
3  30.000000  12.416869  9.165002       A
4  29.107112   8.985755  8.702215       A

Detected columns :
Weight : Weight
Speed: Speed
Depth : Depth
Species: Species
DECISION TREE STRUCTURE
[Speed ≤ 13.73] (Info Gain: 0.8932)
├─ True:
  [Weight ≤ 2.56] (Info Gain: 0.0375)
  ├─ True:
    → Predict: Hare
  └─ False:
    [Speed ≤ 11.06] (Info Gain: 0.0070)
    ├─ True:
      → Predict: Mole
    └─ False:
      [Speed ≤ 11.09] (Info Gain: 0.1565)
      ├─ True:
        → Predict: Fox
      └─ False:
        → Predict: Mole
└─ False:
  [Weight ≤ 4.10] (Info Gain: 0.9405)
  ├
```


### solution.ipynb: original cell 13 (markdown)

Opening: `I chose the splitting criterion at each node by calculating the information gain for all possible splits across all three features (Weight, Speed, and Burrow Depth)At each node, I evaluated every feature and every thresh`


### solution.ipynb: original cell 14 (markdown)

#### **Problem 1.6**: Linear Gaussian Systems (Sensor Fusion) (10 Points) <br> <br>

Opening: `<hr>`


### solution.ipynb: original cell 15 (code)

Opening: `import numpy as np`

Saved execution count: 15. Outputs: 5.

Saved text excerpt:

```text
estimating sensor statistics 
sensor 1:
  mean: [4.9772261  1.76500291]
  covariance determinant: 0.201865
  covariance:
[[0.09679888 0.01851543]
 [0.01851543 2.08894634]]

sensor 2:
  mean: [3.84907575 3.04429151]
  covariance determinant: 0.200889
  covariance:
[[1.96092121 0.00884999]
 [0.00884999 0.10248618]]

sensor 3:
  mean: [5.38870707 3.6120494 ]
  covariance determinant: 0.822618
  covariance:
[[ 1.27612354 -0.7881386 ]
 [-0.7881386   1.13137986]]

sensor 4:
  mean: [6.28521203 2.19259152]
  covariance determinant: 15.334837
  covariance:
[[ 4.27797162 -0.35318545]
 [-0.35318545  3.61376341]]

sequential bayesian fusion (order: 1->2->3->4) 
initial (sensor 1): mean = [4.9772261  1.76500291], det = 0.201865
after sensor 2: mean = [4.93433272 2.98867319], det = 0.008994
after sensor 3: mean = [5.02667313 3.10115909], det = 0.006965
after sensor 4: mean = [5.05015205 3.08091841], 
```


### solution.ipynb: original cell 16 (markdown)

## Task 1:
## task 2
## task 3 :

Opening: `## Task 1:`


### solution.ipynb: original cell 17 (markdown)

## Part 2: Bayesian Network (25 Points)

Opening: `<hr>`


### solution.ipynb: original cell 18 (code)

Opening: `import numpy as np`

Saved execution count: 28. Outputs: 3.

Saved text excerpt:

```text
running sgs algorithm...
phase 1: removing edges...
phase 2: orienting edges...
learned bayesian network structure:
Market_Sentiment (root node)
    -> Trading_Volume, Stock_Price
Trading_Volume <- Market_Sentiment, Volatility
    -> Stock_Price, Option_Volume
Stock_Price <- Market_Sentiment, Trading_Volume
    -> Option_Volume
Volatility (root node)
    -> Trading_Volume
Option_Volume <- Trading_Volume, Stock_Price

<Figure size 1200x1000 with 1 Axes>

plot saved as 'bayesian_network.png'

```


### solution.ipynb: original cell 19 (markdown)

## Part 3: MiniGPT! (Missing-Token prediction) (35 Points)

Opening: `<hr>`


### solution.ipynb: original cell 20 (code)

Opening: `import json`

Saved execution count: 20. Outputs: 1.

Saved text excerpt:

```text
loading and preprocessing  training data...
training data loaded.

training models...
all models  trained .

loading and preprocessing test data ...
500 test cases loaded.

evaluating models...

 evaluation results  : 
model 1 : bigram accuracy: 23.00%
model 2: trigram accuracy : 18.20%
model3: surrounding words accuracy : 29.60%

```


### solution.ipynb: original cell 21 (markdown)

Opening: `We implemented three discrete statistical models using maximum likelihood estimation to predict the missing token. The first is a Bigram model, an auto-regressive model of order 1. It assumes the missing word depends onl`
