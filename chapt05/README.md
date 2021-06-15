# Chapter 5: Support Vector Machines

[HOME](/README.md)

## Misc References

- [Author's Jupyter Notebook](https://github.com/ageron/handson-ml2/blob/master/05_support_vector_machines.ipynb)
- [Stat Quest - Part 1: Support Vector Machines](https://youtu.be/efR1C6CvhmE)
- [Stat Quest - Part 2: The Polynomial Kernel](https://www.youtube.com/watch?v=Toet3EiSFcM&t=0s)
- [Stat Quest - Part 3: The Radial (RBF) Kernel](https://www.youtube.com/watch?v=Qc5IyLW_hns&t=0s)

## Study Group Notebooks

- [Taraqur](https://colab.research.google.com/drive/1WMOYwa2GhspBRzE2mZShjzsG9oV63x8a)

## Topics Covered

- Linear SVM Classification
  - Soft Margin Classification
- Nonlinear SVM Classification
  - Polynomial Kernel
  - Similarity Features
  - Gaussian RBF Kernel
- Computational Complexity  
- SVM Regression
  - Decision Function and Predictions
  - Training Objective
  - Quadratic Programming
  - The Dual Problem
  - The Kernel Trick
- Kernelized SVMs
- Mercer’s theorem
- Online SVMs
- Hinge loss

## Book Questions (p212)

### Q5.1 What is the fundamental idea behind Support Vector Machines?

[Answer](q_5_1_ans.md)

### Q5.2 What is a support vector?

[Answer](q_5_2_ans.md)

### Q5.3 Why is it important to scale the inputs when using SVMs?

[Answer](q_5_3_ans.md)

### Q5.4 Can an SVM classifier output a confidence score when it classifies an instance? What about a probability?

[Answer](q_5_4_ans.md)

### Q5.5 Should you use the primal or the dual form of the SVM problem to train a model on a training set with millions of instances and hundreds of features?

[Answer](q_5_5_ans.md)

### Q5.6 Say you’ve trained an SVM classifier with an RBF kernel, but it seems to underfit the training set. Should you increase or decrease γ ( )? What about C?

[Answer](q_5_6_ans.md)

### Q5.7 How should you set the QP parameters (H, f, A, and b) to solve the soft margin linear SVM classifier problem using an off-the-shelf QP solver?

[Answer](q_5_7_ans.md)

### Q5.8 Train a on a linearly separable dataset. Then train an and a on the same dataset. See if you can get them to produce roughly the same model

***

### Q5.9 Train an SVM classifier on the MNIST dataset. Since SVM classifiers are binary classifiers, you will need to use one-versus-the-rest to classify all 10 digits. You may want to tune the hyperparameters using small validation sets to speed up the process. What accuracy can you reach?

***

### Q5.10 Train an SVM regressor on the California housing dataset

***
