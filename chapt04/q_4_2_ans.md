# Q4.2 Suppose the features in your training set have very different scales. Which algorithms might suffer from this, and how? What can you do about it?

SGD, Minibatch, Batch might have problems

Use Scaling

## MinMax Scaling

(x - Min) / (Range=Max - Min) # Results [0..1]

## Standardization

(x-mean) / sigma  # Good when we have outliers
