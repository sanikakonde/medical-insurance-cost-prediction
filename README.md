# Medical Insurance Cost Prediction

This project uses Machine Learning to predict medical insurance premium costs based on personal and health-related information.

The main goal of this project is to understand how different regression models perform on the same dataset and to select a suitable model for predicting insurance costs.

## Dataset

The dataset used in this project is the **Medical Insurance Premium Prediction** dataset from Kaggle.

Dataset Link:
https://www.kaggle.com/datasets/tejashvi14/medical-insurance-premium-prediction

The dataset contains 986 rows and 11 columns.

## Project Objective

The objective of this project is to:

- Understand and explore the dataset
- Handle missing values and categorical data
- Perform basic data preprocessing
- Train different regression models
- Compare the performance of the models
- Use Cross-Validation for a more reliable comparison
- Tune the Random Forest model using GridSearchCV
- Evaluate the final model on unseen test data

## Features in the Dataset

The dataset contains the following columns:

| Column | Meaning |
|--------|---------|
| Age | Age of the insured person |
| Diabetes | Whether the person has diabetes |
| BloodPressureProblems | Whether the person has blood pressure problems |
| AnyTransplants | Whether the person has undergone any transplant |
| AnyChronicDiseases | Whether the person has any chronic disease |
| Height | Height of the person |
| Weight | Weight of the person |
| KnownAllergies | Whether the person has known allergies |
| HistoryOfCancerInFamily | Whether there is a history of cancer in the family |
| NumberOfMajorSurgeries | Number of major surgeries undergone |
| PremiumPrice | Medical insurance premium amount |

`PremiumPrice` is the target variable that we are trying to predict.

## Tools and Libraries Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Kaggle Notebook

## Project Workflow

The project follows these main steps:

1. Import the required libraries
2. Load the dataset
3. Understand the dataset
4. Check data types
5. Check missing values
6. Check duplicate records
7. Perform exploratory data analysis
8. Prepare the features and target variable
9. Split the data into training and testing sets
10. Preprocess numerical and categorical features
11. Train different regression models
12. Compare model performance
13. Apply 5-fold Cross-Validation
14. Tune the Random Forest model using GridSearchCV
15. Train the final Random Forest model using the best parameters
16. Evaluate the final model on the test data

## Machine Learning Models Used

The following regression models were compared:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest Regressor
- Gradient Boosting Regressor

The models were evaluated using:

- RMSE (Root Mean Squared Error)
- MAE (Mean Absolute Error)
- R² Score

## Cross-Validation

5-fold Cross-Validation was used to compare the models more reliably.

Instead of evaluating a model using only one train-test split, the training data is divided into 5 parts. The model is trained and evaluated multiple times using different parts as validation data.

This helps us understand how consistently a model performs on different subsets of the training data.

## Hyperparameter Tuning

After comparing the models, Random Forest was further tuned using `GridSearchCV`.

Different combinations of Random Forest parameters were tested to find a combination that gives a lower Cross-Validation RMSE.

The selected parameters were:

- `n_estimators = 300`
- `max_depth = None`
- `max_features = 1.0`
- `min_samples_leaf = 2`
- `min_samples_split = 5`

The tuned Random Forest model was then trained and evaluated on the test data.

## Final Model Results

The tuned Random Forest model achieved the following results on the test data:

- **RMSE:** 2052.84
- **MAE:** 955.82
- **MSE:** 4,214,143.37
- **R² Score:** 0.9012

The R² score of approximately **0.90** means that the final model explains about **90.1% of the variation in the test-set insurance premium values**.

## Conclusion

This project helped me understand the complete workflow of a regression-based Machine Learning project.

I worked with data preprocessing, exploratory data analysis, multiple regression algorithms, model evaluation, Cross-Validation, and hyperparameter tuning.

The final tuned Random Forest model provided an R² score of approximately 0.90 on the test data, showing that the model was able to explain a large portion of the variation in the insurance premium values in this test set.

## Project Files

```text
medical-insurance-cost-prediction/
│
├── README.md
└── medical-insurance-cost-prediction.ipynb
