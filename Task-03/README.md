# 🏠 Housing Price Prediction using Linear Regression

This project predicts house prices using a **Linear Regression model**. It uses a dataset (`Housing.csv`) containing various features such as area, number of bedrooms, bathrooms, furnishing status, and other house characteristics.

---

## 📁 Dataset

The dataset contains the following columns:

- `price`: Target variable (house price)
- `area`: Total area of the house
- `bedrooms`: Number of bedrooms
- `bathrooms`: Number of bathrooms
- `stories`: Number of floors
- `mainroad`: Whether the house is located on the main road
- `guestroom`: Availability of a guestroom
- `basement`: Whether the house has a basement
- `hotwaterheating`: Availability of hot water heating
- `airconditioning`: Whether the house has air conditioning
- `parking`: Number of parking spots
- `prefarea`: Preferred locality
- `furnishingstatus`: Furnishing status (unfurnished/semi-furnished/furnished)

---

## 📊 Exploratory Data Analysis (EDA)

The EDA includes:

- Distribution of **bedrooms** and **bathrooms**
- Pie chart of **mainroad** feature
- Count plot for **furnishing status**

Visualizations are generated using `matplotlib` and `seaborn`.

---

## 🧠 Model Used

- **Linear Regression** from `sklearn.linear_model`
- Categorical features were encoded using **One-Hot Encoding** via `pandas.get_dummies(drop_first=True)`

---

## 📈 Evaluation Metrics

The model was evaluated using:

- **MAE** (Mean Absolute Error)
- **MSE** (Mean Squared Error)
- **R² Score** (Coefficient of Determination)

### 📋 Results

MAE: 970043.40
MSE: 1754318687330.66
R²: 0.65

This shows the model explains **65% of the variance** in house prices.

---

## 📉 Visualization

- **Actual vs Predicted** house prices plotted as a scatter plot
- **Regression coefficients** printed to show how each feature influences the price

---

## 🛠 Dependencies

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`

Install dependencies via:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn