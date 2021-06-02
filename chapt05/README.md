# Chapter 5: Support Vector Machines

[Author's Jupyter Notebook](https://github.com/ageron/handson-ml2/blob/master/05_support_vector_machines.ipynb)

## Topics Covered


## Exercises

1. What is the fundamental idea behind Support Vector Machines? 

See Figure 5.1 - 215

The fundamental idea behind Support Vector Machines is to fit the widest possible “street” between the classes.
p915

2. What is a support vector?

Any instance that's on the edge of the street

Instances Observations ... p 915

3. Why is it important to scale the inputs when using SVMs?

Can make the margins wider.  Two different axis...

See Figure 5.2

4. Can an SVM classifier output a confidence score when it classifies an instance? What about a probability?

No, no.

5. Should you use the primal or the dual form of the SVM problem to train a model on a training set with millions of instances and hundreds of features?

Use Primal. p230

Dual Form is better when training is smaller than the number of features.

Answer: p916

6. Say you’ve trained an SVM classifier with an RBF kernel, but it seems to underfit the training set. Should you increase or decrease γ ( )? What about C?

p223

increasing Gamma increases regularization

regularization in the left plot (i.e., a large value
more regularization in the right plot (i.e., a small value


7. How should you set the QP parameters (H, f, A, and b) to solve the soft margin linear SVM classifier problem using an off-the-shelf QP solver?

p230


8. Train a on a linearly separable dataset. Then train an and a
on the same dataset. See if you can get them to produce roughly
the same model.


9. Train an SVM classifier on the MNIST dataset. Since SVM classifiers are binary classifiers, you will need to use one-versus-the-rest to classify all 10 digits. You may want to tune the hyperparameters using small validation sets to speed up the process. What accuracy can you reach?


10. Train an SVM regressor on the California housing dataset.

## References

- [Stat Quest - Part 1: Support Vector Machines](https://youtu.be/efR1C6CvhmE)
- [Stat Quest - Part 2: The Polynomial Kernel](https://www.youtube.com/watch?v=Toet3EiSFcM&t=0s)
- [Stat Quest - Part 3: The Radial (RBF) Kernel](https://www.youtube.com/watch?v=Qc5IyLW_hns&t=0s)
