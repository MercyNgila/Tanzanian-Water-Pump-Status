# Pump-It-Up


## Introduction

![running water](unsplash_water .jpeg)

<span>Photo by <a href="https://media.istockphoto.com/photos/poor-indian-children-asking-for-fresh-water-india-picture-id637020090?s=612x612">Bartosz Hadyniak</a> on <a 
href="https://www.istockphoto.com/photo/poor-indian-children-asking-for-fresh-water-india-gm637020090-113379827">Unsplash</a></span>


## Business Understanding

### Problem
Water shortage in Tanzania has been a problem for years now. The most affected are the rural areas. One out of six people lack access to safe drinking water in Tanzania (WHO/UNICEF, 2004).

According to UNICEF, It is estimated that Tanzania spends 70 per cent of its health budget on preventable Water, Sanitation and Hygiene (WASH) related diseases as the majority of the population does not have access to improved sanitation, and close to half of the population does not have access to clean drinking water.

As part of its Vision 2025, the Government of Tanzania has pledged to increase access to improved sanitation to 95 per cent by 2025. The Second Five Year Development Plan (FYDP II) has also set the target for access to improved sanitation facilities at 85 per cent in rural areas.

UNICEF is working with the Tanzanian Government and development partners on four priority WASH areas:

1. To ensure access to improved sanitation and hygiene in rural and peri-urban communities.
2. Develop sustainable solutions for provision of WASH facilities in health and educational institutions.
3. Ensure sustainable and equitable access to safe drinking water in rural and periurban areas.
4. Provide effective response in emergencies to prevent the spread of diseases due to poor sanitation, unhygienic living conditions and unsafe drinking water.

### Aim
There are many water wells already established across different parts of the country.

To achieve the third priority WASH areas goal, there is need to know the conditions of the waterpumps in these water wells which would advice the best strategy moving forward.. Visiting each well to establish their conditions would be highly costly and time consuming.

The Tanzanian Government in partnership with UNICEF has contracted my consulting company, Nangila Analytics, to create a machine learning (ML) model to predict conditions of waterpumps ranking them in three levels:

- Functional
- Non Functional
- Functional needs repair

This ML model will be used to choose the best strategy moving forward.

## Objectives

- To build a ML prediction model for condition of waterpumps
- To compare different ML models predictions to achieve highest accuracy
- Advice the client on best strategy


##  Data Understanding

The data that I will use for this project comes from the Taarifa waterpoints dashboard, which aggregates data from the Tanzania Ministry of Water.

Taarifa is an open source platform for the crowd sourced reporting and triaging of infrastructure related issues. It acts a a bug tracker for real world which helps to engage citizens with their local government. It has been working on an Innovation Project in Tanzania, with various partners.

There are three datasets for this project:
 1. Training set labels (59400 waterpoints × 2 features)
 2. Training set values (59400 waterpoints × 40 features)
 3. Test set values (14850 waterpoints × 40 features)

For this project I will use datasets 1 & 2. 

The target variable will be status_group which details the functionality of a waterpoint

### Features include:

- amount_tsh           - Total static head (amount water available to waterpoint)
- date_recorded         - The date the row was entered
- funder                - Who funded the well
- gps_height            - Altitude of the well
- installer             - Organization that installed the well
- longitude             - GPS coordinate
- latitude              - GPS coordinate
- wpt_name              - Name of the waterpoint if there is one
- num_private           - No description
- basin                 - Geographic water basin
- subvillage            - Geographic location
- region                - Geographic location
- region_code           - Geographic location (coded)
- district_code         - Geographic location (coded)
- lga                   - Geographic location
- ward                  - Geographic location
- population            - Population around the well
- public_meeting        - True/False
- recorded_by           - Group entering this row of data
- scheme_management     - Who operates the waterpoint
- scheme_name           - Who operates the waterpoint
- permit                - If the waterpoint is permitted
- construction_year     - Year the waterpoint was constructed
- extraction_type       - The kind of extraction the waterpoint uses
- extraction_type_group - The kind of extraction the waterpoint uses
- extraction_type_class - The kind of extraction the waterpoint uses
- management            - How the waterpoint is managed
- management_group      - How the waterpoint is managed
- payment               - What the water costs
- payment_type          - What the water costs
- water_quality         - The quality of the water
- quality_group         - The quality of the water
- quantity              - The quantity of water
- quantity_group        - The quantity of water
- source                - The source of the water
- source_type           - The source of the water
- source_class          - The source of the water
- waterpoint_type       - The kind of waterpoint
- waterpoint_type_group - The kind of waterpoint




## Project Plan

1. Data Preparation
       - Loading Libraries
       - Loading data
       - Descriptive Exploration
       - Data Cleaning
       - Exploratory Descriptive Analysis (EDA)
       - Pre-processing Data
       
2.  Modelling
        - Train test split
        - Baseline Model
        - Random Forest
        - Decision Tree
        - Logistic Regression
        - Evaluation
        
4.  Conclusion

5.  Recommendation

## Modelling
For modelling I will apply:

1. Perform an X_Train-y_Test Split

2. Build and Evaluate a Baseline Model

3. Grid search to Find the Random Forest Model

4. Build Iterative Models to Find the Best Decision Tree Model

5. Build and Evaluate Additional Logistic Regression Models

6. Choose and Evaluate a Final Model

## Evaluation

The best performing model was picked as the final model. The best model was the base Random Forest Regression model. 
Its metric was: Accuracy:  0.8003032089615093. This translates to an accuracy of 80.03%


## Conclusion

Despite rigorous applications of different classification models to achieve the best accuracy, the final model at 80.03% is a good prediction model that is ready for deployment. With the high but balanced precision and recall results, the ML model advices greatly on which waterpoints to prioritise efforts on which further informs wise investments.

## Recommendation

bueborwnknpknrpginhihqeqhoquehohhnihwrpihdofhgihdpihfpivhndxbojfvjoabxsojbfvjobnsxojbfvjbasxbcjfdbnojasbovjbojdbvfjobdojabvojbndojbvfojbdojbfdjbdjbvfjbedjbvdfojndejbvfojbdwojbvjbdwjbvjbdwojbvfojoebojbeojefbwojdwbojbdwojbfvojbdoajbnfjobndejbrjbwdqojbvjobdqwojbj
