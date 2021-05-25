# Chapter 4: Training Models

[Author's Jupyter Notebook](https://github.com/ageron/handson-ml2/blob/master/04_training_linear_models.ipynb)

## Topics Covered

- Linear Regression
  - Normal Equation - closed form solution
  - Gradient Descent
    - Batch Gradient Descent - compute error with all values then step
    - Stochastic Gradient Descent - random instance for each step
    - Mini-batch Gradient Descent - small random set for each step
- Polynomial Regression
  - Add powers of each feature
  - Still a linear model
- Learning Curves
- Regularized Linear Models
  - Reduces overfitting
  - Ridge Regression
    - L2 Norm
  - Lasso Regression
    - L1 Norm
  - Elastic Net
  - Early Stopping
- Logistic Regression
  - Training and Cost Function
  - Decision Boundaries
  - Softmax Regression
  - Cross entropy

## Book Questions (p212)

### Q4.1 Which Linear Regression training algorithm can you use if you have a training set with millions of features?

[Answer](q_4_1_ans.md)

### Q4.2 Suppose the features in your training set have very different scales. Which algorithms might suffer from this, and how? What can you do about it?

[Answer](q_4_2_ans.md)

### Q4.3 Can Gradient Descent get stuck in a local minimum when training a Logistic Regression model?

[Answer](q_4_3_ans.md)


## Questions


### Level 1: Beginner

- Describe the Bias/Variance Tradeoff

### Level 2: Intermediate

- If the model keeps underfitting the data, what should you do?

### Level 3: Master
