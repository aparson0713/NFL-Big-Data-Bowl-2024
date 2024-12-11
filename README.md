# NFL-Big-Data-Bowl-2024
This repository contains the code for an analysis of the NFL Big Data Bowl 2024. This was done as part of an Advanced Machine Learning class project for the MSBA program at UT McCombs. We developed several models to predict play type (run vs pass) and run location. These models can be found in the folder labeled 'Code'.

Data and information regarding this competititon can be found at this link: https://www.kaggle.com/competitions/nfl-big-data-bowl-2025

We have broken down the code by team member. Below is a brief description of each code

## Aditya Code

Baseline Models.ipynb: This notebook sets up foundational models, primarily focusing on logistic regression as a baseline, with engineered features like score differential and third-and-long to predict play outcomes. It evaluates basic performance metrics, setting a benchmark for more advanced models.

Logistic Regression.ipynb: This notebook delves deeper into logistic regression, optimizing its features and parameters while assessing its predictive power through metrics like precision, recall, and ROC-AUC scores.

XG and RF.ipynb: This file explores advanced ensemble methods like XGBoost and Random Forest, leveraging their ability to handle complex interactions in the data and comparing their performance against baseline models.

Exploring 1.ipynb: Focused on exploratory data analysis (EDA), this notebook examines patterns in the dataset, identifying key features and correlations that influence model predictions.

Exploring 2.ipynb: Continuing EDA, this notebook analyzes play-specific variables and distributions, creating visualizations to uncover trends and inform feature engineering.

Exploring 3.ipynb: This file expands on earlier EDA by inspecting outliers and segment-specific patterns, providing insights into data segmentation and refinement for modeling purposes. 

## Alicia Code
Tracking Data Integration: Filters and merges weekly player tracking datasets for the Kansas City Chiefs, combining it with play-by-play, player, and game-level data for enriched feature engineering.

Feature Engineering: Creates variables like play types (pass or run), pre-snap player alignment, and possession-specific metrics, leveraging both raw tracking data and play-level attributes.

Visualization and Insights: Uses matplotlib and seaborn to visualize patterns in player movements, play distributions, and team-specific strategies, enhancing interpretability of data trends.

Play Type Prediction Models: Implements logistic regression to classify plays as pass or run, evaluates models using metrics such as ROC-AUC, and emphasizes the importance of integrating tracking and play-by-play features.

## Alex Code
Random Forest:
The Random Forest model is used for run location prediction by training on engineered features like yardline position, offensive formation, and alignment.
This was most accurate model for run location, when combined with team-level PCA groupings. 

XGBoost:
XGBoost is applied to the same play prediction task, leveraging its efficiency and handling of missing data.

Hybrid Neural Network:
Combines structured data (features) with insights from embeddings derived from tracking or categorical data.
This hybrid model combines a GRU and dense layers to capture both the granular patterns of individual plays and broader game-level trends.

Team-Level PCA Groupings (used in both Random Forest and XGBoost):
Principal Component Analysis (PCA) groups teams based on offensive and defensive play styles, clustering teams with similar tendencies.
This reduces dimensionality and allows for nuanced insights into how team-specific strategies influence model predictions.
