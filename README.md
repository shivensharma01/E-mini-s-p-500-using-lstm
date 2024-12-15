# Deep Learning LSTM Model Project

## Overview
This project focuses on building and training a **Long Short-Term Memory (LSTM)** model to analyze time-series data. The workflow covers preprocessing, model development, and evaluation, aiming to capture temporal dependencies and deliver accurate predictions.

---

## Objectives
- Clean and preprocess time-series data.
- Develop an LSTM model for sequence prediction tasks.
- Evaluate model performance using appropriate metrics.
- Visualize results for actionable insights.

---

## Dataset
The dataset used in this project (`dfDL.csv`) contains the following fields:
- **volume**: Data on transaction volumes (preprocessed to handle invalid values).
- **average**: Averages associated with the data.
- **barCount**: The count of bars for each segment.

### Preprocessing Steps:
1. **Data Cleaning**:
   - Invalid values (e.g., `-1`) replaced with `NaN`.
   - Removed irrelevant columns: `volume`, `average`, and `barCount`.
2. **Scaling**:
   - Applied **StandardScaler** to normalize the data for better model performance.
3. **Train-Test Split**:
   - Divided the data into 75% training and 25% testing subsets.

---

## Model Architecture
The model is built using TensorFlow/Keras:
- **Layers**:
  - LSTM layer to capture sequential dependencies.
  - Dense layer for final output predictions.
- **Compilation**:
  - Optimizer: `Adam`
  - Loss function: `Mean Squared Error (MSE)`
  - Metrics: Mean Absolute Error (MAE)

---

## Results
The LSTM model was trained for **20 epochs** and achieved the following results:
- **Final Training Loss (MSE)**: 0.0203
- **Final Validation Loss (MSE)**: 0.0140
- **Test Loss (MSE)**: 0.0135

### Visual Insights
- The model exhibited a steady decline in loss during training, with minimal overfitting observed.
- Test loss indicates the model generalizes well to unseen data.

---

## Future Work
1. **Hyperparameter Optimization**:
   - Experiment with different configurations of LSTM layers, units, and dropout rates.
2. **Advanced Architectures**:
   - Compare performance with GRU (Gated Recurrent Unit) and Transformer models.
3. **Additional Data Sources**:
   - Integrate larger and more diverse datasets to improve generalization.
4. **Real-Time Deployment**:
   - Adapt the model for real-time prediction scenarios using streaming data.

---

## Technologies Used
- **Programming Language**: Python
- **Libraries**:
  - `pandas`, `numpy`: For data manipulation and preprocessing.
  - `matplotlib`: To visualize model predictions and performance.
  - `scikit-learn`: For train-test splitting and data scaling.
  - `TensorFlow/Keras`: For building and training the LSTM model.
