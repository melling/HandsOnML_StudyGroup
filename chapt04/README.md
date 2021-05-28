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

### Q4.4 Do all Gradient Descent algorithms lead to the same model, provided you let them run long enough

[Answer](q_4_4_ans.md)

### Q4.5 Suppose you use Batch Gradient Descent and you plot the validation error at every epoch. If you notice that the validation error consistently goes up, what is likely going on? How can you fix this?

[Answer](q_4_5_ans.md)

### Q4.6 Is it a good idea to stop Mini-batch Gradient Descent immediately when the validation error goes up?

[Answer](q_4_6_ans.md)

### Q4.7 Which Gradient Descent algorithm (among those we discussed) will reach the vicinity of the optimal solution the fastest? Which will actually converge? How can you make the others converge as well?

[Answer](q_4_7_ans.md)

### Q4.8 Suppose you are using Polynomial Regression. You plot the learning curves and you notice that there is a large gap between the training error and the validation error. What is happening? What are three ways to solve this?

[Answer](q_4_8_ans.md)

### Q4.9 Suppose you are using Ridge Regression and you notice that the training error and the validation error are almost equal and fairly high. Would you say that the model suffers from high bias or high variance? Should you increase the regularization hyperparameter α or reduce it?

[Answer](q_4_9_ans.md)

### Q4.10 Why would you want to use:

- a. Ridge Regression instead of plain Linear Regression (i.e., without any regularization)?
- b. Lasso instead of Ridge Regression?
- c. Elastic Net instead of Lasso?

[Answer](q_4_10_ans.md)

### Q4.11 Suppose you want to classify pictures as outdoor/indoor and daytime/nighttime. Should you implement two Logistic Regression classifiers or one Softmax Regression classifier?

[Answer](q_4_11_ans.md)

### Q4.12 Implement Batch Gradient Descent with early stopping for Softmax Regression (without using Scikit-Learn)

To be implemented individually.

## Questions

### Level 1: Beginner

- Describe the Bias/Variance Tradeoff

### Level 2: Intermediate

- If the model keeps underfitting the data, what should you do?

### Level 3: Master
