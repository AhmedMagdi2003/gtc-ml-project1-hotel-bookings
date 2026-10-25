# Hotel Booking Cancellation: Data Preparation

**Turn historical booking records into a cleaner foundation for cancellation analysis.** This notebook project focuses on understanding the data and preparing useful, leakage-aware features for a later prediction study.

[Open the notebook](https://github.com/AhmedMagdi2003/gtc-ml-project1-hotel-bookings/blob/main/Notebook.ipynb) · [View the repository](https://github.com/AhmedMagdi2003/gtc-ml-project1-hotel-bookings)

## The project

The objective is to prepare booking data around the is_canceled outcome while avoiding fields that disclose the answer. The repository covers data cleaning, exploratory analysis, feature creation, and a stratified train/test split. It does not contain a completed prediction application.

## What the analysis covers

- Reviews missing values, duplicates, outliers, and selected categories.
- Creates booking context such as total nights, total guests, family status, waiting-list status, and room assignment differences.
- Removes reservation-status fields that directly reveal cancellation outcomes, reducing target leakage in downstream modeling.
- Prepares stratified data partitions for future model development.

## Explore the notebook

Open Notebook.ipynb in Jupyter with hotel_bookings.csv at the relative location expected by the notebook. Install the analysis libraries imported in the notebook if they are not already available in your environment.

## Built with

Python · pandas · NumPy · Matplotlib · Seaborn · scikit-learn · Jupyter

## Project scope

This repository is the preparation stage, not a cancellation-prediction product: it has no trained production model, prediction API, or deployment workflow. Historical booking patterns may not carry over to other hotels or time periods. Review the notebook's preprocessing and split strategy before using its outputs for model evaluation.

## About

Built by Ahmed Magdi as an applied data and machine-learning project. [Repository](https://github.com/AhmedMagdi2003/gtc-ml-project1-hotel-bookings)
