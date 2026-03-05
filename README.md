# Late Delivery Risk Prediction for Order Flow

## 📌 Project Overview
This data science project aims to predict the probability of **late delivery** at the moment an order is placed, using historical order flow data. By framing this as a machine learning risk prediction problem rather than just a delivery time estimation, the model helps operations teams and automated systems proactively manage courier allocation, update customer expectations, and optimize business efficiency.

## 💼 Business & Decision Context
Late deliveries create frustration for customers and inefficiencies for operations. The outputs of this model primarily support:
- **Operations Teams**: Better allocate couriers during peak demand or low supply periods.
- **Product Managers**: Understand patterns in delivery performance.
- **Automated Systems**: Dynamically adjust ETA estimates and flag high-risk orders for early intervention.

## 📊 Data & Feature Engineering
The project utilizes a simulated order flow dataset for Helsinki, containing three months of order-level records (e.g., timestamps, item count, ETAs, courier supply index, and weather conditions). 

Key feature engineering steps include:
- **Time Features**: Hour of day, day of week, weekend indicator, and cyclical encoding for time.
- **Order & ETA Features**: Item count, order category, and ETA uncertainty (upper - lower estimate).
- **Operational Features**: Courier supply index and precipitation. 

## 🧠 Modeling Approach
A **baseline probabilistic Machine Learning pipeline** was built using **Logistic Regression**. This model was chosen for its:
- **Interpretability**: Clear understanding of what drives risk.
- **Stability & Transparency**: Reliable behavior on structured data and easy to explain to stakeholders.
- **Calibration**: Outputs meaningful probabilities rather than just hard class labels.

The model is evaluated as a risk-ranking system using metrics like ROC-AUC and PR-AUC, optimized with a recall-driven decision threshold to effectively catch the most risky orders.

## 🚀 Getting Started

### 1. Install Dependencies
Ensure you have Python installed, then run the following command to install the required data science packages (`pandas`, `numpy`, `matplotlib`, `scikit-learn`):

```bash
# Linux / Mac
pip install -r requirements.txt

# Windows
py -m pip install -r requirements.txt
```

### 2. Prepare Data
Modify the path of the orders_spring_2022.csv file in the notebook to point to your local data directory:

```Python
DATA_PATH = "[INSERT_PROJECT_BASE_PATH]/data/orders_spring_2022.csv"
```

### 3. Run the Pipeline
- Open `late_delivery_risk_modeling.ipynb` in Jupyter Notebook or Google Colab.

- Run the cells in order from top to bottom to execute data loading, exploratory analysis, and model training.

## 📁 Project Structure
`assignment_report_Negin.Hadad.pdf`: Comprehensive project report detailing the problem context, EDA findings, modeling assumptions, and evaluation strategy.

`late_delivery_risk_modeling.ipynb`: The main Jupyter Notebook containing the data science and ML pipeline.

`requirements.txt`: Python package dependencies.

`README.md`: Project documentation.