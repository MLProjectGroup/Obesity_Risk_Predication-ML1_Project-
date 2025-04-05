# Obesity Risk Prediction

## Overview
This project uses machine learning techniques to predict obesity risk based on various lifestyle and health factors. By analyzing demographic, dietary, and physical activity data, our models aim to identify individuals at higher risk of obesity, potentially enabling early intervention.

## Table of Contents
- [Project Motivation](#project-motivation)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Models](#models)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Project Motivation
Obesity is a significant global health challenge associated with numerous health complications including diabetes, cardiovascular disease, and certain cancers. Early identification of individuals at risk can lead to timely interventions and improved health outcomes. This project leverages machine learning to create a predictive model that can assist healthcare professionals in identifying at-risk individuals.

## Dataset
The project uses a dataset containing attributes such as:
- Demographic information (age, gender, etc.)
- Eating habits and dietary patterns
- Physical activity levels
- Family history
- Psychological factors
- Other lifestyle choices

The data has been preprocessed to handle missing values, encode categorical variables, and normalize numerical features.

## Installation

```bash
# Clone the repository
git clone https://github.com/MLProjectGroup/Obesity_Risk_Predication-ML1_Project.git
cd Obesity_Risk_Predication-ML1_Project

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows, use: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## Usage

### Data Preprocessing
```python
# Import the preprocessing module
from src.preprocessing import preprocess_data

# Load and preprocess the data
X_train, X_test, y_train, y_test = preprocess_data('path/to/data.csv')
```

### Training Models
```python
# Import the training module
from src.models import train_model

# Train a model (e.g., Random Forest)
model = train_model(X_train, y_train, model_type='random_forest')
```

### Making Predictions
```python
# Import the prediction module
from src.predict import predict_obesity_risk

# Make predictions
predictions = predict_obesity_risk(model, X_test)
```

## Models
We have implemented and compared several machine learning models:
- Random Forest
- Gradient Boosting
- Support Vector Machines
- Neural Networks
- Logistic Regression

Each model has been optimized through hyperparameter tuning using techniques such as grid search and cross-validation.

## Results
Our best-performing model achieved an accuracy of XX% on the test set, with precision of XX% and recall of XX%. The most important features in predicting obesity risk were found to be:
1. Physical activity level
2. Dietary habits
3. Family history

