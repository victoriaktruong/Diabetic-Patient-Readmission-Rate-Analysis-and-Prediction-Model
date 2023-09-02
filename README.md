# Predictive Modeling of Hospital Readmission Rates 

## Background



## Dataset 

The dataset, originally sourced from a research paper by [Strack et al.][1] in 2014 and made available on the [UC Irvine Machine Learning Repository][2], was retrieved from [Kaggle][3]. This dataset represents a comprehensive overview of a decade's worth of clinical care spanning the years 1999 to 2008, encompassing 130 U.S. hospitals and integrated delivery networks. It's worth noting that the Kaggle dataset represents a subset, containing ~25,000 encounters, which is one-fourth of the original dataset available on the UC Irvine Machine Learning Repository, comprising a total of ~100,000 encounters.

[1]: https://www.hindawi.com/journals/bmri/2014/781670/
[2]: https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008
[3]: https://www.kaggle.com/datasets/dubradave/hospital-readmissions

### Variables 
The table below shows the variables used for analysis:

| Variable            | Description                                                   |
|---------------------|---------------------------------------------------------------|
| age                 | Patient's age group                                           |
| time_in_hospital    | Length of hospital stay (1 to 14 days)                       |
| n_procedures        | Number of procedures during the hospitalization              |
| n_lab_procedures    | Number of laboratory procedures during the hospitalization   |
| n_medications       | Number of medications administered during the stay            |
| n_outpatient        | Number of outpatient visits in the year prior to admission   |
| n_inpatient         | Number of inpatient visits in the year prior to admission    |
| n_emergency         | Number of emergency room visits in the year prior to admission |
| medical_specialty   | Admitting physician's medical specialty                       |
| diag_1              | Primary diagnosis category (e.g., Circulatory, Respiratory)   |
| diag_2              | Secondary diagnosis category                                  |
| diag_3              | Additional secondary diagnosis category                       |
| glucose_test        | Glucose serum test result (High, Normal, Not performed)       |
| A1Ctest             | A1C level result (High, Normal, Not performed)                |
| change              | Change in diabetes medication (Yes, No)                       |
| diabetes_med        | Prescription of diabetes medication (Yes, No)                |
| readmitted          | Hospital readmission (Yes, No)                                |


## Methodology

**Section 1: Data Preprocessing:** Data preprocessing serves as the foundation for insightful analysis. Beginning with library imports and dataset loading, data integrity is prioritized by addressing missing values. The conversion of categorical variables like 'glucose_test' and 'A1Ctest' into binary representations simplifies complexities.The dataset is further enhanced by converting 'age' ranges into numerical values. Meanwhile, label encoding preserves essential information for medical specialties and diagnoses, ensuring compatibility with machine learning models. Thoughtful column reordering improves clarity and paves the way for robust analyses. 

**Section 2: Create a Logistic Regression to Predict Hospital Readmittance:** This section focuses on preparing the dataset for a logistic regression model to predict hospital readmittance. The steps include loading preprocessed data, extracting the 'readmitted' column as the target variable, and verifying dataset balance (47% readmission rate). 20 input features are selected, encompassing patient demographics, medical procedures, and diagnostic codes. Standardization ensures feature consistency, an essential aspect for a reliable model.

**Section 3: Data Splitting into Train and Test Sets with Shuffling:** The split ratio is 80% for training (20,000 samples) and 20% for testing (5,000 samples), ensuring that the logistic regression model is properly validated.

**Section 4: Logistic Regression Model:** The logistic regression model is created and trained to predict hospital readmission. The model's performance on the training data is assessed, and the coefficients are interpreted to understand the impact of different features. Following this, the data is preprocessed by splitting it into training, validation, and test sets and scaling the inputs. A neural network model with multiple hidden layers is then defined and compiled. The model is trained with tuned hyperparameters, and its performance is evaluated on the test data. This process involves data scaling, dataset creation, data splitting, neural network model definition, and training with hyperparameter tuning. The final model achieves an accuracy of 61.78% on the test data, demonstrating its predictive capability for hospital readmission.

## Conclusion

