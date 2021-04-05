# Business Goal
To provide an accurate and safe model to implement on an individual or any list of patients in order to predict the weather or not a patient is at risk of having a stroke in the future.

# The Data
This project uses the a dataset found from [Kaggle.com.](https://www.kaggle.com/fedesoriano/stroke-prediction-dataset) The data set was posted by user 'fedesoriano'.

It should be noted that the origins of this dataset are unknown and this user has not shown proof of this dataset coming from a reliable source. However, it should be noted that weather this data is falsified or not, the model should still function properly and accurately should a verified dataset be provided.

# Cleaning the data
 - column 'id' was removed to prevent noise in the data.
 - columns 'gender', 'hypertension', 'heartDisease', 'everMarried', 'residenceType', and 'stroke' were modified to be a binary classifcation resulting in a 0 or 1 as the value
 - column 'bmi' had 201 records that were null and were filled in with a mean of all bmi values to prevent skewing the data and allowing the model to function properly. 

# sTEP 1: Testing different model types
This was a set of model's built in order to explore various model types to fit onto the data for the most accurate result.

RandomForestClassifier was selected as the winning model.

# Final Model (Model 1)
Final model was feature engineered to be as accurate as possible with minimal false negative (not at risk of a stroke) results, however this resulted in an overfitting of false positive (at risk of having a stroke). This was found to be acceptable as over predicting an a risk where none exists is safer than not predicting a risk often enough.

# Results
This model will essentially:

- Predict 74.8% if a patient will or will not be at risk of heart correctly.
- Only a minimal Aprox. 2.1% of patients predicted to be 'not at risk' will be misdiagnosed
- Model has been made to air on the side of caution and over predict risk as opposed to underpredict.