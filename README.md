AI-Driven Forest Fire Prediction with Explainable AI (XAI)

Project Overview:
This project develops an AI-powered system to predict forest fire risks by integrating Explainable AI (XAI) with real-time environmental and climatic data. Traditional models often struggle with adaptability across different regions due to limited feature diversity. By incorporating vegetation data and XAI techniques, this approach enhances prediction accuracy and decision-making in high-risk scenarios.

Data Collection and Preprocessing:
Data Sources:
1)ERA5 Single Levels Dataset: Provides meteorological data such as temperature, wind speed, humidity, and precipitation.
2)NASA FIRMS Data: Satellite-based fire location data, including fire intensity and duration.

Data Processing Steps:
1)Preprocessing: Separated date and time components for improved temporal analysis, handled missing values, and resolved inconsistencies.
2)Dataset Merging: Aligned spatial and temporal attributes of ERA5 and FIRMS datasets, applying feature selection to retain key factors affecting fire occurrences.
3)Region Selection: Focused on the Satpura Range, a high-risk area for seasonal forest fires, ensuring balanced training and validation data.
4)Scaling & Transformation: Resampled data into weekly averages and applied log transformation with MinMax scaling for normalization.

Model Architecture: LSTM for Fire Prediction
Predictive Modeling:
Model Used: Long Short-Term Memory (LSTM) for time-series forecasting.
Feature Selection: Considered meteorological, fire incident, and vegetation attributes.
Input: Last 4 weeks of data used for predicting upcoming fire risks.
Architecture: Two-layer LSTM with 64 hidden units, followed by a fully connected layer for final predictions.

Optimization:
Loss Function: Mean Squared Error (MSE).
Optimizer: Adam with a learning rate of 0.001.
Gradient Clipping: Prevents exploding gradients.
NaN Handling: Training stops automatically if NaN loss is detected.

Explainability and Evaluation:
SHAP (SHapley Additive exPlanations): Provides interpretability by explaining feature contributions to model predictions.
Performance Metrics: Evaluated using accuracy, precision, recall, and F1-score.

Implementation Progress and Insights:
Current Progress:
Completion Status: Phase 1 achieved 35% completion, covering data integration, preprocessing, and initial model training.
Key Findings:
Identified gaps in integrating diverse datasets, including meteorological, fire incidents, and vegetation data.
Vegetation data plays a crucial role in improving model accuracy, yet remains underexplored in existing research.
Models Tested: LSTM and Transformer-based models for comparative analysis.

Ongoing Work and Future Enhancements:
This project is still in progress, with planned optimizations and improvements:
Hyperparameter Tuning: Refining LSTM layers, dropout rates, and learning rate to improve performance.
Transformer Models: Exploring Transformer-based models for long-term dependency learning and comparing results with LSTM.
Extended Forecasting: Developing hierarchical forecasting for daily and monthly predictions.
Real-World Deployment: Ensuring cost-effective, open-source implementation with data security and privacy compliance.

This project sets the stage for advanced forest fire prediction systems by leveraging Explainable AI and multi-source data integration to enhance prediction accuracy and interpretability.

