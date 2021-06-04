# Chapter 6: Decision Trees

## Book Questions

###  1. What is the approximate depth of a Decision Tree trained (without restrictions) on a training set with one million instances?

p247

log2(1,000,000)

***

### 2. Is a node’s Gini impurity generally lower or greater than its parent’s? Is it generally lower/greater, or always lower/greater?

See Stat Quest video

Gini index

1 - (the probability of "yes")^2 - (the probability of "no")^2

Generally, it should be lower.  In other words, more pure. Gini 0 = pure

Book Answer: p918

***

### 3. If a Decision Tree is overfitting the training set, is it a good idea to try decreasing max_depth? p247

Yes.

Book Answer: p918

***

### 4. If a Decision Tree is underfitting the training set, is it a good idea to try scaling the input features?

NO

### 5. If it takes one hour to train a Decision Tree on a training set containing 1 million instances, roughly how much time will it take to train another Decision Tree on a training set containing 10 million instances?

Look up forumula. p242

***

### 6. If your training set contains 100,000 instances, will setting speed up training?

Reference: p242

Too much training so it slows it down considerably.

Book Answer: p918
