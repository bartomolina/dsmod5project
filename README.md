# Flatiron Data Science Bootcamp - Module 5 Final Project

* Student name: **Barto Molina**
* Student pace: **part time**
* Scheduled project review date/time: **01/16/2020 2:00 PM (EST)**
* Instructor name: **Victor Geislinger**
* Blog post URL: []()

## Deliverables

- Kaggle Notebooks
- [Presentation](presentation.pdf)
- Blog post: []()
- [Video walkthrough]()

---

## 1. Introduction

In this project, we're going to create, test and compare different machine learning classifiers. For this, we're going to use a dataset from a Kaggle competition from the Banco Santander which aims to predict whether a customer is satisfied or not based on different features.

## 2. The dataset

We're going to use a dataset form this Kaggle competition: [Santander Customer Satisfaction](https://www.kaggle.com/c/santander-customer-satisfaction). This dataset consist in 369 features and 76020 instances. The features are all numerical (some of them are categorical - one hot encoded) and the competition doesn't provide a definition, so we'll need to do some digging in order to figure out the meaning of each of them. Our TARGET variable is either 0 (customer satisfied) or 1 (not satisfied).

## 3. Methodology

In order to make it easier to work with the different notebooks, we're going to divide the different phases of the process in different notebooks:

1. [Feature exploration and dataset preparation](https://www.kaggle.com/bartomolina/feature-exploration-and-dataset-preparation): We'll explore the dataset and look at some of the most important features with the help of some of the notebooks in Kaggle, data cleaning, remove unused features, replace null values and outliers, standarize.
2. [Resampling](https://www.kaggle.com/bartomolina/resampling): As our data is highly unbalanced, we will try some resampling techniques to get a more balanced dataset between the two classes.
3. [PCA](https://www.kaggle.com/bartomolina/pca-principal-component-analysis): Given the high-dimensional nature of our dataset, we're going to try reducing some of the features using PCA.
4. [Decision Tree and Random Forest](https://www.kaggle.com/bartomolina/decision-tree-and-random-forest): We're going to try this models using different inputs and perform hyperparameter tuning.
5. [XGBoost](https://www.kaggle.com/bartomolina/xgboost): As with the Random Forest, we're going to experiment with different inputs and hyperparameters.

## 4. Conclusions

These are the main challenges we've faced during the project:

- Lack of a feature dictionary: We've had to rely on information from other notebooks in Kaggle and spend some time during the feature exploration phase in order to figure out the meaning for each of the features.
- Number of features: Working with high dimensional data may cause some problems. In this case, while working with machine learning algorithms, it may increase the time needed to fit the classifiers.
- Unbalanced dataset: Less than 4% of the dataset correspond to unsatisfied customers.

From these, the last one has been the most problematic. Unbalanced data may result in classifiers with a very high accuracy just because they classify everything as the majority class. We've explored diffent techniques (i.e. downsampling), but still we couldn't avoid having most of our classifiers predicting the majority class in most cases.

## 5. Future work

- As mentioned in the point before, more work needs to be done to fix the issues caused by the unbalanced data, like exploring additional sampling techniques or fine tununing the classifiers hyperparameters.
- Try additional machine learning algorithms (AdaBoost, SVM).
- Use pipelines to help streamline the machine learning process.