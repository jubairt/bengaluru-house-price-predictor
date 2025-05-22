# 🏡 Bengaluru House Price Prediction

This project predicts house prices in Bengaluru using Linear Regression and other ML models. It helps users estimate property values based on inputs like location, BHK, bathroom count, and square footage.

---

## 📌 Objective

Predict housing prices (in Lakhs INR) based on features like:

- Size (sqft)
- Number of BHKs
- Number of bathrooms
- Location

---

## 🧠 Problem Type

- **Type**: Regression  
- **Target**: Price (continuous value)

---

## 📂 Dataset

- **Source**: [Kaggle - Bengaluru House Price Data](https://www.kaggle.com/amitabhajoy/bengaluru-house-price-data)

---

## 🧹 Data Cleaning

- Handled missing values  
- Dropped irrelevant features:  
  - `area_type`, `availability`, `society`, `balcony`

---

## 🛠 Feature Engineering

- Converted `size` (e.g., "2 BHK") into a numeric `BHK` column  
- Converted range values like `'2100 - 2850'` into their averages  
- Applied **One-Hot Encoding** on the `location` column

---

## 📊 Exploratory Data Analysis (EDA)

- **Visuals**: Scatter plots of BHK vs sqft and BHK vs price  
- **Outliers**:  
  - Removed rows with extreme bathroom counts (e.g., > 10)  
  - Filtered inconsistent pricing for similar square footage

---

## 🧮 Modeling

### ✅ Algorithm

- Linear Regression (main model)  
- Lasso Regression and Decision Tree (for comparison)

### 🎯 Features Used

- `total_sqft`  
- `bath`  
- `bhk`  
- Encoded `location`

### 🔍 Evaluation

- **Train-Test Split**: `train_test_split()`  
- **Cross Validation**: `ShuffleSplit`  
- **Metrics**:  
  - R² Score  
  - Mean Squared Error (MSE)  
- **Model Tuning**: Used `GridSearchCV` to compare models and select the best

---

## 🌐 Web App

### Frontend

- Built using HTML/CSS and JavaScript  
- Inputs:  
  - Location (drop-down)  
  - BHK  
  - Bathroom  
  - Total Square Feet

### Backend

- Flask API  
- Loads trained model from `.pkl` file  
- Handles input and returns predicted price

---

## 📤 Output

- Returns the predicted house price (in Lakhs INR) based on user input

---

## 📁 Project Structure

```
├── data/
│   └── Bengaluru_House_Data.csv
├── model/
│   ├── model.pkl
│   └── columns.json
├── app.py
├── index.html
├── styles.css
├── script.js
└── README.md
```

---

## 🛠 Technologies Used

- Python  
- Pandas, NumPy, scikit-learn  
- Matplotlib/Seaborn (for EDA)  
- Flask (backend)  
- HTML/CSS/JS (frontend)

---

## 🚀 Run the Project Locally

```bash
# Install dependencies
pip install -r requirements.txt

# Run Flask app
python app.py
```

Open your browser and go to: `http://127.0.0.1:5000/`

---

## 📌 Notes

- The model was selected using cross-validation and hyperparameter tuning.  
- Predictions are for educational/demo purposes only and not real-market prices.

---

## 📬 Contact

If you have questions or want to contribute, feel free to reach out or create a pull request.

---

⭐ *Give the repo a star if you found it helpful!*
