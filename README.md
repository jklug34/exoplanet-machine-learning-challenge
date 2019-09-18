# exoplanet-machine-learning-challenge
Creation of a machine learning models to best classify candidate exoplanets from NASA's Kepler space telescope


#### Link to raw data
https://www.kaggle.com/nasa/kepler-exoplanet-search-results


#### List of Column Descriptions
#### https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html


### Evaluated 5 Models
- Logistic Regression Model
- Random Forest Classifier
- Decision Tree Classifier
- K- Nearest Neighbors (KNN) Classifier
- Support Vector Machines (SVM) Classifier

## The best model after hypertuning parameter was the Random Forest Classifier

- All models were better at predicting False Positives than Confirmed or Canidate Exoplanets



#### Confusion Matrix

|        |      |            Predicted             |
| :----: |:----:|   :----:        |   :----:       |
|        |      |         0       |       1        |
|        | 0    | True Negative   | False Positive |
| Actual | 1    | False Negative  | True Positive  |


Precision = This is the rate of values that measures the accuracy of positive predictions. So when we divide True Positives, by total positives, we get the precision value
Recall = This is the rate of values that measures positive instances that were correctly identified by the classifier. It is also called sensitivity, or the true positive rate. Thus recall is (True Positive)/(True Positive+False Negative)
F1 Score = It is the harmonic mean of precision and recall  2/(1/precision + (1/recall)
Support = Number of data points



## Logistic Regression Model

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


## Random Forest Classifier

- Best Testing Score (r2) = 0.88501
- With Hypertuning (r2) = 0.89624

|               | precision  |  recall |  f1-score |  support |
|    :----:     |  :----:    |  :----: |   :----:  |  :----:  |
|     CANDIDATE |   0.84     |   0.80  |    0.82   |    422   |
|     CONFIRMED |   0.82     |   0.84  |    0.83   |    450   |
|FALSE POSITIVE |   0.99     |   1.00  |    0.99   |    876   |
|               |            |         |           |          |
|     micro avg |   0.91     |   0.91  |   0.91    |   1748   |
|     macro avg |   0.88     |   0.88  |   0.88    |   1748   |
|  weighted avg |   0.91     |   0.91  |   0.91    |   1748   |


Top Five Feature Importance Ranking

| Feature Importance (r2) |     Feature Name        |
|         :----:          |        :----:           |
|0.13705110593371891      | transit_signal_to_noise |
|0.13481467581039355      | not_transit_like_flag   |
|0.13084184032135046      | centroid_offset_flag    |
|0.10441113201541898      | stellar_eclipse_flag    |
|0.08379134255359354      | planetary_radius        |



## Decision Tree Classifier

- Best Testing Score (r2) = 0.83139
- With Hypertuning (r2) = 0.85183

|               | precision  |  recall |  f1-score |  support |
|    :----:     |  :----:    |  :----: |   :----:  |  :----:  |
|     CANDIDATE |   0.75     |   0.71  |    0.73   |    422   |
|     CONFIRMED |   0.75     |   0.75  |    0.75   |    450   |
|FALSE POSITIVE |   0.99     |   0.97  |    0.98   |    876   |
|               |            |         |           |          |
|     micro avg |   0.87     |   0.85  |    0.86   |   1748   |
|     macro avg |   0.83     |   0.81  |    0.82   |   1748   |
|  weighted avg |   0.87     |   0.85  |    0.86   |   1748   |
|   samples avg |   0.85     |   0.85  |    0.85   |   1748   |

Top Five Feature Importance Ranking

| Feature Importance (r2) |     Feature Name        |
|         :----:          |        :----:           |
|0.1850671657800496       | not_transit_like_flag   |
|0.18451426519832592      | centroid_offset_flag    |
|0.1777361275931974       | stellar_eclipse_flag    |
|0.1540030292664817       | transit_signal_to_noise |
|0.04854855579725562      | impact_parameter        |



## K- Nearest Neighbors (KNN) Classifier

- Best Testing Score (r2) = 0.82910
- With Hypertuning (r2) = 0.82977

|               | precision  |  recall |  f1-score |  support |
|    :----:     |  :----:    |  :----: |   :----:  |  :----:  |
|     CANDIDATE |   0.68     |   0.58  |    0.63   |    422   |
|     CONFIRMED |   0.65     |   0.72  |    0.68   |    450   |
|FALSE POSITIVE |   0.99     |   1.00  |    0.99   |    876   |
|               |            |         |           |          |
|     micro avg |   0.83     |   0.83  |    0.83   |   1748   |
|     macro avg |   0.77     |   0.77  |    0.77   |   1748   |
|  weighted avg |   0.83     |   0.83  |    0.82   |   1748   |


## Support Vector Machines (SVM) Classifier

- Best Testing Score (r2) = 0.79291
- With Hypertuning (r2) = 0.80373

|               | precision  |  recall |  f1-score |  support |
|    :----:     |  :----:    |  :----: |   :----:  |  :----:  |
|     CANDIDATE |   0.76     |   0.43  |    0.55   |    422   |
|     CONFIRMED |   0.62     |   0.86  |    0.72   |    450   |
|FALSE POSITIVE |   0.99     |   1.00  |    0.99   |    876   |
|               |            |         |           |          |
|     micro avg |   0.82     |   0.82  |    0.82   |   1748   |
|     macro avg |   0.79     |   0.76  |    0.75   |   1748   |
|  weighted avg |   0.84     |   0.82  |    0.81   |   1748   |

















