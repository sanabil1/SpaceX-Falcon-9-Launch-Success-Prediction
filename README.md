# SpaceX Falcon 9 First Stage Landing Prediction 

## Table of Contents

1. [Project Overview](#project-overview)
2. [Objectives](#objectives)
3. [Dataset Description](#dataset-description)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
5. [Machine Learning Modeling](#machine-learning-modeling)
6. [Final Observation](#final-observation)
7. [Data Visualization](#data-visualization)
8. [Tools & Libraries Used](#tools--libraries-used)
9. [Results Summary](#results-summary)

## Project Overview   
This project aims to **predict whether the Falcon 9 first stage will successfully land** after launch, helping estimate potential launch costs and offering valuable insights for competitors and stakeholders.  

Through a combination of **Exploratory Data Analysis (EDA)**, **Machine Learning modeling**, and **Interactive Dashboards**, this project demonstrates the full data science lifecycle — from **data collection** to **model deployment**.

## Objectives  
- Perform **exploratory data analysis** to identify key factors affecting launch success.  
- Build and compare multiple **Machine Learning models** to predict first-stage landing success.  
- Visualize trends and insights using **Python (Matplotlib, Seaborn, Folium)**.  
- Create an **interactive dashboard** using **Plotly Dash**.  

## Dataset Description  

### SpaceX Launch Data  
- **Source:** [IBM Skills Network Datasets (SpaceX)]
- **Files Used:**  
  - `dataset_part_1.csv`, `dataset_part_2.csv`, `dataset_part_3.csv`  
  - `spacex_launch_dash.csv` (for dashboard)  
  - `spacex_launch_geo.csv` (for geographical visualization)  

### Key Features  

| Feature | Description |
|----------|-------------|
| `FlightNumber` | Flight serial number |
| `Payload Mass (kg)` | Weight of the payload |
| `Orbit` | Orbit type of the mission |
| `Launch Site` | Site of rocket launch |
| `Class` | Landing success indicator (1 = Landed, 0 = Not Landed) |
| `Booster Version Category` | Type of rocket booster used |


## Exploratory Data Analysis (EDA)  

EDA was performed using **Matplotlib**, **Seaborn**, and **Folium** to uncover key insights such as:  
- Relationship between **payload mass** and **landing success rate**  
- Impact of **orbit type** and **launch site** on success probability  
- **Geographical visualization** of launch sites and their proximities using **Folium Maps**  
- Interactive **Dash app** showing success rates and payload correlations  

## Machine Learning Modeling  

We tested multiple classification models to predict first-stage landing success:

| Model | Algorithm | Validation Accuracy | Test Accuracy | F1 Score |
|--------|------------|--------------------------|----------------|-----------|
| Logistic Regression | Supervised | 0.846 | 0.833 | 0.814 |
| Support Vector Machine (SVM) | Supervised | 0.848 | 0.833 | 0.814 |
| Decision Tree Classifier | Supervised | 0.875 | 0.944 | 0.943 |
| K-Nearest Neighbors (KNN) | Supervised | 0.848 | 0.833 | 0.814 |


## Final Observation  

Among all models tested, the **Decision Tree Classifier** achieved the **best performance** with:  
- **Accuracy:** 94.4%  
- **F1-score:** 0.943
- **Criterion:** Entropy  
- **Max Depth:** 4  
- **Random State:** 3  

This model effectively predicts whether the Falcon 9 first stage will successfully land, making it the most reliable for future launch outcome predictions.


## Data Visualization  

Key visualizations generated during EDA include:  
- Success rate distribution across different **launch sites**  
- Relationship between **payload mass** and **landing outcomes**  
- Interactive **Folium map** marking all SpaceX launch sites  
- Correlation analysis between payload and success using **Plotly Scatter Charts**  
- Custom **Matplotlib dashboard** summarizing all launch metrics  


## Tools & Libraries Used  

| Category | Tools / Libraries |
|-----------|-------------------|
| Programming | Python |
| Data Analysis | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn, Plotly, Folium |
| Machine Learning | Scikit-learn |
| Dashboard | Plotly Dash |
| Environment | Jupyter Notebook / Vocareum Cloud |


## Results Summary  

- Identified patterns affecting Falcon 9 first-stage landing outcomes.
- Achieved **94%+ predictive accuracy** using the Decision Tree Classifier.  
- Built **interactive dashboards** and **geospatial visualizations** for launch analysis.  
- Developed a **reproducible ML pipeline** covering preprocessing, modeling, and evaluation.
