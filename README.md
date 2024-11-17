# Bank Marketing Campaign Prediction

This project develops a predictive model using AdaBoost with a Decision Tree Classifier to determine whether a customer will respond positively to a bank's marketing campaign. The model is trained and evaluated on the publicly available **Bank Marketing Dataset**.

## Dataset

The dataset used in this project is sourced from Kaggle and can be found at the following link: [Kaggle](https://www.kaggle.com/datasets/henriqueyamahata/bank-marketing).

### Dataset Description

The dataset contains data from a direct marketing campaign by a Portuguese bank. Each row represents a customer contacted during the campaign, with features describing their demographic and financial status, as well as details of the contact.

### Dataset Highlights

The dataset consists of the following columns:
- **age**: Customer's age.
- **job**: Employment type.
- **marital**: Marital status.
- **education**: Level of education.
- **default**: Credit default status.
- **housing**: Housing loan status.
- **loan**: Personal loan status.
- **contact**: Communication type (cellular or telephone).
- **month**: Last contact month.
- **day_of_week**: Last contact day.
- **campaign**: Number of contacts during the current campaign.
- **pdays**: Days since the last contact in the previous campaign.
- **previous**: Number of contacts during previous campaigns.
- **poutcome**: Outcome of the previous marketing campaign.
- **emp.var.rate**: Employment variation rate.
- **cons.price.idx**: Consumer price index.
- **cons.conf.idx**: Consumer confidence index.
- **euribor3m**: 3-month Euribor rate.
- **nr.employed**: Number of employees.
- **y**: Target variable, indicating whether the client subscribed to the product (`yes` or `no`).


### Dataset Location

- **Data/**: This folder will contain the dataset files downloaded from Kaggle.
- **Notebook/**: This folder will house your Jupyter notebooks. **Currently, we are working within the Notebook directory.**

## Project Structure

```plaintext
Bank-Marketing-Prediction/
├── Data/
│   └── [dataset files downloaded from Kaggle]
├── Notebooks/
│   └── [Jupyter notebooks for analysis and modeling]
└── README.md
```


## Project Workflow

### Data Preprocessing
1. **Encoding Categorical Variables**: Applied `LabelEncoder` to convert categorical features into numerical values.
2. **Feature Scaling**: Standardized features using `StandardScaler` for optimal model performance.

### Model Training
- Base Estimator: `DecisionTreeClassifier` with a maximum depth of 3.
- Boosting Algorithm: `AdaBoostClassifier` with 70 estimators and a learning rate of 1.0.

### Model Evaluation
The model's performance was assessed using the **F1 score**:
- **Training F1 Score**: 0.6552
- **Test F1 Score**: 0.6042

## Requirements

To run this project, you'll need the following Python libraries:
- `pandas`
- `scikit-learn`
- `kaggle`
