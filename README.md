<h1 align="center">Hi 👋, We're DSF PT09 Group 7 Capstone Project  </h1>

Github Repository: [Click to Open the Project Github Repository](https://github.com/odhinto/Phase3Project.git)

Tableau Dashboard: [Click to Open the Tableau Dashboard](https://public.tableau.com/views/Churn_17414751223480/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

# Concrete Compressive Strength Prediction Model
## 1. **Business Understanding**

**Problem to Solve**:  
The goal of this project is to develop a machine learning model that predicts concrete compressive strength based on the proportions of ingredients and other factors like age, using the concrete mix data.

**Why This Topic?**  
Accurate prediction of concrete compressive strength is essential for optimizing concrete mix design, minimizing material waste, and ensuring safety in construction projects.

**Industry/Application**:  
This project applies to the civil engineering and construction industries, where optimizing concrete mix designs is critical for both cost-efficiency and structural integrity.

**Target Audience**:  
- Civil Engineers
- Concrete Manufacturers
- Construction Project Managers

**Real-World Impact**:  
The ability to predict concrete strength effectively will lead to better mix design practices, reducing costs, and ensuring the required strength specifications for buildings and infrastructure.

## 2. **Data Understanding**

**Data Overview**:  
The dataset comprises 1030 records, with key features including cement, water, aggregates, superplasticizer, fly ash, slag, and age, with compressive strength as the target variable.

**Source of Data**:  
This dataset comes from Prof. I-Cheng Yeh’s research on concrete strength prediction using artificial neural networks.

**Feature Engineering**:  
The following derived ratios will be calculated as new features for model training:
- **Water-to-Cement Ratio**: To understand the impact of hydration on concrete strength.
- **Water-to-Binder Ratio**: To evaluate the influence of all binder materials (cement, fly ash, slag).
- **SP-to-Binder Ratio**: The role of superplasticizers in improving workability and strength.
- **Fly Ash-to-Binder Ratio**: To assess the impact of fly ash as a supplementary cementitious material.
- **Slag-to-Binder Ratio**: To examine the role of slag in strengthening the concrete mix.
- **Fly Ash + Slag-to-Binder Ratio**: To account for the combined effect of fly ash and slag on concrete properties.

**Data Collection Plan**:  
The data is already collected and is available for use in the project.

### 3. **Data Preparation**

**Data Storage**:  
The data will be stored in an Excel file and loaded into Pandas DataFrames for processing.

**Preprocessing**:
- **Feature Generation**: Create the new ratios (as described in the feature engineering section) for improved predictive performance.
- **Scaling**: Normalize the features to ensure consistent units and ranges, particularly for neural network models.
- **Handling Missing Data**: There are no missing values, but checks for any anomalies or outliers will be conducted.

**Challenges**:  
- **Feature Interaction**: The complexity of how the features interact (e.g., how water-to-cement ratio interacts with fly ash or slag content) requires careful modeling.
- **Multicollinearity**: Some features may be highly correlated, especially among the binder-related ratios, which could affect model performance.

### 4. **Modeling**

**Modeling Techniques**:  
- **Linear Regression**: For baseline comparison.
- **Random Forest Regressor**: To handle non-linear interactions and evaluate feature importance.
- **Gradient Boosting Machines**: For improved predictive accuracy.
- **Neural Networks**: To capture complex patterns, especially for interactions between newly generated feature ratios.

**Feature Selection**:  
- The generated ratios will be tested for their importance using models like Random Forest and Gradient Boosting, and less important features may be discarded.

**Target Variable**:  
Concrete compressive strength (measured in MPa).

## 5. **Evaluation**

**Evaluation Metrics**:  
- **Mean Absolute Error (MAE)**: For overall error measurement.
- **Root Mean Squared Error (RMSE)**: To highlight larger prediction errors.
- **R-Squared (R²)**: To evaluate how well the model explains the variance in compressive strength.

**Model Comparison**:  
- Performance will be compared across models (Linear Regression, Random Forest, Gradient Boosting, and Neural Networks) to identify the best predictive model.

### 6. **Deployment**

**Deployment Plan**:  
The model will be deployed as a Flask web app where users can input concrete mix details and receive a compressive strength prediction, or input a desired strength and receive suggested mix adjustments.

**Functionality**:  
- Input concrete mix features to predict compressive strength.
- Input a desired compressive strength and receive feature recommendations for the optimal mix.

### 7. **Tools/Methodologies**

**Libraries & Frameworks**:  
- **Pandas**: For data manipulation and preprocessing.
- **Scikit-learn**: For machine learning algorithms.
- **Keras/TensorFlow**: For building and training neural networks.
- **Matplotlib/Seaborn**: For visualizations.

**Analysis Environment**:  
The analysis will be conducted locally, with deployment on cloud platforms such as Heroku.

**Data Storage**:  
Data will be stored locally for development and on cloud storage during deployment.
