# Parameter-Optimisation-of-SVM
Assignment



## Introduction
This assignment illustrates a way of finding the optimal hyperparameter of Support Vector Classifier. The data set used here is Nursery Data Set from UCI repository.


## Dataset
The data used contains 8 columns and 12,960 rows. 
- parents: usual, pretentious, great_pret
- has_nurs: proper, less_proper, improper, critical, very_crit
- form: complete, completed, incomplete, foster
- children: 1, 2, 3, more
- housing: convenient, less_conv, critical
- finance: convenient, inconv
- social: non-prob, slightly_prob, problematic
- health: recommended, priority, not_recom



## Methodology
The dataset is split into training and testing set for 10 times and the following SVC classifier hyperparameter are selected for best accuracy:
- **Kernel** - Selected from RBF, Polynomial, Linear and Sigmoid
-  **C (Regularisation parameter)** 
- **Gamma (Kernel coefficient)** - Random integer values from -1 to 7. If the value is less than 1, then gamma is randomly set as auto or scale. It is used only by rbf, poly and sigmoid kernel.
- **Degree** - Random integer from 1 to 5. It is only used by poly kernel and represent the degree of polynomial kernel function.

The above hyperparameters are randomly selected from the given values for 100 iterations. The parameters that gave the best accuracy for each sample are shown in table below:

|Sample| Kernel   | Accuracy |
|-----:|:---------|--------- |
|1     | poly     | 0.738646 |
|2     | poly     | 0.823479 |
|3     | poly     | 0.782347 |
|4     | poly     | 0.758354 |
|5     | poly     | 0.602399 |
|6     | poly     | 0.647814 |
|7     | poly     | 0.791773 |
|8     | poly     | 0.783204 |
|9     | poly     | 0.816623 |
|10    | poly     | 0.773778 |

The following Convergence graph shows the accuracy of sample 2 (maximum accuracy) over the 100 iterations:

![Convergence graph of sample 2](./download.png)


## Result
The best parameters of SVC for the given dataset are:
- Kernel : poly
- C : 0.2
- Gamma : 0.5
- Degree : 2

The above parameter gave a maximum accuracy of 0.8234790059982862
