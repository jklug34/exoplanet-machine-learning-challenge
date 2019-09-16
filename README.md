# exoplanet-machine-learning-challenge
Creation of a machine learning models to best classify candidate exoplanets from NASA's Kepler space telescope

### Logistic Regression Model

- Best Testing Score (r2) = 0.81464
- With Hypertuning (r2) = 0.816517

|               | precision  |  recall  | f1-score | support |
|    :----:     |    :----:  |  :----:  |  :----:  |  :----: |
|     CANDIDATE |      0.71  |    0.56  |    0.62  |     422 |
|     CONFIRMED |      0.65  |    0.77  |    0.71  |     450 |
|FALSE POSITIVE |      0.99  |    1.00  |    0.99  |     876 |
|               |            |          |          |         |
|     micro avg |      0.83  |    0.83  |    0.83  |    1748 |
|     macro avg |      0.78  |    0.77  |    0.77  |    1748 |
|  weighted avg |      0.83  |    0.83  |    0.83  |    1748 |


### Random Forest Classifier

- Best Testing Score (r2) = 0.89244
- With Hypertuning (r2) = 0.89585

                precision    recall  f1-score   support

     CANDIDATE       0.84      0.80      0.82       422
     CONFIRMED       0.82      0.84      0.83       450
FALSE POSITIVE       0.99      1.00      0.99       876

     micro avg       0.91      0.91      0.91      1748
     macro avg       0.88      0.88      0.88      1748
  weighted avg       0.91      0.91      0.91      1748


### Decision Tree Classifier

- Best Testing Score (r2) = 0.84839
- With Hypertuning (r2) =


### K- Nearest Neighbors (KNN) Classifier

- Best Testing Score (r2) = 0.83009
- With Hypertuning (r2) =


### Support Vector Machines (SVM) Classifier

- Best Testing Score (r2) = 0.79291
- With Hypertuning (r2) =

















