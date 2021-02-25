# NOTES: Applied Predictive Modeling

* Applied Predictive Modeling, 1st edition (2013)

## Introduction

* Definition of *predictive modeling*: the process of developing a mathematical tool or model that generates an accurate prediction

* Key points:
  * Primary goal of PM: generate accurate predictions
  * Secondary goals of PM: interpret the model and understand why it works
  * most PMs fundamentally influenced by a modeler with *expert knowledge* and context of the problem (i.e. data curation!)
  * PM is *not* a substitute for intuition, but rather a complement
  * The foundation of an effective PM is laid with *intuition* and *deep knowledge of the problem context*, which are entirely vital for driving decisions about model development.

* Why predictive models fail:
  1. inadequate preprocessing of data
  2. inadequate model validation
  3. unjustified extrapolation
  4. overfitting with existing data

* Book objectives:
  1. Foundational principles for building predictive models
  2. Intuitive explanations of many commonly used predictive modeling methods for both classification and regression problems
  3. Principles and steps for validating a predictive model
  4. Computer code to perform the necessary foundational work to build and validate predictive models

* Key ingredients of predictive models
  1. intuition and deep knowledge of the problem context
  2. relevant data
  3. a versatile computational toolbox (with techniques for data preprocessing, visualization, modeling)

* Great summary section on terminology in predictive modeling (p.6)

* Four parts of the book:
  1. General Strategies
  2. Regression Models
  3. Classification Models
  4. Other Considerations

## Part I: General Strategies

* TODO

## Chapter 4: Over-fitting and Model Tuning

### The Problem of Over-Fitting

### Model Tuning

### Data Splitting

### Resampling Techniques

#### k-Fold Cross-Validation

* Cross-validation = a method for evaluating the quality of a statistical model by splitting the original dataset into test and training subsets
* k-fold cross-validation = the original sample is randomly partitioned into k equal sized subsamples; k-fold cross-validation = the original sample is randomly partitioned into k equal sized subsamples; 1 subsample is then used to test while the other k-1 subsamples are used to train (non-exhaustive form of CV so less computationally intensive) (see p.69)
  * when k = n (where n = total number of samples) --> leave-one-out cross validation (LOOCV)
* For a nice review of cross-validation, see this link: https://robjhyndman.com/hyndsight/crossvalidation/
