## 🗺️ Project Workflow Roadmap

Below is the structured, step-by-step roadmap we are executing to take this project from raw data to a production-ready Flask application.

### 📍 Epic 1: Environment Setup & Workspace Organization
- [x] **Story 1:** Download and install Python environments, machine learning libraries, and Flask dependencies.
- [x] **Story 2:** Structure the workspace directory cleanly:
  ```text
  ├── data/             # Raw & processed datasets
  ├── models/           # Saved serialized ML models (.pkl)
  ├── templates/        # HTML front-end layouts
  ├── static/           # CSS/JS styling and images
  └── app.py            # Flask server code
📍 Epic 2: Importing Core Libraries[x] Story 1: Initialize the development workspace by importing standard analytical modules (numpy, pandas), visualization tools (matplotlib, seaborn), model utilities (sklearn), saving engines (pickle), and hosting pipelines (flask).
📍 Epic 3: Dataset Ingestion & EDA[ ] Story 1: Retrieve the primary dataset from Kaggle and load it into the program.[ ] Story 2: Conduct structural data checks (data types, features, targets).[ ] Story 3: Generate statistical graphs to expose underlying features, correlations, and trends.
📍 Epic 4: Data Preprocessing & Feature Engineering[ ] Story 1: Define the target dependent variable ($y$) and independent predictor features ($X$).[ ] Story 2: Check for missing or corrupted data points and apply statistical imputation.[ ] Story 3: Perform Label Encoding to transform textual categories into model-ready numerical values.[ ] Story 4: Package the finalized, clean dataset.
📍 Epic 5: Splitting the Dataset[ ] Story 1: Partition the master data into dedicated Training (80%) and Testing (20%) subsets to prevent model overfitting.
📍 Epic 6: Model Training & Evaluation (Linear Regression)[ ] Story 1: Initialize and train a Linear Regression model using the training subset.[ ] Story 2: Run predictions against unseen test data.[ ] Story 3: Assess prediction accuracy using standard mathematical regression metrics (MAE, MSE, R-squared).
📍 Epic 7: Serializing & Saving the Model[ ] Story 1: Package the fully-trained model into a local binary file using the Pickle library.[ ] Story 2: Export the saved model artifact to the /models/ directory for application integration.
📍 Epic 8: Web Application Development (Flask)[ ] Story 1: Code a Flask server that processes user-submitted parameters, feeds them to our saved model, and returns predicted results.[ ] Story 2: Construct a user-friendly UI using HTML forms.[ ] Story 3: Launch, test, and debug the local web host to confirm accurate end-to-end performance.
