# Machine Learning - Exoplanet Exploration

![exoplanets.jpg](Images/exoplanets.jpg)


## Background:

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

In this project, I created two machine learning models capable of classifying candidate exoplanets from the raw dataset.


## Project outline:
---
### Processes

1. Preprocess the raw data
2. Tune the models
3. Compare two or more models

### Preprocess the Data

* Preprocess the dataset prior to fitting the model.
* Perform feature selection and remove unnecessary features.
* Use MinMaxScaler to scale the numerical data.
* Separate the data into training and testing data.

### Tune Model Parameters

* Use GridSearch to tune model parameters.
* Tune and compare two different classifiers (Random Forest Classifier and Support Vector Machine).


## Report and outcome:
---
Both Random Forest and Support Vector Machine (SVM) models had high accuracy scores of train and test data before tuning the models. Although the SVM model yeilded 0.83731 and 0.85584 acuray scores on the train and test data, the Random Forest model had higher accuracy scores (train: 0.99466 and test: 0.899474) than the SVM model.

After tuning hyperparameters using Gridsearch, the Random Forest model still performed better (train: 1.0 and test: 0.91018) than the SVM model (train: 0.87126 and test: 0.088387)


### Random Forest:
| Score | Before GridSearch | After GridSearch |
| :---: | :---: | :---: |
| Train score | 0.99466 | 1.0 |
| Test score | 0.89474 | 0.91018 |

### Support Vector Machine:
| Score | Before GridSearch | After GridSearch |
| :---: | :---: | :---: |
| Train data score | 0.83731 | 0.87126 |
| Test data score | 0.85584 | 0.88387 |


The Classification Reports showed that even if the SVM had higher scores on the precision of CANDIDATE (0.88) and the recall of CONFIRMED (0.91), overall the scores of Random Forest model were better than the scores of SVM model.

(Precison: Accuracy of positive predictions, Recall: Fraction of positives that were correctly identified, F1 score: percentage of positive predictions that were correct)

### Random Forest:
|  | precision | recall | f1-score |
| :---: | :---: | :---: | :---: |
| CANDIDATE | 0.84 | 0.77 | 0.80 |
| CONFIRMED | 0.81 | 0.86 | 0.84 |
| FALSE POSITIVE | 0.99 | 1.00 | 0.99 |

### Support Vector Machine:
|  | precision | recall | f1-score |
| :---: | :---: | :---: | :---: |
| CANDIDATE | 0.88 | 0.60 | 0.71 |
| CONFIRMED | 0.71 | 0.91 | 0.80 |
| FALSE POSITIVE | 0.99 | 1.00 | 0.99 |

The Random Forest model was more accurate, effective and capable in classifying candidate exoplanets based on the results above.

---
## Technology used:
* Python, Scikit-learn
