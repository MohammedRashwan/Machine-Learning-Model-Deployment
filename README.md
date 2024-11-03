# 🌟 End-to-End Machine Learning Model Training & Deployment on Azure

## Overview
This project provides an end-to-end solution for **Machine Learning model training**, serving predictions through a **Flask API**, and optionally deploying the model on **Microsoft Azure**. This workflow covers data handling, model training, local API setup, and cloud deployment.

---

<div align="center">
    <svg width="100%" height="30">
        <rect width="100%" height="100%" fill="#4CAF50"/>
    </svg>
</div>

## Key Components

### 🗃️ Data Loading and Model Training
- Loads a dataset, trains a **RandomForest Classifier** model, and saves it for inference.

<div align="center">
    <svg width="100%" height="30">
        <rect width="100%" height="100%" fill="#2196F3"/>
    </svg>
</div>

### 🌐 Flask API for Model Serving
- Deploys a **Flask API** to serve predictions, providing easy access to the trained model through a RESTful interface.

<div align="center">
    <svg width="100%" height="30">
        <rect width="100%" height="100%" fill="#FFC107"/>
    </svg>
</div>

### ☁️ Azure ML Deployment (Optional)
- **Registers** and **deploys** the trained model on **Azure Machine Learning**, enabling cloud-hosted, scalable predictions.

---

## Getting Started

### Prerequisites
- **Python 3.7+**
- **Azure SDK** and other dependencies installed via:
   ```bash
   pip install pandas scikit-learn joblib flask azureml-core

### Installation
- Clone the repository
- Copy code
  ```bash
  git clone https://github.com/yourusername/yourproject.git
  cd yourproject

Install dependencies as listed above.

### Step-by-Step Usage Guide
- Step 1: Model Training and API Setup
- Train the Model and Launch the API
Run the main script to train the model and start a local API:
   ```bash
   python main.py
   

This will:

- Train a RandomForestClassifier model on your dataset.

- Save the model as model.pkl for later use.

- Start a local Flask API at http://localhost:5000 to serve predictions.

Test the Prediction API
- Test the API by sending a POST request to the /predict endpoint:
    
    curl -X POST http://localhost:5000/predict -H
    "Content-Type: application/json" -d "{\"features\": [5.1, 3.5, 1.4, 0.2]}"
    
Step 2: Optional Azure Deployment
- Configure Azure Workspace
1. Azure Setup: Ensure that your Azure credentials are properly configured in a config.json file.
- Register and Deploy the Model on Azure
2. Azure Deployment:
- Uncomment the azure_register_and_deploy() function in main.py and rerun:
    ```bash
     python main.py
This process will register the model and deploy it on Azure, providing an endpoint URL upon successful deployment.

- Code Structure
    ```
    ├── main.py            # Main script for training, API, and Azure deployment
    ├── data
    │   └── dataset.csv    # Sample dataset (replace with your data)
    └── src
        └── app.py         # Entry script for Azure deployment


- Contributing :
Feel free to submit issues or pull requests to suggest improvements or additional features.

- License :
This project is licensed under the MIT License.

- Acknowledgments :
Azure Machine Learning for cloud deployment
Flask for API framework


