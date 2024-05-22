## Overview

This project aims to enhance water distribution in Tanzania by identifying and repairing dysfunctional wells. It leverages data analysis to forecast patterns in non-operational wells, providing actionable insights for Maji Safi Global and the Tanzanian government.

## Problem Statement

Tanzania has faced significant issues with poorly planned water projects, resulting in wasted funds and insufficient access to clean water. Maji Safi Global, an NGO, collaborates with the Tanzanian government through the Visima Vyema initiative to improve water infrastructure by repairing dysfunctional wells and analyzing non-functional well patterns.

## Data Understanding

The dataset contains features that describe various aspects of the water wells, including geographic, managerial, and operational details. Key features include:

amount_tsh: Total static head (water available)
date_recorded: Date the data was recorded
funder: Who funded the well
gps_height: Altitude of the well
installer: Organization that installed the well
longitude & latitude: GPS coordinates
population: Population around the well
status_group: Functional status of the well (target variable)

## Data Cleaning
Several columns were dropped due to irrelevance or redundancy. These include date_recorded, num_private, region_code, district_code, ward, extraction_type_group, extraction_type_class, management_group, payment_type, quality_group, quantity_group, source_type, waterpoint_type_group, and recorded_by.

## Exploratory Data Analysis (EDA)
EDA revealed outliers in amount_tsh, longitude, num_private, region_code, district_code, and population. Since some of these columns represent geographic locations, they were left unchanged, while others were investigated further.

## Feature Engineering
Feature engineering involved transforming and encoding categorical variables, handling missing values, and scaling numerical features to prepare the data for model training.

## Model Training and Evaluation
Several machine learning models were trained and evaluated:

## Random Forest Classifier

Accuracy: 80.38%
Precision: 79.77%
Recall: 80.38%
F1 Score: 79.87%
AUC: 0.90 for 'functional', 0.86 for 'functional needs repair'
Gradient Boosting Classifier

Accuracy: 77.30%
Precision: 76.51%
Recall: 77.30%
F1 Score: 75.79%
Both models performed well in classifying functional and non-functional wells but struggled with the 'functional needs repair' category.

Installation and Usage
To replicate this analysis, follow these steps:

Clone the repository

sh
Copy code
git clone https://github.com/yourusername/visima-vyema-classifier.git
cd visima-vyema-classifier
Install dependencies

sh
Copy code
pip install -r requirements.txt
Run the Jupyter notebook

sh
Copy code
jupyter notebook Visima_Vyema_Classifier.ipynb
Results
The Random Forest model showed the best performance overall, with an accuracy of 80.38%. However, the classification of wells that need repair remains challenging, indicating a need for further data or model refinement.

Conclusion
This project successfully identified key factors affecting well functionality and provided a robust model for predicting well statuses. Future work will focus on improving the model's performance for wells that require repair.

Contact
For questions or collaboration, please contact Brian909 at bmaina909@gmail.com
