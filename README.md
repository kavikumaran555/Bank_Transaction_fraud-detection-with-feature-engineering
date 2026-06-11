# Bank Fraud Detection ML

This project is about detecting fraud transactions using machine learning.

I used bank transaction dataset and tried to find patterns which can help identify fraud.

---

## Step 1: Loading data

Data was loaded using spark into dataframe.

![Loading Data](loading_table_into_dataframe_using_spark_in_python.PNG)

Also viewed data in Databricks using SQL.

![Dataset Preview](showing_imported_bank_transactions_dataset_in_databricks_notebook_using_sql.PNG)

---

## Step 2: Understanding patterns

I checked different columns to see if fraud has any pattern.

Some features showed weak patterns:

* age
* account type
* device type
* transaction type
* merchant category
* location

Examples:

![Age Pattern](showing_weak_pattern_from_fraudcount_and_fraudrate_by_age.PNG)

![Account Type](showing_weak_pattern_from_fraudcount_and_fraudrate_by_account_type.PNG)

![Device Type](showing_weak_pattern_from_fraudcount_and_fraudrate_by_device_type.PNG)

![Transaction Type](showing_weak_pattern_from_fraudcount_and_fraudrate_by_transaction_type.PNG)

![Merchant Category](showing_weak_pattern_from_fraudcount_and_fraudrate_by_transaction_merchant_category.PNG)

![Location Pattern](showing_weak_pattern_from_fraudcount_and_fraudrate_by_transaction_location.PNG)

There was one medium level pattern in transaction amount:

![Amount Pattern](showing_medium_strength_pattern_from_fraudcount_and_fraudrate_by_amount_category.PNG)

---

## Step 3: Feature Engineering

Created new columns to help model understand behavior better.

* high amount
* transaction hour
* night transaction flag
* customer transaction count
* average amount per customer
* difference from average

![Feature Engineering](creating_more_columns_from_feature_engineering_support_pattern_recognition.PNG)

---

## Step 4: Preparing data

Separated features and target variable.

![Feature Target Split](storing_Independant_and_dependant_columns_as_feature_and_target.PNG)

Then created train and test split and applied model.

![Model Training](creating_test_train_split_and_applying_random_forest_classifier_model.PNG)

---

## Step 5: Model evaluation

Used Random Forest model.

Accuracy was high but fraud detection was low because dataset is imbalanced.

![Model Results](checking_accuracy_score_and_classification_report_for_applied_model.PNG)

---

## Conclusion

* Most features had weak pattern
* Feature engineering helped create better signals
* Model accuracy is high but recall for fraud is low
* Need to handle imbalance better to improve results

---

## Future Improvement

* Handle class imbalance
* Try other models
* Improve feature engineering
* Focus more on fraud recall

---
