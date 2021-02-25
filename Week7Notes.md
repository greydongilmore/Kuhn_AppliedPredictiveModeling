## Chapter 20: Factors That Can Affect Model Performance

* Type III errors: i.e. developing a model that answers the wrong question
* Three general forms of noise/error in predictors
  1. systematic noise associated with the measurement system
  2. inclusion of non-informative predictors
  3. systematic noise associated with the *outcome* measure (i.e. response variable)
    e.g. if categorical outcome measure mislabeled 10% of time; unlikely model can do better than 90%

### 20.1 Type III Errors

* i.e. developing a model that answers the wrong question
* suggestion: very important to focus on the overall strategy of the problem at hand and not just the technical tactics of the potential solution

### 20.2 Measurement Error in the Outcome

* recall residual error (epsilon) from linear regression model
* lowest possible error obtainable would be *irreducible* error; however often inflated by *model* error (since true model unknown)
* measurement noise in outcome also important component of irreducible error (Fig. 20.1 and Fig. 20.2 below)
  * ceiling effect for model performance
  
  ![Fig.20.1.](https://github.com/jclauneuro/Kuhn_AppliedPredictiveModeling/blob/master/figures/Fig20.01.png)
  ![Fig.20.2.](https://github.com/jclauneuro/Kuhn_AppliedPredictiveModeling/blob/master/figures/Fig20.02.png)

### 20.3 Measurement Error in the Predictors

* noise in predictors affects model (Fig. 20.3)

![Fig.20.3.](https://github.com/jclauneuro/Kuhn_AppliedPredictiveModeling/blob/master/figures/Fig20.03.png)

### 20.4 Discretizing Continuous Outcomes

* can be desirable to work with a categorical response even if original data is continuous scale
* if continuous variable is bimodal, categorizing appropriate
* if unimodal, induces a loss of information (Fig.20.6 below)

![Fig.20.6.](https://github.com/jclauneuro/Kuhn_AppliedPredictiveModeling/blob/master/figures/Fig20.06.png)

* A second common reason: continuous response contains a high degree of error, so much so that only the response values in either extreme of the distribution are likely to be correctly categorized
  * the data can be partitioned into three categories, where data in either extreme are classified generically as positive and negative, while the data in the midrange are classified as unknown or indeterminate.

### 20.5 When Should You Trust Your Model's Prediction?

* the predictive modeling process assumes that the underlying mechanism that generated the existing data for the predictors and the response will continue to generate data from the *same mechanism*
* ask yourself whether this holds for new datasets
* defn extrapolation: using a model to predict samples that are outside the range of the training data
* Hastie2008: approach for quantifying likelihood that new sample is member of the training data:
```
1. Compute the variable importance for the original model and identify the top 20 predictors
2. Randomly permute these predictors from the training set
3. Row-wise concatenate the original training set’s top predictors and the randomly permuted version of these predictors
4. Create a classification vector that identifies the rows of the original training set and the rows of the permuted training set
5. Train a classification model on the newly created data
6. Use the classification model to predict the probability of new data being in the class of the training set.
```

### 20.6 The Impact of a Large Sample

* often assumed that the more datasets we have, the better model we can produce
* however, noise in the data may minimize any advantages brought by an increase in sample size
* also increases computational burden
