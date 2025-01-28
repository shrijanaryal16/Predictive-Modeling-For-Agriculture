# Crop Yield Prediction Model

This project focuses on analyzing soil metrics to determine which elements have the most significant impact on crop yield. Using a dataset containing soil measurements (Nitrogen, Phosphorous, Potassium, and pH levels), the project employs machine learning techniques to identify the most predictive feature for crop production.

## Dataset
The dataset used in this project contains the following features:
- **N**: Nitrogen content ratio in the soil
- **P**: Phosphorous content ratio in the soil
- **K**: Potassium content ratio in the soil
- **pH**: pH value of the soil
- **crop**: The target variable, representing the type of crop grown in the soil.

The dataset is stored in a CSV file named `soil_measures.csv`.

## Project Workflow
1. **Data Loading and Exploration**:
   - The dataset is loaded using `pandas`.
   - Basic exploration is performed to understand the structure and content of the data.

2. **Data Preprocessing**:
   - Categorical features (crop types) are converted into numerical features using one-hot encoding (`pd.get_dummies`).
   - Missing values are checked, and since there are none, no imputation is required.

3. **Feature Analysis**:
   - A logistic regression model is trained for each soil feature (N, P, K, pH) to determine its predictive power for crop yield.
   - The accuracy scores for each feature are calculated and compared.

4. **Results**:
   - Potassium (K) is identified as the most predictive feature for crop yield, with the highest accuracy score.

## Key Findings
- **Potassium (K)** has the most significant impact on crop yield among the measured soil metrics.

## Libraries Used
- `pandas`: For data manipulation and analysis.
- `scikit-learn`: For machine learning model training and evaluation.
  - `LogisticRegression`: Used to train the model.
  - `train_test_split`: For splitting the dataset into training and testing sets.
  - `metrics`: For evaluating model performance.

## How to Run the Code
1. Clone this repository:
   ```bash
   git clone https://github.com/shrijanaryal16/crop-yield-prediction.git
