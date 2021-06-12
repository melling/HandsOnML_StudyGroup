# Chapter 7: Ensemble Learning and Random Forests

## Misc References

- [Author's Jupyter Notebook](https://github.com/ageron/handson-ml2/blob/master/07_ensemble_learning_and_random_forests.ipynb)
- [StatQuest - Random Forests: Part 1](https://youtu.be/J4Wdy0Wc_xQ)
- [StatQuest - Random Forests: Part 2](https://youtu.be/sQ870aTKqiM)
- [StatQuest - AdaBoost](https://youtu.be/LsK-xG1cLYA)

## Topics Covered

- Voting Classifiers
  - Soft Voting
  - Hard Voting
- Bagging and Pasting
- Out-of-Bag Evaluation
- Random Patches and Random Subspaces
- Random Forests
  - Feature Importance
- Boosting
  - AdaBoost
  - Gradient Boosting
- Stacking

## Study Group Notebooks

## Book Questions

### Q7.1 If you have trained five different models on the exact same training data, and they all achieve 95% precision, is there any chance that you can combine these models to get better results? If so, how? If not, why?

[Answer](q_7_1_ans.md)

***

### Q7.2 What is the difference between hard and soft voting classifiers?

[Answer](q_7_2_ans.md)

***

### Q7.3. Is it possible to speed up training of a bagging ensemble by distributing it across multiple servers? What about pasting ensembles, boosting ensembles, Random Forests, or stacking ensembles?

[Answer](q_7_3_ans.md)

***

### Q7.4 What is the benefit of out-of-bag evaluation?

***

### Q7.5 What makes Extra-Trees more random than regular Random Forests? How can this extra randomness help? Are Extra-Trees slower or faster than regular Random Forests?

***

### Q7.6 If your AdaBoost ensemble underfits the training data, which hyperparameters should you tweak and how?

***

### Q7.7 If your Gradient Boosting ensemble overfits the training set, should you increase or decrease the learning rate?
