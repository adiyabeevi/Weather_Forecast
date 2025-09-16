# Weather Temperature Prediction using RNN

## Objective
This project aims to forecast the next day's temperature based on historical weather data using a Recurrent Neural Network (SimpleRNN).  

## Dataset
- **Source:** [Daily Weather Dataset – Kaggle](https://www.kaggle.com/)  
- **Features:**  
  - Date  
  - Temperature (target variable)  
  - Humidity  
  - Wind Speed  
  - Pressure (optional)  

## Project Workflow

### 1. Data Understanding and Preprocessing
- Loaded dataset and explored the first few rows.  
- Visualized temperature trends over time.  
- Checked for missing values and handled them via imputation/removal.  
- Normalized features using `MinMaxScaler` for faster RNN convergence.  
- Created sequences using past 7–14 days of weather data to predict the next day’s temperature.  
- Split data into training, validation, and test sets.  

### 2. SimpleRNN Model Development
- Built a Sequential model in TensorFlow/Keras:  
  - Input layer (sequence length × number of features)  
  - SimpleRNN layer (32–64 units)  
  - Optional Dropout layer  
  - Dense layer with 1 unit (linear activation)  
- Compiled the model using:  
  - Loss: Mean Squared Error (MSE)  
  - Optimizer: Adam  
  - Metrics: Mean Absolute Error (MAE)  
- Trained the model for 50–100 epochs with a batch size of 32, using validation data to monitor performance.  
- Plotted training vs validation loss curves.  

### 3. Model Evaluation & Forecasting
- Evaluated model on the test set using RMSE, MAE, and R² score.  
- Plotted predicted vs actual temperatures for the test period.  
- Forecasted the next 7 days of temperature and visualized predictions alongside recent historical data.  

<img width="1008" height="491" alt="image" src="https://github.com/user-attachments/assets/8c8faeec-dbea-4b97-94c0-ad0715cce086" />
<img width="826" height="451" alt="image" src="https://github.com/user-attachments/assets/7e066cac-c4a6-45d4-8472-73dca21f0931" />
<img width="700" height="393" alt="image" src="https://github.com/user-attachments/assets/cdba9615-aabc-479c-8dab-3ede83be2d10" />
