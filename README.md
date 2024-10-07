Predictive Maintenance with LSTM in PyTorch

This project demonstrates a predictive maintenance model using Long Short-Term Memory (LSTM) networks built in PyTorch. The goal of this project is to predict the Remaining Useful Life (RUL) of turbofan engines based on historical sensor data. This can be particularly useful for industries where predictive maintenance is critical, such as aerospace, automotive, and manufacturing.

Dataset
The dataset used in this project is the NASA C-MAPSS Turbofan Engine Degradation Dataset (FD001). The dataset contains operational settings and sensor data from multiple engines across their entire life cycle, until failure.

Training Set: Contains data for engines from the beginning of their operation until failure.
Test Set: Contains data for engines where we need to predict the Remaining Useful Life (RUL).
Each engine has several sensor readings and operational settings over a series of cycles. The target is to predict the remaining cycles before failure (RUL).

Model Architecture
This project utilizes a Long Short-Term Memory (LSTM) network, a recurrent neural network (RNN) well-suited for time-series forecasting tasks. The model is designed to capture the temporal dependencies between consecutive engine cycles and sensor readings.

Input: Sequences of sensor readings for each engine over a defined time window (e.g., 30 cycles).
LSTM Layers: The model consists of 4 LSTM layers, with 256 hidden units in each layer, which captures temporal dependencies.
Output: The model predicts each input sequence's Remaining Useful Life (RUL).
Model Hyperparameters:
Hidden size: 256
LSTM layers: 4
Learning Rate: 0.0001 (with a learning rate scheduler that decreases over time)
Optimizer: Adam
Loss Function: Mean Squared Error (MSE)
Batch Size: 64
Epochs: 50
