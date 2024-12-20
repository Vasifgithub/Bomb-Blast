
Peak Particle Velocity (PPV) Prediction Using Ensemble Machine Learning Models

This project focuses on predicting Peak Particle Velocity (PPV), a critical measure of ground vibration generated by blasting operations in mining and construction. Ground vibrations can cause significant damage to nearby structures and ecosystems, making it essential to accurately predict PPV for safer and more efficient blasting practices.

Table of Contents
Project Overview
Data Collection
Machine Learning Models
Model Performance
Features and Target
Installation
Usage
Results and Evaluation
Applications and Future Scope
Project Overview
Blasting operations generate ground vibrations that can cause significant damage to structures, fields, and ecosystems. Traditional methods for predicting PPV are limited, relying on a narrow set of parameters. This project uses ensemble machine learning models to overcome these limitations by considering multiple factors such as burden, stemming, and number of holes.

The dataset used includes 121 blast events from Mine-A, India. The goal is to predict PPV using a variety of machine learning algorithms, improving safety, efficiency, and reducing ecological impact.

Data Collection
Source: Mine-A, India (121 blast events).
Features: Distance, stemming, burden, spacing, charge per delay, hole diameter, number of holes.
Target: Peak Particle Velocity (PPV) (log-transformed).
Machine Learning Models
This project uses ensemble learning models, which combine multiple base models for better predictive performance:

XGBoost
Random Forest
Gradient Boosting
DecisionTree
Stacking Regressor: Combines the outputs of base models using ElasticNet as the meta-model.
Hyperparameter Tuning
GridSearchCV is used to tune the hyperparameters for each model:

XGBoost: Learning rate, number of estimators, depth.
Random Forest: Number of trees, max depth, minimum samples.
Gradient Boosting: Learning rate, subsampling, depth.
Model Performance
Hybrid Model: A combination of XGBoost, Random Forest, Gradient Boosting, and ElasticNet achieved the best performance with an R² value of 0.974.
Metrics:
R² (Coefficient of Determination): Measures the goodness of fit.
RMSE (Root Mean Squared Error): Measures prediction accuracy.
MAE (Mean Absolute Error): Measures the average error magnitude.
Features and Target
Features: Burden, spacing, stemming, number of holes, distance, etc.
Target: PPV (log-transformed).
Installation
To install and run the project locally, follow these steps:

Clone this repository:

bash
Copy code
git clone https://github.com/Vasifgithub/Bomb-Blast.git
Navigate to the project directory:

bash
Copy code
cd Bomb-Blast
Install the required dependencies:

bash
Copy code
pip install -r requirements.txt
Usage
To train and evaluate the model, run the following Python script:

bash
Copy code
python app.py
This will train the ensemble models on the provided dataset and output the performance metrics.

Results and Evaluation
The hybrid ensemble model (XGBoost + Random Forest + Gradient Boosting + ElasticNet) provided the best performance for predicting PPV, achieving an R² score of 0.974. The results demonstrate the power of ensemble learning techniques in overcoming the limitations of traditional empirical models.

Applications and Future Scope
Applications: Safer mining practices, reduced environmental damage, and improved operational efficiency in blasting operations.
Future Scope:
Real-time integration for dynamic PPV prediction.
Exploration of neural networks and other advanced AI techniques for further enhancement of prediction accuracy.
