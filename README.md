# Hotel Booking Cancellation Prediction
## Requirements
1) python 3 or later
2) work with vscode or colab
3) setup the enviroment for vs code 
```bash
pip install requirements.txt
```

## Introduction

This project aims to develop a reliable data preprocessing pipeline and a predictive model for hotel booking cancellations. By accurately predicting cancellations, hotels can better manage their resources, optimize revenue, and reduce losses associated with last-minute changes. The focus of this initial phase is on transforming raw booking data into a clean, structured, and informative dataset suitable for machine learning model development.

## Data

The dataset used in this project contains historical hotel booking information. Key features include booking details (lead time, arrival dates, length of stay), guest demographics (adults, children, babies, country of origin), booking specifics (meal plan, market segment, distribution channel, repeated guest status), previous booking history (cancellations, non-cancellations), room information (reserved and assigned room types), booking changes, deposit type, agent and company information, waiting list days, average daily rate (ADR), required parking spaces, and special requests. The target variable is `is_canceled`, indicating whether a booking was canceled (1) or not (0).

Detailed column descriptions and data types are provided in the notebook.

## Methodology

The data preprocessing pipeline involved several crucial steps:

1.  **Data Loading and Initial Exploration**: The dataset was loaded and examined to understand its structure, identify data types, and get initial summary statistics.
2.  **Handling Missing Values**: Missing data in columns such as `children`, `country`, `agent`, and `company` were identified and addressed through imputation or removal based on the extent of missingness and potential relevance.
3.  **Handling Duplicates**: Duplicate booking records were identified and removed to ensure data integrity and prevent bias.
4.  **Outlier Detection and Treatment**: Potential outliers in numerical features like `lead_time` and `adr` were visualized and analyzed using the IQR method. Outliers were treated by capping extreme values to plausible limits based on business context.
5.  **Handling Categorical Features**: Low-frequency categories in certain columns were managed, and high-cardinality features like `country` were simplified by grouping less frequent categories.
6.  **Feature Engineering**: New features were created to capture more predictive information, such as `cancelation_ratio`, `assigned_reserved_room`, `is_in_waiting_list`, `total_nights`, `total_guests`, and `is_family`.
7.  **Handling Data Types**: Data types were corrected for columns where necessary to ensure proper handling during analysis and modeling.
8.  **Feature Selection**: Features that could cause data leakage (`reservation_status`, `reservation_status_date`) were removed. Redundant features were identified using Variance Inflation Factor (VIF) and feature importance from a preliminary model and subsequently dropped.
9.  **Encoding Categorical Variables**: Categorical features were converted into a numerical format using one-hot encoding to make them suitable for machine learning algorithms.
10. **Target Variable Analysis**: The distribution of the target variable was analyzed to understand the class balance and consider potential strategies for handling imbalance during modeling.
11. **Data Splitting**: The dataset was split into training and testing sets using stratified sampling to ensure representative subsets for model development and evaluation.

## Results

The data preprocessing steps have resulted in a clean, structured, and feature-engineered dataset. Missing values have been handled, duplicates removed, outliers addressed, and relevant new features created. The dataset is now prepared for the next phase of the project, which involves building and evaluating predictive models for hotel booking cancellations.



## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues if you have suggestions or find any bugs.
