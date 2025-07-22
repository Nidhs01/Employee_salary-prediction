# 💼 Employee Salary Predictor

This project is a **Machine Learning model** to predict employee salaries based on features like age, experience, job title, education, and location.  
It is built as part of a **capstone internship project** to demonstrate practical use of regression, data preprocessing, and deployment with **Streamlit**.

---

## 📌 **Project Structure**

- `Employee_salary_prediction.ipynb` — Jupyter notebook with all steps
- `employee_salary_prediction.py` — Python script version of the pipeline
- `adult 3.csv.xlsx` — Source dataset (replace with your own dataset if needed)
- `employee_salary_model.pkl` — Saved trained Random Forest model

---

## ⚙️ **Workflow**

### 1️⃣ **Data Collection**
- Loads employee dataset from `adult 3.csv.xlsx`.

### 2️⃣ **Data Preprocessing**
- Handles missing values.
- Encodes categorical features using `OneHotEncoder`.
- Standardizes numeric features with `StandardScaler`.

### 3️⃣ **Model Building**
- Splits the data into training and testing sets.
- Builds a `Pipeline` with preprocessing and `RandomForestRegressor`.
- Trains a simple Random Forest (10 trees, max depth 3 for speed).

### 4️⃣ **Model Evaluation**
- Evaluates model using **Mean Absolute Error (MAE)** and **R² Score**.
- Visualizes results with a scatterplot (Actual vs Predicted).

### 5️⃣ **Model Serialization**
- Saves the trained pipeline as `employee_salary_model.pkl` for deployment.

---

## 🚀 **Deployment**

This project is designed to be deployed with **Streamlit**:

1. Create a `streamlit_app.py` that:
   - Loads `employee_salary_model.pkl`.
   - Takes user input (age, experience, job title, education, location).
   - Predicts salary and displays it dynamically.

2. Run locally:
   ```bash
   streamlit run streamlit_app.py
