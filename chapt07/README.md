# Chapter 8: Ensemble Learning and Random Forests

## Topics Covered

## Study Group Notebooks

## Book Questions

### Q1 If you have trained five different models on the exact same training data, and they all achieve 95% precision, is there any chance that you can combine these models to get better results? If so, how? If not, why?

Yes, by using voting system.

p273

Book Answer: p920

### Q2. What is the difference between hard and soft voting classifiers?

Hard Voting: Take majority vote in the classification
Soft Voting: Takes the probabilities instead. Average probability

"Hard voting is appropriate when the models used in the voting ensemble predict crisp class labels. Soft voting is appropriate when the models used in the voting ensemble predict the probability of class membership."


3. Is it possible to speed up training of a bagging ensemble by distributing it across multiple servers? What about pasting ensembles, boosting ensembles, Random Forests, or stacking ensembles?

Everything except boosting
Stacking can be but there is a dependency for the layer.


