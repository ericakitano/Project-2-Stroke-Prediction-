# **Stroke Prediction**

## Using classification models to predict the occurrence of stroke in patients

 - **Author:** Erica Kitano

### Business problem:

Help doctors predict whether a patient is likely to get stroke based on parameters such as gender, age, various diseases, and smoking status.

### Data:
The original source of the data used is [Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset) from Kaggle.

### Methods
- Data cleaning:
  - checked for duplicates
  - checked and addressed missing values
  - checked and addressed unnecessary columns
  - checked for inconsistent and odd values
- Performed Exploratory Analysis to understand the statistics and correlation of each feature to the target
- Performed Explanatory Analysis to show the relationship between `age` vs `stroke`  and `work_type` vs `stroke`

### Results

#### ![image](https://github.com/ericakitano/Project-2-Stroke-Prediction-/assets/127703546/68c501d4-012c-4093-88e5-a49bcc81dfc5)


There is a trend that `stroke` is observed in people of older age. 

#### ![image](https://github.com/ericakitano/Project-2-Stroke-Prediction-/assets/127703546/4d557b4d-66a9-4fbf-9d6f-7f6d84198157)

There are no `stroke`s observed in children.

### Models
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Random Forest Classifier

### Other methodologies explored
- Tuning via GridSearchCV
- Principal Component Analysis (PCA)
- Boosting
- Decision Threshold
- Class Weight Balance
- Feature Engineering (For Future Improvement)

### Evaluation
- Accuracy
- F1 score
- Precision
- Recall
- ConfusionMatrix

### Final Recommendation
- Model Name: Tuned Logistic Regression (Balanced)
  - Parameters: C=0.01, penalty = l1, class_weight='balanced'
  - Recall score: **0.865** 
  - Accuracy score: **0.747**

This model is recommended because it has a balance of relatively high recall score and accuracy score. Having a high recall score is important because Type 2 errors (False Negatives) are more costlier for this dataset than Type 1 errors.

### Limitations

For this set of data, it is difficult to find a model that has both low Type 1 and low Type 2 errors. This can be explained from the observation that the features do not correlate well with the target. 

### For further information
For any additional questions, please contact ekitano1@gmail.com
