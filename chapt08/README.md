# Chapter 8: Dimensionality Reduction

[HOME](/README.md)

## Misc References

- [Author's Jupyter Notebook](https://github.com/ageron/handson-ml2/blob/master/08_dimensionality_reduction.ipynb)
- [StatQuest - Principal Component Analysis (PCA), Step-by-Step](https://youtu.be/FgakZw6K1QQ)

## Study Group Notebooks

- [Taraqur](https://colab.research.google.com/drive/1G74Vs4EnBBuIzN44SJ7fqQS-bP8p14fh)

## Topics Covered

- Curse of Dimensionality
- Main Approaches for Dimensionality Reduction
  - Projection
  - Manifold Learning
    - Manifold hypothesis
    - task will be simpler if expressed in the lower-dimensional space of the manifold
    - Locally Linear Embedding - LLE
- Projection
  - PCA
    - Identifies the hyperplane that lies closest to the data, and then it projects the data onto it
    - Preserving the Variance
    - Principal Components
    - Projecting Down to d Dimensions
    - Explained Variance Ratio
    - Choosing the Right Number of Dimensions
  - PCA for Compression
  - Randomized PCA
  - Incremental PCA
- Kernel PCA
  - Kernel trick, again
  - Selecting a Kernel and Tuning Hyperparameters

## Book Questions

### Q8.1. What are the main motivations for reducing a dataset’s dimensionality? What are the main drawbacks?

p300

***

### Q8.2. What is the curse of dimensionality?

***

### Q8.3. Once a dataset’s dimensionality has been reduced, is it possible to reverse the operation? If so, how? If not, why?

***

### Q8.4. Can PCA be used to reduce the dimensionality of a highly nonlinear dataset?

***

### Q8.5. Suppose you perform PCA on a 1,000-dimensional dataset, setting the explained variance ratio to 95%. How many dimensions will the resulting dataset have?

***

### Q8.6. In what cases would you use vanilla PCA, Incremental PCA, Randomized PCA, or Kernel PCA?

***

### Q8.7. How can you evaluate the performance of a dimensionality reduction algorithm on your dataset?

***

### Q8.8. Does it make any sense to chain two different dimensionality reduction algorithms?

***
