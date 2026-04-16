# Wine Quality Prediction

An end-to-end machine learning project for predicting wine quality using physicochemical properties. This project implements a complete ML pipeline with data ingestion, validation, transformation, model training, and evaluation using MLflow for experiment tracking.

## 🍷 Project Overview

This project predicts the quality of red wine based on its physicochemical properties such as acidity, sugar content, and alcohol level. The system uses a structured ML pipeline architecture with configuration management and experiment tracking.

### Key Features

- **Automated ML Pipeline**: Complete end-to-end workflow from data ingestion to prediction
- **Configuration Management**: YAML-based configuration for easy parameter tuning
- **Experiment Tracking**: MLflow integration for model versioning and metrics tracking
- **Web Interface**: Flask-based web application for real-time predictions
- **Data Validation**: Schema-based data quality checks
- **Modular Architecture**: Clean separation of components for maintainability

## 🚀 ML Pipeline Components

### 1. Data Ingestion
- Downloads wine quality dataset from specified source
- Extracts and stores data in structured format

### 2. Data Validation
- Validates data against predefined schema
- Generates status reports for data quality checks

### 3. Data Transformation
- Feature engineering and preprocessing
- Train-test split preparation
- Data scaling and normalization

### 4. Model Training
- Trains machine learning model on processed data
- Hyperparameter optimization support
- Model serialization with joblib

### 5. Model Evaluation
- Comprehensive model performance evaluation
- MLflow integration for experiment tracking
- Metrics logging and model registry

## 🛠️ Installation

### Prerequisites
- Python 3.8+
- Git

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Wine-Quality-Prediction
   ```

2. **Create and activate virtual environment**
   ```bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # Unix/MacOS
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## 📊 Dataset

The project uses the Wine Quality dataset containing physicochemical properties:
- Fixed acidity
- Volatile acidity
- Citric acid
- Residual sugar
- Chlorides
- Free sulfur dioxide
- Total sulfur dioxide
- Density
- pH
- Sulphates
- Alcohol
- Quality (target variable)

## 🏃‍♂️ Usage

### Training the Model

Run the complete ML pipeline:
```bash
python main.py
```

### Web Application

Start the Flask web application:
```bash
python app.py
```

Access the application at `http://localhost:8080`

- **Home Page**: Input wine properties for prediction
- **Train Endpoint**: `/train` - Triggers model training
- **Predict Endpoint**: `/predict` - Returns quality predictions

## 📁 Project Structure

```
Wine-Quality-Prediction/
├── config/
│   └── config.yaml          # Pipeline configuration
├── src/
│   └── WineQualityPrediction/
│       ├── components/      # ML pipeline components
│       ├── pipeline/        # Pipeline orchestration
│       └── utils/           # Utility functions
├── templates/               # Flask HTML templates
├── research/               # Notebooks and experiments
├── artifacts/              # Generated artifacts (models, data)
├── app.py                  # Flask web application
├── main.py                 # Main training script
├── schema.yaml             # Data schema definition
├── params.yaml             # Model parameters
└── requirements.txt        # Python dependencies
```

## ⚙️ Configuration

### Key Configuration Files

- **config.yaml**: Pipeline paths and data sources
- **schema.yaml**: Data validation schema
- **params.yaml**: Model hyperparameters

### Updating Configuration

To modify the pipeline:

1. Update `config.yaml` for data paths and sources
2. Update `schema.yaml` for data validation rules
3. Update `params.yaml` for model parameters
4. Update entity classes in `src/WineQualityPrediction/entity/`
5. Update configuration manager in `src/WineQualityPrediction/config/`
6. Update components in `src/WineQualityPrediction/components/`
7. Update pipeline in `src/WineQualityPrediction/pipeline/`
8. Update `main.py` if needed

## 📈 Model Performance

The model is evaluated using:
- Accuracy metrics
- Confusion matrix
- Classification report
- Cross-validation scores

All metrics are logged to MLflow for tracking and comparison.

## 🔧 Technologies Used

- **Machine Learning**: scikit-learn
- **Data Processing**: pandas, numpy
- **Experiment Tracking**: MLflow
- **Web Framework**: Flask
- **Configuration**: PyYAML, python-box
- **Visualization**: matplotlib
- **Model Serialization**: joblib

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## 📄 License

This project is licensed under the terms specified in the LICENSE file.

## 📞 Contact

For questions or suggestions, please open an issue in the repository.