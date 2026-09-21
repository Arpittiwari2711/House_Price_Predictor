# 🏠 House Price Prediction Using Linear Regression

## 📌 Project Overview

**HomeVista Properties** is a real estate company operating across multiple cities and handling thousands of residential property sales every year. The company wants to automate its house pricing process using Machine Learning.

This project develops a **Supervised Machine Learning Regression model** that predicts the selling price of a residential property based on its physical features, location, construction details, and overall condition.

The project uses **Linear Regression** to learn the relationship between historical property characteristics and their final selling prices.

---

# 🎯 Problem Statement

The objective of this project is to build a Machine Learning regression model that can automatically predict the **market price of a house** using historical property data.

The model uses different house-related features such as:

- Type of dwelling
- Zoning classification
- Lot size
- Building type
- Overall condition
- Construction year
- Remodeling year
- Exterior material
- Basement area

The target variable is:

```text
SalePrice

```

---

# 🤖 Machine Learning Approach

This project follows the following Machine Learning approach:

```text
Supervised Learning
        ↓
Regression
        ↓
Linear Regression

```

Since `SalePrice` is a continuous numerical variable, this problem is treated as a **Regression Problem**.

## 🔄 Prediction Workflow

```text
House Property Data
        ↓
Data Loading
        ↓
Data Exploration
        ↓
Data Preprocessing
        ↓
Feature Engineering
        ↓
Categorical Encoding
        ↓
Train-Test Split
        ↓
Linear Regression Model
        ↓
Price Prediction
        ↓
Model Evaluation

```

---

# 📊 Dataset

The project uses the following dataset:

**Dataset Name:** `HousePricePrediction.csv`

Each row in the dataset represents one residential house along with its physical, location, and construction details.

## 📋 Dataset Features

| FeatureDescription |                                                              |
| ------------------ | ------------------------------------------------------------ |
| `Id`               | Unique identification number for each house                  |
| `MSSubClass`       | Type/class of dwelling involved in the sale                  |
| `MSZoning`         | General zoning classification                                |
| `LotArea`          | Lot size in square feet                                      |
| `LotConfig`        | Lot configuration such as Inside, Corner, Cul-de-sac, etc.   |
| `BldgType`         | Type of dwelling such as 1Fam, 2Fam, Duplex, Townhouse, etc. |
| `OverallCond`      | Overall condition rating of the house on a scale of 1–10     |
| `YearBuilt`        | Original construction year                                   |
| `YearRemodAdd`     | Year the house was remodeled or additions were made          |
| `Exterior1st`      | Exterior covering/material of the house                      |
| `BsmtFinSF2`       | Type 2 finished basement area                                |
| `TotalBsmtSF`      | Total basement area in square feet                           |
| `SalePrice`        | Final selling price of the house — **Target Variable**       |

---

# 🎯 Features and Target

## Input Features

The model uses the following property features:

```text
MSSubClass
MSZoning
LotArea
LotConfig
BldgType
OverallCond
YearBuilt
YearRemodAdd
Exterior1st
BsmtFinSF2
TotalBsmtSF

```

## Target Variable

```text
SalePrice

```

`SalePrice` represents the final selling price of the residential property and is the value that the model is trained to predict.

> The `Id` column is an identifier and is not treated as a meaningful predictive feature.

---

# 🧹 Data Preprocessing

Before training the Machine Learning model, the dataset is prepared through several preprocessing steps.

## Data Inspection

The dataset is examined to understand:

- Number of rows and columns
- Data types
- Missing values
- Duplicate records
- Statistical summary
- Numerical and categorical features

## Handling Missing Values

Missing values are identified and handled appropriately before model training.

## Categorical Feature Encoding

The dataset contains categorical variables such as:

```text
MSZoning
LotConfig
BldgType
Exterior1st

```

These categorical features need to be converted into numerical representations before being provided to the Linear Regression model.

**One-Hot Encoding** can be used to transform categorical variables into numerical features.

## Feature Selection

The `Id` column is treated as an identifier rather than a predictive feature and is excluded from the model.

---

# 📈 Exploratory Data Analysis

Exploratory Data Analysis (EDA) is performed to understand the dataset and identify relationships between property characteristics and house prices.

The analysis includes:

- Distribution of house prices
- Distribution of numerical features
- Correlation analysis
- Feature-price relationships
- Categorical feature analysis
- Identification of potential outliers
- Visualization of important patterns

## 📊 Visualizations

The project may include visualizations such as:

- Histograms
- Box plots
- Scatter plots
- Correlation heatmap
- Bar charts
- Actual vs. predicted price plots

---

# ✂️ Train-Test Split

The dataset is divided into two parts:

### Training Dataset

Used to train the Linear Regression model and learn relationships between the input features and `SalePrice`.

### Testing Dataset

Used to evaluate how well the trained model performs on previously unseen data.

```text
Dataset
   │
   ├── Training Data → Model Training
   │
   └── Testing Data  → Model Evaluation

```

---

# 🤖 Linear Regression Model

The main Machine Learning algorithm used in this project is:

**Linear Regression**

Linear Regression attempts to model the relationship between the input features and the target house price.

The model learns coefficients for the input features and uses them to estimate the selling price of a house.

