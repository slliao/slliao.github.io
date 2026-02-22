---
title: Top 10 algorthims in 20 centry
categories: [Tools, Numerical methods]
tags: [Algorithms]
pin: True
math: true
---

Very interesting [series](https://www.cs.fsu.edu/~lacher/courses/COT4401/notes/cise_v2_i1/index.html) on the top 10 algorithms with the greatest influence on the development and practice of science and engineering in the 20th century.

 - Metropolis Algorithm for Monte Carlo
 - Simplex Method for Linear Programming
 - Krylov Subspace Iteration Methods
 - The Decompositional Approach to Matrix Computations
 - The Fortran Optimizing Compiler
 - QR Algorithm for Computing Eigenvalues
 - Quicksort Algorithm for Sorting
 - Fast Fourier Transform
 - Integer Relation Detection
 - Fast Multipole Method

Source: [Computing in Science & Engineering ( Volume: 2, Issue: 1, Jan.-Feb. 2000)](https://doi.org/10.1109/MCISE.2000.814652)

---

## 同場加映：Top Equations in Machine Learning

### Probability & Statistics

**Normal Distribution**

$$f(x \mid \mu, \sigma^2) = \frac{1}{\sigma\sqrt{2\pi}} \exp\!\left( -\frac{(x-\mu)^2}{2\sigma^2} \right)$$

The probability density function of a Gaussian distribution with mean $\mu$ and variance $\sigma^2$. The backbone of parametric statistics and many ML models.

**Z-Score**

$$z = \frac{x - \mu}{\sigma}$$

Standardizes a value $x$ by expressing how many standard deviations it lies from the mean. Used in feature scaling and anomaly detection.

**Shannon Entropy**

$$H = -\sum_{i} p_i \log_2(p_i)$$

Measures the average information content (uncertainty) of a discrete probability distribution. A uniform distribution has maximum entropy; a deterministic distribution has zero entropy.

**KL Divergence**

$$D_{KL}(P \| Q) = \sum_{x \in \mathcal{X}} P(x) \log\!\left( \frac{P(x)}{Q(x)} \right)$$

Measures how much probability distribution $P$ diverges from a reference distribution $Q$. Always $\geq 0$, and not symmetric: $D_{KL}(P \| Q) \neq D_{KL}(Q \| P)$.

---

### Linear Algebra

**Eigenvalue Equation**

$$Av = \lambda v$$

Defines the eigenvectors $v$ and eigenvalues $\lambda$ of a matrix $A$. Fundamental to PCA, spectral clustering, and stability analysis of dynamical systems.

**Singular Value Decomposition (SVD)**

$$A = U \Sigma V^T$$

Decomposes any $m \times n$ matrix $A$ into orthogonal matrices $U$, $V$ and a diagonal matrix $\Sigma$ of singular values. The foundation of PCA, latent semantic analysis, and low-rank matrix approximation.

---

### Regression & Loss

**Linear Regression**

$$y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \cdots + \beta_n x_n + \epsilon$$

Models the relationship between a response variable $y$ and predictors $x_1, \dots, x_n$ with additive Gaussian noise $\epsilon$.

**OLS — Ordinary Least Squares**

$$\hat{\beta} = (X^T X)^{-1} X^T y$$

The closed-form solution (normal equations) to linear regression. Minimizes the sum of squared residuals; requires $X^TX$ to be invertible.

**Mean Squared Error (MSE)**

$$\text{MSE} = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2$$

The average squared difference between predicted and true values. The standard loss function for regression; sensitive to outliers due to squaring.

**Ridge Regression (MSE + L2)**

$$\mathcal{L}_{\text{ridge}} = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2 + \lambda \sum_{j=1}^{p} \beta_j^2$$

Adds an L2 penalty $\lambda \sum \beta_j^2$ to MSE, shrinking coefficients toward zero to reduce overfitting. $\lambda$ controls the regularization strength.

**R² Score (Coefficient of Determination)**

$$R^2 = 1 - \frac{\sum_{i=1}^{n} (y_i - \hat{y}_i)^2}{\sum_{i=1}^{n} (y_i - \bar{y})^2}$$

Measures the proportion of variance in $y$ explained by the model. $R^2 = 1$ is a perfect fit; $R^2 = 0$ means the model is no better than predicting the mean.

**Log Loss (Binary Cross-Entropy)**

$$\mathcal{L} = -\frac{1}{N} \sum_{i=1}^{N} \bigl[y_i \log(\hat{y}_i) + (1 - y_i) \log(1 - \hat{y}_i)\bigr]$$

The standard loss function for binary classification. Penalizes confident wrong predictions heavily; minimizing log loss is equivalent to maximizing likelihood under a Bernoulli model.

---

### Optimization

**Gradient Descent**

$$\theta_{j+1} = \theta_j - \alpha \nabla J(\theta_j)$$

Iteratively updates parameters by moving in the direction of steepest descent of the loss $J$. $\alpha$ is the learning rate controlling the step size.

**Maximum Likelihood Estimation (MLE)**

$$\hat{\theta} = \operatorname*{argmax}_{\theta} \prod_{i=1}^{n} P(x_i \mid \theta)$$

Finds the parameter $\theta$ that makes the observed data most probable, assuming i.i.d. samples. In practice, the log-likelihood $\sum \log P(x_i \mid \theta)$ is maximized for numerical stability.

**Lagrange Multiplier**

$$\mathcal{L}(x, \lambda) = f(x) - \lambda \cdot g(x)$$

Transforms a constrained optimization (minimize $f(x)$ subject to $g(x) = 0$) into an unconstrained one. At the optimum, $\nabla f = \lambda \nabla g$. Used in SVMs, entropy maximization, and control theory.

---

### Activation Functions

**Sigmoid**

$$\sigma(x) = \frac{1}{1 + e^{-x}}$$

Squashes any real-valued input into $(0, 1)$. Used for binary classification output layers and as a gating mechanism in LSTMs.

**ReLU (Rectified Linear Unit)**

$$f(x) = \max(0,\, x)$$

Sets negative values to zero. Computationally cheap, avoids the vanishing gradient problem for positive inputs, and is the default activation in most modern deep networks.

**Softmax**

$$P(y = j \mid x) = \frac{e^{x^T w_j}}{\sum_{k=1}^{K} e^{x^T w_k}}$$

Converts a vector of raw scores (logits) into a probability distribution over $K$ classes. The multi-class generalization of sigmoid.

---

### Similarity & Clustering

**Pearson Correlation**

$$\rho = \frac{\text{Cov}(X, Y)}{\text{Std}(X) \cdot \text{Std}(Y)}$$

Measures the linear relationship between two variables; ranges from $-1$ (perfect negative) to $+1$ (perfect positive). Zero implies no linear dependence.

**Cosine Similarity**

$$\text{similarity}(A, B) = \frac{A \cdot B}{\|A\| \|B\|}$$

Measures the cosine of the angle between two vectors. Direction-sensitive but magnitude-insensitive; widely used in NLP and information retrieval.

**K-Means Objective**

$$\operatorname*{argmin}_{S} \sum_{i=1}^{k} \sum_{x \in S_i} \|x - \mu_i\|^2$$

Partitions data into $k$ clusters $S_1, \dots, S_k$ by minimizing total within-cluster variance. $\mu_i$ is the centroid of cluster $S_i$.

---

### Classification

**Naive Bayes**

$$P(y \mid x_1, \dots, x_n) = \frac{P(y) \prod_{i=1}^{n} P(x_i \mid y)}{P(x_1, \dots, x_n)}$$

Applies Bayes' theorem with the "naive" assumption that features are conditionally independent given the class label. The denominator is constant across classes and is dropped during prediction.

**F1 Score**

$$F_1 = \frac{2 \cdot P \cdot R}{P + R}$$

The harmonic mean of Precision ($P$) and Recall ($R$). Useful when classes are imbalanced and both false positives and false negatives matter.

**SVM — Soft-Margin**

$$\min_{w,\, b} \;\frac{1}{2}\|w\|^2 + C \sum_{i=1}^{n} \max\!\bigl(0,\, 1 - y_i(w \cdot x_i - b)\bigr)$$

Finds the maximum-margin hyperplane while allowing misclassifications via hinge loss. $C$ controls the trade-off between margin width and training error tolerance.
