# Business Goal
To provide an accurate and safe model to implement on an individual or any list of patients in order to predict the weather or not a patient is at risk of having a stroke in the future.

# The Data
This project uses the a dataset found from [Kaggle.com.](https://www.kaggle.com/fedesoriano/stroke-prediction-dataset) The data set was posted by user 'fedesoriano'.

Here is a comprehensive list of the columns in this dataset and their corresponding meanings. The following list is directly copy/pasted from the original user's post.

1) id: unique identifier
2) gender: "Male", "Female" or "Other"
3) age: age of the patient
4) hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension
5) heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease
6) ever_married: "No" or "Yes"
7) work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
8) Residence_type: "Rural" or "Urban"
9) avg_glucose_level: average glucose level in blood
10) bmi: body mass index
11) smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*
12) stroke: 1 if the patient had a stroke or 0 if not
*Note: "Unknown" in smoking_status means that the information is unavailable for this patient

It should be noted that the origins of this dataset are unknown and this user has not shown proof of this dataset coming from a reliable source. However, it should be noted that weather this data is falsified or not, the model should still function properly and accurately should a verified dataset be provided.

# Cleaning the data
 - column 'id' was removed to prevent noise in the data.
 - columns 'gender', 'hypertension', 'heartDisease', 'everMarried', 'residenceType', and 'stroke' were modified to be a binary classifcation resulting in a 0 or 1 as the value
 - column 'bmi' had 201 records that were null and were filled in with a mean of all bmi values to prevent skewing the data and allowing the model to function properly. 

# Model 1: Testing different model types
This was a set of model's built in order to explore various model types to fit onto the data for the most accurate result.

RandomForestClassifier was selected as the winning model.

# Final Model (Model 2)
Final model was feature engineered to be as accurate as possible with minimal false negative (not at risk of a stroke) results, however this resulted in an overfitting of false positive (at risk of having a stroke). This was found to be acceptable as over predicting an a risk where none exists is safer than not predicting a risk often enough.

# Results
This model will essentially:

- Predict 74.8% if a patient will or will not be at risk of heart correctly.
- Only a minimal Aprox. 2.1% of patients predicted to be 'not at risk' will be misdiagnosed
- Model has been made to air on the side of caution and over predict risk as opposed to underpredict.