### Model

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X_train, y_train)

```

The trained model is then used to predict house prices:

```python
y_pred = model.predict(X_test)

```

---

# 📏 Model Evaluation

The performance of the Linear Regression model is evaluated using standard regression metrics.

## 1. Mean Absolute Error (MAE)

MAE measures the average absolute difference between actual and predicted house prices.

A lower MAE indicates smaller prediction errors.

## 2. Mean Squared Error (MSE)

MSE calculates the average squared difference between actual and predicted values.

A lower MSE indicates better prediction performance.

## 3. Root Mean Squared Error (RMSE)

RMSE is the square root of MSE and represents prediction error in the same unit as the target variable.

A lower RMSE indicates better model performance.

## 4. R² Score

R² measures how much of the variation in house prices is explained by the model.

A value closer to `1` indicates that the model explains a larger proportion of the variation in the target variable.

---

# 📉 Model Performance

The final model performance is evaluated using:

| MetricDescription |                              |
| ----------------- | ---------------------------- |
| **MAE**           | Mean Absolute Error          |
| **MSE**           | Mean Squared Error           |
| **RMSE**          | Root Mean Squared Error      |
| **R² Score**      | Coefficient of Determination |

> Actual metric values can be added here after the final model is executed.

---

# 📊 Actual vs Predicted Prices

The project can visualize the relationship between actual and predicted house prices.

```text
Actual SalePrice
       vs.
Predicted SalePrice

```

A scatter plot can be used to visually examine how closely the predictions follow the actual selling prices.

---

# 🛠️ Technologies Used

## Programming Language

- **Python**

## Libraries

- **NumPy** — Numerical computation
- **Pandas** — Data manipulation and analysis
- **Matplotlib** — Data visualization
- **Seaborn** — Statistical visualization
- **Scikit-learn** — Machine Learning and model evaluation
- **Jupyter Notebook** — Development and experimentation environment

---

# 📁 Project Structure

```text
House-Price-Prediction/
│
├── HousePricePrediction.csv
│
├── House_Price_predictor.ipynb
│
├── requirements.txt
│
└── README.md

```

## 📄 File Description

### `HousePricePrediction.csv`

Contains the historical residential property data used for training and evaluating the Machine Learning model.

### `House_Price_predictor.ipynb`

Jupyter Notebook containing the complete Machine Learning workflow, including:

- Data loading
- Data inspection
- Data preprocessing
- Exploratory Data Analysis
- Feature engineering
- Model training
- Price prediction
- Model evaluation
- Data visualization

### `requirements.txt`

Contains the Python libraries required to run the project.

### `README.md`

Project documentation containing information about the problem statement, dataset, methodology, implementation, and Machine Learning approach.

---

# ⚙️ Installation and Setup

## 1. Clone the Repository

```bash
git clone https://github.com/Arpittiwari2711/REPOSITORY-NAME.git

```

## 2. Navigate to the Project Directory

```bash
cd REPOSITORY-NAME

```

## 3. Create a Virtual Environment

```bash
python -m venv venv

```

## 4. Activate the Virtual Environment

### Windows

```bash
venv\Scripts\activate

```

### macOS/Linux

```bash
source venv/bin/activate

```

## 5. Install Dependencies

```bash
pip install -r requirements.txt

```

## 6. Start Jupyter Notebook

```bash
jupyter notebook

```

## 7. Open the Notebook

Open:

```text
House_Price_predictor.ipynb

```

Run the notebook cells sequentially to execute the complete project.

---

# 📦 Requirements

The project requires the following Python libraries:

```text
numpy
pandas
matplotlib
seaborn
scikit-learn
jupyter

```

These dependencies can be installed using:

```bash
pip install -r requirements.txt

```

---

# 🔮 Future Improvements

Although this project focuses on Linear Regression, the model can be further improved by experimenting with:

- Feature selection
- Feature engineering
- Outlier detection and treatment
- Log transformation of skewed variables
- Ridge Regression
- Lasso Regression
- Decision Tree Regression
- Random Forest Regression
- Gradient Boosting
- Cross-validation
- Hyperparameter tuning
- Model comparison
- Model deployment using Streamlit or Flask

---

# 🎓 Learning Outcomes

This project provides practical experience with:

- Supervised Machine Learning
- Regression problems
- Linear Regression
- Data preprocessing
- Exploratory Data Analysis
- Handling numerical and categorical data
- One-Hot Encoding
- Feature selection
- Train-test splitting
- Model training
- Model prediction
- Regression evaluation metrics
- Data visualization
- Model interpretation

---

# 💡 Conclusion

This project demonstrates how **Supervised Machine Learning** can be applied to a real-world real estate problem.

By using historical property data and a **Linear Regression** model, the system attempts to learn the relationship between house characteristics and their selling prices.

The project covers the complete Machine Learning pipeline, from **data preprocessing and exploratory analysis to model training, prediction, and evaluation**.

The approach provides a foundation for developing more advanced and accurate house-price prediction systems using additional Machine Learning algorithms and feature engineering techniques.

---

# 👨‍💻 Author

## Arpit Tiwari


# 📜 License

This project is created for **educational and academic purposes** as part of a **Supervised Machine Learning Assignment**.
