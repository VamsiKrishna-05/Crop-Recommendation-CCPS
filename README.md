"A Novel DAG-Based SVM Model for Crop Recommendation Using Fruit Fly Optimization on Soil and Climate Features"

# 🌾 Crop Recommendation using Soil and Climate Data

This project proposes a novel machine learning pipeline for **crop recommendation** based on **soil nutrient analysis** and **seasonal weather patterns**. It compares traditional ML algorithms with a custom **MSVM-DAG-FFO model** designed for high accuracy and robust multi-class classification.

---

## 🚀 Key Features

- 🔍 Soil + Weather integrated feature set (N, P, K, pH, temp, rainfall, etc.)
- ✅ Class balancing with **SMOTE**
- 🧠 Custom SVM-DAG with **Fruit Fly Optimization (FFO)** for hyperparameter tuning
- 📊 Performance comparison with **Random Forest**, **XGBoost**, and **Logistic Regression**
- 📈 Achieved **>99% accuracy** with MSVM-DAG-FFO

---

## 🗂️ Dataset Used

- **File**: `Crop Recommendation using Soil Properties and Weather Prediction.csv`
- **Features**:
  - Soil: N, P, K, pH, S, Zn, Soil Color
  - Weather: Temperature, Humidity, Rainfall (Seasonal)
- **Target**: Crop Label (Multi-class classification)

---

## 📁 Project Structure

```bash
├── dataset/
│   └── Crop Recommendation using Soil Properties and Weather Prediction.csv
├── notebooks/
│   ├── MSVM_DAG_FFO_Model.ipynb
│   ├── Baseline_Models_Comparison.ipynb
├── README.md
```
| Model               | Accuracy | F1 Score |
| ------------------- | -------- | -------- |
| ✅ MSVM-DAG-FFO      | 0.9964   | 0.9964   |
| Random Forest       | \~0.52   | \~0.49   |
| XGBoost             | \~0.51   | \~0.49   |
| Logistic Regression | \~0.47   | \~0.42   |

🛠️ How to Run
Clone this repo:
```
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```
Run the notebooks in the notebooks/ folder:

MSVM_DAG_FFO_Model.ipynb for the main model

Baseline_Models_Comparison.ipynb for RF/XGB/LR results
