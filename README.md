# Forest-Fire-Prediction-AI-ML

Project Overview
This project aims to create an AI-driven system for predicting forest fire risks by combining Explainable AI (XAI) with real-time environmental and climatic data. Current research often lacks diverse features and adaptive methods, limiting model effectiveness across different geographic areas. This project incorporates vegetation data and XAI techniques to improve prediction accuracy and enhance decision-making in high-risk situations.

Data Collection and Preprocessing
Data Sources
We obtained meteorological and fire incident data from multiple sources:
ERA5 Single Levels Dataset: Provides temperature, wind speed, humidity, and precipitation data.
NASA FIRMS Data: Satellite-based fire location data, including fire intensity and duration.

Data Processing Steps
Data Preprocessing:
Splitting date and time into separate components for better temporal analysis.
Handling missing and inconsistent data.
Dataset Merging:
Aligning spatial and temporal dimensions of ERA5 and FIRMS datasets.
Applying feature selection to retain relevant attributes influencing fire occurrence.
Region Selection:
Focused on the Satpura Range, known for frequent seasonal forest fires, to ensure balanced training and validation data.
Scaling and Transformation:
Resampled data to weekly averages.
Applied log transformation and MinMax scaling for normalization.

Model Architecture: LSTM for Fire Prediction
Predictive Modeling
Model Used: Long Short-Term Memory (LSTM) for time-series forecasting.
Feature Selection: Included meteorological, fire incident, and vegetation attributes.
Input: Last 4 weeks of data for predicting upcoming fire risks.
Architecture:
2-layer LSTM with 64 hidden units.
Fully connected (FC) layer for final prediction.
Optimization:
Loss Function: Mean Squared Error (MSE).
Optimizer: Adam (learning rate = 0.001).
Gradient Clipping: Prevents exploding gradients.
NaN Check: Stops training if NaN loss occurs.

Explainability and Evaluation
SHAP (SHapley Additive exPlanations): Used to interpret model outputs and explain feature contributions.
Performance Metrics: Evaluated using accuracy, precision, recall, and F1-score.
Implementation Progress and Insights
Progress: Achieved 35% implementation after Phase 1, covering data integration, preprocessing, and initial model training.
Key Observations:
Identified a research gap in integrating diverse datasets (meteorological, fire incidents, vegetation).
Vegetation data significantly improves model accuracy, though underexplored in existing research.
Models Used: LSTM and Transformer-based models for comparison.
Ongoing Work and Future Enhancements
This project is still ongoing and not yet fully completed. Several improvements and optimizations are planned to enhance model performance and deployment readiness:

Hyperparameter Tuning:
Optimize the number of LSTM layers, dropout rates, and learning rate to enhance accuracy.
Transformer-based Models:
Improve long-term dependency modeling.
Compare performance with LSTM.
Extended Forecasting:
Develop daily and monthly predictions using hierarchical forecasting.
Real-World Deployment:
Optimize model for cost-effective, open-source implementation.
Ensure data security and privacy compliance.

This project lays the foundation for advanced forest fire prediction systems, leveraging Explainable AI and multi-source data integration for more accurate and interpretable predictions.
