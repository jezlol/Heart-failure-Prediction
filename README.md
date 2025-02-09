# Heart Disease Prediction

A machine learning web application that predicts the likelihood of heart disease based on various health parameters. The project combines deep learning with a user-friendly web interface for easy access to predictions.

## Features

### 1. Prediction Capabilities
- Predicts heart disease risk with probability percentage
- Provides risk level classification (Low, Moderate, High)
- Risk levels are categorized as:
  - Low Risk (≤30%): Indicated by green progress bar
  - Moderate Risk (31-70%): Indicated by yellow progress bar
  - High Risk (>70%): Indicated by red progress bar

### 2. Input Parameters
The model accepts the following health parameters:
- Age (20-100 years)
- Sex (Male/Female)
- Chest Pain Type (ATA/NAP/ASY/TA)
- Resting Blood Pressure (80-200 mmHg)
- Cholesterol Level (100-600 mg/dL)
- Fasting Blood Sugar (>120 mg/dl: Yes/No)
- Resting ECG (Normal/ST/LVH)
- Maximum Heart Rate (60-220 bpm)
- Exercise-Induced Angina (Yes/No)
- ST Depression (Oldpeak: 0-6)
- ST Slope (Up/Flat/Down)

### 3. Web Interface Features
- Responsive design for desktop and mobile devices
- Real-time form validation
- Interactive progress bar showing risk level
- Color-coded risk indicators
- Smooth animations and transitions
- User-friendly input forms with appropriate ranges
- Immediate visual feedback

### 4. Technical Implementation
- Neural Network model with multiple layers
- Data preprocessing and scaling
- Support for both neural network (.h5) and traditional ML models (.pkl)
- Error handling and validation
- Real-time predictions

## Project Structure

```
.
├── data/                      # Data directory
│   ├── heart_failure_data.csv # Original dataset
│   ├── X_train_scaled.npy    # Scaled training features
│   ├── X_test_scaled.npy     # Scaled test features
│   ├── y_train.npy           # Training labels
│   └── y_test.npy            # Test labels
├── models/                    # Model directory
│   ├── heart_disease_model.h5 # Trained neural network model
│   ├── scaler.pkl            # StandardScaler object
│   └── label_encoders.pkl    # LabelEncoder objects
├── notebooks/                 # Jupyter notebooks
│   ├── 1_data_preparation.ipynb  # Data preprocessing
│   ├── 2_model_training.ipynb    # Model training
│   └── 3_web_interface.ipynb     # Flask web application
├── requirements.txt          # Project dependencies
└── README.md                # Project documentation
```

## Installation

1. Clone this repository:
```bash
git clone <repository-url>
cd heart-disease-prediction
```

2. Create a virtual environment and activate it:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install the required dependencies:
```bash
pip install -r requirements.txt
```

## Usage

### 1. Data Preparation
Run the data preparation notebook:
```bash
jupyter notebook notebooks/1_data_preparation.ipynb
```
This notebook handles:
- Data loading and cleaning
- Feature encoding
- Data scaling
- Train-test splitting

### 2. Model Training
Run the model training notebook:
```bash
jupyter notebook notebooks/2_model_training.ipynb
```
This notebook includes:
- Neural network model creation
- Model training and validation
- Performance evaluation
- Model saving

### 3. Web Interface
Run the web interface notebook:
```bash
jupyter notebook notebooks/3_web_interface.ipynb
```
Features:
- Flask web server setup
- Interactive HTML interface
- Real-time predictions
- Risk level visualization

## Dependencies
- Python 3.12+
- numpy>=1.21.0
- pandas>=1.3.0
- matplotlib>=3.4.0
- seaborn>=0.11.0
- scikit-learn>=0.24.0
- tensorflow>=2.7.0
- flask>=2.0.0
- And other requirements listed in requirements.txt

## Model Performance
The neural network model achieves:
- High accuracy in prediction
- Robust performance across different patient profiles
- Real-time prediction capability
- Reliable risk assessment

## Future Improvements
- Add more visualization options
- Implement user authentication
- Add prediction history tracking
- Expand the dataset
- Add model retraining capabilities

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.