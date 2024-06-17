# shreyas_Datahack

# Summer Analytics Hackathon - 2024

The final submission is `submission.csv`.

The procedure followed is as follows:
- Load the datasets into `train_set`, `test_set` and `train_labels`.
- Preprocess the data by removing the `ID` column and dummy encoding the necessary columns.
- The columns `health_insurance`, `employment_occupation`, `employment_industry` had 45-55% missing values. So, they were dropped to avoid incorrect imputation.
- `race`, `marital_status` and `rent_or_own` were dropped as they contribute little to none to the probability of a person getting a `vaccine`
- The remaining columns were imputed by:
  - `median` for numerical columns(to avoid outliers)
  - `mode` for categorical columns
- The model used was a Logistic Regression model.
- The model was trained on the training set by dividing it into `train` and `validation` sets.
- The model was then used to predict the `test_set`.
- The predictions were saved in `submission.csv`.
