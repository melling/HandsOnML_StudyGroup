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

Minibatch, SGD (table on p185)

### Q4.2 Suppose the features in your training set have very different scales. Which algorithms might suffer from this, and how? What can you do about it?

SGD, 

Use Scaling

MinMax Scaling: (x - Min) / (Range=Max - Min) # Results [0..1]
Standardization: (x-mean) / sigma  # Good when we have outliers

### Q4.3 Can Gradient Descent get stuck in a local minimum when training a Logistic Regression model?

"The good news is that this cost function is convex, so Gradient Descent (or any other optimization algorithm) is guaranteed to find the global minimum (if the learning rate is not too large and you wait long enough)."  p204 

https://en.wikipedia.org/wiki/Convex_function


## Questions


### Level 1: Beginner

- Describe the Bias/Variance Tradeoff

### Level 2: Intermediate

- If the model keeps underfitting the data, what should you do?

### Level 3: Master
