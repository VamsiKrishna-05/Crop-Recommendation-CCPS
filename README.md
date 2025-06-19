"A Novel DAG-Based SVM Model for Crop Recommendation Using Fruit Fly Optimization on Soil and Climate Features"

# 🌾 Crop Recommendation using Soil and Climate Data

This project proposes a novel machine learning pipeline for **crop recommendation** based on **soil nutrient analysis** and **seasonal weather patterns**. It compares traditional ML algorithms with a custom **MSVM-DAG-FFO model** designed for high accuracy and robust multi-class classification.

📄 Project Summary
The dataset used for this crop recommendation project comprises various soil and environmental parameters such as nitrogen, phosphorus, potassium, soil pH, humidity, rainfall, and temperature, covering multiple crop types. A significant challenge in this dataset is the severe class imbalance, where some crops have many more samples than others, making it difficult for standard machine learning models to accurately predict minority classes. To address this, we experimented with a range of models including classical classifiers (Logistic Regression, Decision Tree, SVM), ensemble methods (Random Forest, Balanced Random Forest, EasyEnsemble), neural networks with focal loss, hierarchical models that separate majority and minority classes, and finally our proposed MSVM-DAG-FFO model. These models were chosen to explore diverse strategies for handling imbalance and improving classification accuracy. The MSVM-DAG-FFO model consistently outperformed all others, demonstrating its robustness and effectiveness in managing imbalanced multi-class crop recommendation tasks.
---

## 🚀 Key Features

- 🔍 Soil + Weather integrated feature set (N, P, K, pH, temp, rainfall, etc.)
- ✅ Class balancing with **SMOTE**
- 🧠 Custom SVM-DAG with **Fruit Fly Optimization (FFO)** for hyperparameter tuning
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
| **Model**                           | **Accuracy** | **Weighted F1** |
| ----------------------------------- | ------------ | --------------- |
| **MSVM-DAG-FFO (Proposed)**         | **0.9964**   | **0.9964**      |
| LightGBM (class\_weight='balanced') | 0.4483       | 0.4528          |
| Random Forest (weighted)            | 0.4393       | 0.4404          |
| Hierarchical Model (sklearn)        | 0.4186       | 0.4381          |
| MLPClassifier                       | 0.3682       | 0.3886          |
| Focal Loss (PyTorch model)          | 0.3837       | 0.3986          |
| Decision Tree (weighted)            | 0.3204       | 0.3363          |
| SVM (weighted)                      | 0.2791       | 0.3206          |
| Balanced Random Forest              | 0.2364       | 0.2693          |
| Logistic Regression (weighted)      | 0.1912       | 0.2184          |
| EasyEnsembleClassifier              | 0.1899       | 0.2212          |


🛠️ How to Run
Clone this repo:
```
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```
Run the notebooks in the notebooks/ folder:

MSVM_DAG_FFO_Model.ipynb for the main model

