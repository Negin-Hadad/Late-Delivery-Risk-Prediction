# Late Delivery Risk Prediction

Predicts the probability of **late delivery** using order flow data. This is a **baseline ML pipeline** with logistic regression and exploratory analysis.

---

## Getting Started

### 1. Install Dependencies

```bash
# Linux / Mac
pip install -r requirements.txt

# Windows
py -m pip install -r requirements.txt
```

### 2. Prepare Data
Modify the path of `orders_spring_2022.csv` file in the notebook as follows:

```python
DATA_PATH = "[INSERT_PROJECT_BASE_PATH]/data/orders_spring_2022.csv"
```

### 3. Run the Pipeline

- Open `late_delivery_risk_modeling.ipynb` in Jupyter or Google Colab.
- Run cells in order from top to bottom.
