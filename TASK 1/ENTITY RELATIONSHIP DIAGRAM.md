# Comprehensive Measure of Wellbeing

This repository hosts a Machine Learning-driven Human Development Index (HDI) Prediction System designed to track, model, and visualize global wellbeing metrics.

## 📊 Task 1: Entity Relationship (ER) Diagram

The architecture below defines how user sessions, machine learning models, datasets, and target wellbeing (HDI) predictions interact structurally within our system.

```mermaid
erDiagram
    USER {
        int user_id PK
        string name
        string email
        string role
    }
    COUNTRY {
        int country_id PK
    }
    HDI_INPUT_DATA {
        int input_id PK
        int user_id FK
        int country_id FK
    }
    ML_MODEL {
        int model_id PK
        int dataset_id FK
    }
    HDI_PREDICTION {
        int prediction_id PK
        int input_id FK
        int model_id FK
    }
    DATASET {
        int dataset_id PK
    }
    VISUALIZATION_REPORT {
        int report_id PK
        int prediction_id FK
    }
    SESSION {
        int session_id PK
        int user_id FK
    }

    USER ||--o{ HDI_INPUT_DATA : "submits"
    COUNTRY ||--o{ HDI_INPUT_DATA : "has records"
    HDI_INPUT_DATA ||--|| HDI_PREDICTION : "generates"
    ML_MODEL ||--o{ HDI_PREDICTION : "produces"
    HDI_PREDICTION ||--o{ VISUALIZATION_REPORT : "generates"
    DATASET ||--o{ ML_MODEL : "trains"
    USER ||--o{ SESSION : "has"
## 🛠️ Technologies & Tools Used

Our machine learning pipeline, visualization tools, and web interface are powered by the following industry-standard technologies:

| Tool / Library | Role in Project | Documentation |
| :--- | :--- | :--- |
| **Anaconda Navigator** | Environment & package management for clean setup | [Download](https://www.anaconda.com/download) |
| **PyCharm** | Primary IDE used for clean Python development and debugging | [Docs](https://www.jetbrains.com/pycharm/) |
| **NumPy** | High-performance numerical grid arrays and vector operations | [Docs](https://numpy.org/doc/stable/) |
| **Pandas** | Critical data cleaning, manipulation, and analysis tables | [Docs](https://pandas.pydata.org/docs/) |
| **Scikit-learn** | Implementing training, regression, and classification ML models | [Docs](https://scikit-learn.org/stable/) |
| **Matplotlib** | Generating baseline statistical plots and data graphs | [Docs](https://matplotlib.org/stable/) |
| **Seaborn** | Creating beautiful, advanced statistical data visualizations | [Docs](https://seaborn.pydata.org/) |
| **Flask** | Lightweight web framework used to serve our ML predictions as a web app | [Docs](https://flask.palletsprojects.com/) |
