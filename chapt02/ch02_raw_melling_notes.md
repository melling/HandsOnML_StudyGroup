# Kaggle NYC Hands On ML Python Notes

Taraqur, Lisa, and I have started study for an hour a week.
First part of Chapter 2


https://github.com/ageron/handson-ml2

https://raw.githubusercontent.com/ageron/handson-ml2/master/datasets/housing/housing.csv



Chapter 2: End-to-End Machine Learning Project

30,000 foot view

## California House Prices

Insert Figure 2-1 Here.

Organized by Block Groups:

- Population
- Median income
- Median house price

Target: Which Block Groups in which to invest.

This is Supervise Learning because we have labels (the answers)

- Multiple Regression
- Univarate
- Batch Processing - All the data.

Performance Measure: RMSE - preferred if there are few outliers
p42

Attributes:
longitude, latitude, housing_median_age, total_rooms, total_bed rooms, population, households, median_income,  and ocean_proximity.

median_house_value - label
Rest are features

## Downloads data on pg49

 20,640 instances in the dataset/ rows

 

## Histogram Observations: (p53)

[Insert Histogram Pic]

Show a Gaussian Normal Curve

- many histograms are tail heavy
- transforming these attributes

## Create a Test Data Set p54

Discusses how to create a separate set of data validate model.

 **stratified sampling** p56

population is divided into homogeneous subgroups called strata

It is important to have a sufficient number of instances in your dataset for each stratum, or else the estimate of the stratum’s importance may be biased. This means that you should not have too many strata, and each stratum should be large enough. The following code uses the pd.cut() function to create an income category attribute

StratifiedShuffleSplit - scikit learn handles it

## EDA p58

Uses lots of visualizations

[Insert Figure 2-11]
[Insert Figure 2-12]
[Insert Figure 2-13]

The radius of each circle represents the district’s population (option s), and the color represents the price (option c)

### Looking for Correlations

corr_matrix["median_house_value"].sort_values(ascending=False) median_house_value 1.000000
median_income 0.687170

p62

total_rooms 0.135231
    housing_median_age    0.114220
    households
    total_bedrooms
    population
    longitude
    latitude

coefficients close to zero mean that there is no linear correlation

### Scatter Plots

[Insert 2-15 Scatter Plots]

The main diagonal (top left to bottom right) would be full of straight lines if Pandas plotted each variable against itself, which would not be very useful. So instead Pandas displays a histogram of each attribute

The author zooms

Figure 2-16. Median income versus median house value

the correlation is indeed very strong; you can clearly see the upward trend and the points are not too dispersed. Second, the price cap that we noticed earlier is clearly visible as a horizontal line at $500,000. But this plot reveals other less obvious straight lines: a horizontal line around $450,000, another around $350,000, perhaps one around $280,000, and a few more below that. You may want to try removing the corresponding districts to prevent your algorithms from learning to reproduce these data quirks.

## Building a Model

Next Session Taraqur will NOT present!!!

## Prepare the Data for Machine Learning Algorithms

p66

Remove Label from Training so it's not used as feature?

    housing = strat_train_set.drop("median_house_value", axis=1)

    housing_labels = strat_train_set["median_house_value"].copy()

## Data Cleaning

Dropping rows with no data

1) Get rid of the corresponding districts.
2) Get rid of the whole attribute.
3) Set the values to some value (zero, the mean, the median, etc.).

housing.dropna(subset=["total_bedrooms"]) # option 1
housing.drop("total_bedrooms", axis=1) # option 2

median = housing["total_bedrooms"].median() # option 3
ohousing["total_bedrooms"].fillna(median, inplace=True)

### Impute Numerical
scikit learn

from sklearn.impute import SimpleImputer

imputer = SimpleImputer(strategy="median") # Specify method e.g. "median" / mean

p68
Consistent Interface 
Estimators
Transformers
Predictors

### Handling Text and Categorical Attributes

Encode into numbers

 from sklearn.preprocessing import OrdinalEncoder 
 >>> ordinal_encoder = OrdinalEncoder()

one-hot encoding - one method

only one attribute will be equal to 1 (hot), while the others will be 0 (cold)

Use sparse matrix

Embeddings

see Chapter 13

## Custom Transformers

### Feature Scaling

One of the most important transformations you need to apply to your data is feature scaling. With few exceptions, Machine Learning algorithms don’t perform well when the input numerical attributes have very different scales

1) Min-max scaling (many people call this normalization)

2) Standardization is quite different: first it subtracts the mean value (so standardized values always have a zero mean), and then it divides by the standard deviation so that the resulting distribution has unit variance.

Unlike min-max scaling, standardization does not bound values to a specific range, which may be a problem for some algorithms (e.g., neural networks often expect an input value ranging from 0 to 1). However, standardization is much less affected by outliers

## Transformation Pipelines

```python
from sklearn.pipeline import Pipeline
from sklearn.preprocessing import StandardScaler
    num_pipeline = Pipeline([
            ('imputer', SimpleImputer(strategy="median")),
            ('attribs_adder', CombinedAttributesAdder()),
            ('std_scaler', StandardScaler()),
        ])
    housing_num_tr = num_pipeline.fit_transform(housing_num)
```

Combines to get a ColumnTransformer

## Select and Train a Model

p75

Fit a model in a few lines of code

## Fit a Model
```
from sklearn.linear_model import LinearRegression 

lin_reg = LinearRegression()
lin_reg.fit(housing_prepared, housing_labels)
```

## Predict with Model

```python
from sklearn.metrics import mean_squared_error
housing_predictions = lin_reg.predict(housing_prepared)
lin_mse = mean_squared_error(housing_labels, housing_predictions) 
lin_rmse = np.sqrt(lin_mse)
lin_rmse
```

Simple change to do a Tree Model

```python
from sklearn.tree import DecisionTreeRegressor 
tree_reg = DecisionTreeRegressor()
tree_reg.fit(housing_prepared, housing_labels)
```

```python
housing_predictions = tree_reg.predict(housing_prepared)
tree_mse = mean_squared_error(housing_labels, housing_predictions) >>> tree_rmse = np.sqrt(tree_mse)
tree_rmse
```

### Evaluation Using Cross-Validation

For more information see the Chapter 5 ISLR Blog by fellow cult member Taraqur

Scikit-Learn’s K-fold cross-validation feature

```python
from sklearn.ensemble import RandomForestRegressor 
forest_reg = RandomForestRegressor()
forest_reg.fit(housing_prepared, housing_labels) 
>>> [...]
forest_rmse
```

Grid Search

>>> feature_importances = grid_search.best_estimator_.feature_importances_
with RandomForestRegressor can indicate the relative importance of each attribute for making accurate predictions:


Randomized Search

https://www.kaggle.com/dansbecker/shap-values

