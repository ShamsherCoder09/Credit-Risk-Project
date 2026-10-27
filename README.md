Credit Risk Assessment & Prediction 📊🏦

An end-to-end Machine Learning project designed to predict credit risk and loan default probability. This project covers the entire data science lifecycle, from Exploratory Data Analysis (EDA) and data preprocessing to model training and the deployment of a user-friendly web interface.

🚀 Project Overview

The objective of this project is to assess the risk of a person defaulting on a loan based on their financial and personal history. It utilizes an advanced Machine Learning pipeline (XGBoost + Calibrated Classifier) on the backend, paired with an interactive static web frontend (HTML, CSS, JS) where users can input data and receive instant risk evaluations.

🛠️ Tech Stack

Frontend:

HTML5 (index.html)

CSS3 (style.css for styling)

JavaScript (script.js for handling form logic and API calls)

Backend & Machine Learning:

Python 3

XGBoost: Primary classification algorithm (XGBClassifier).

Scikit-Learn: For constructing the data pipeline, imputation (SimpleImputer), encoding (OneHotEncoder), and model calibration (CalibratedClassifierCV).

NumPy & Pandas: Data manipulation and analysis.

📂 Project Structure

credit-risk-project/
├── static/
│   ├── css/
│   │   └── style.css          # Frontend styling
│   ├── js/
│   │   └── script.js          # Client-side validation and logic
│   └── index.html             # Main user interface
├── data/
│   └── credit_risk_dataset_3.csv # Training dataset
├── models/
│   └── trained_model.pkl      # Serialized XGBoost pipeline
├── .gitignore_3               # Git ignore rules for Python/pycache
├── app.py                     # Backend server (Flask/FastAPI) to serve the model
└── README.md                  # Project documentation


🧠 Model Pipeline Details

Based on the project's architecture, the data undergoes a robust preprocessing pipeline before making predictions:

Numerical Features:

Includes: person_age, person_income, person_emp_length, loan_amnt, loan_int_rate, loan_percent_income, cb_person_cred_hist_length.

Handling: Missing values are imputed using the Median strategy.

Categorical Features:

Includes: person_home_ownership, loan_intent, loan_grade, cb_person_default_on_file.

Handling: Transformed using One-Hot Encoding.

Classifier: The preprocessed data is fed into an XGBoost Classifier, which is further wrapped in a CalibratedClassifierCV to output reliable probability scores instead of just binary predictions.

⚙️ Setup & Installation

Follow these steps to run the project locally on your machine:

Clone the repository:

git clone https://github.com/yourusername/credit-risk-project.git
cd credit-risk-project


Set up a virtual environment (Recommended):

python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`


Install the required dependencies:

pip install -r requirements.txt


(Ensure scikit-learn, xgboost, pandas, numpy, and your web framework like flask are included).

Run the Application:

python app.py


Access the Frontend:
Open your browser and navigate to https://credit-risk-project-cove.onrender.com/ (or the port specified by your backend).

💡 How to Use

Open the web interface.

Fill in the applicant's financial and personal details in the form.

Click on the "Predict" or "Analyze" button.

The JavaScript will send the data to the backend model, which will return the probability of loan default and a safe/risky classification.

🔮 Future Improvements

Add a database to store historical predictions.

Implement user authentication for bank employees.

Enhance the EDA section with interactive dashboards (e.g., Plotly/Dash) accessible from the UI.
