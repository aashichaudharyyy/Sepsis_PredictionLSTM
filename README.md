# 🧠 Early Sepsis Prediction using Deep Learning (PyTorch LSTM)

> 🚨 Predicting sepsis **6 hours before onset** using ICU time-series data
> ⚡ Achieved **AUROC: 0.9341** | **57× improvement over baseline AUPRC**

---

## 🌟 Why This Project Matters

Sepsis is responsible for **~20% of global deaths**, and every hour of delay in treatment significantly increases mortality risk.

This project builds a **real-world early warning system** using machine learning to detect sepsis *before clinical deterioration*, enabling faster intervention and better patient outcomes.

---

## 🚀 Highlights

* 🔥 Built an **end-to-end ML pipeline** on real ICU data (40K+ patients)
* 🧠 Implemented **LSTM for temporal pattern learning**
* ⚖️ Tackled **extreme class imbalance (0.87%)**
* 📊 Compared deep learning vs traditional ML (Logistic Regression)
* 🎯 Achieved **state-of-the-art level performance on PhysioNet dataset**

---

## 📊 Results That Matter

| Model               | AUROC      | AUPRC      | Recall    | Precision |
| ------------------- | ---------- | ---------- | --------- | --------- |
| Logistic Regression | 0.6377     | 0.0152     | 56.7%     | 1.3%      |
| **LSTM (PyTorch)**  | **0.9341** | **0.4963** | **68.3%** | **32.5%** |

### 💡 Key Takeaways

* LSTM captures **temporal deterioration patterns** → massive performance boost
* **AUPRC improved ~57×** → crucial for imbalanced medical data
* Significant reduction in **false positives** and improved detection

---

## 🧠 How It Works

### 📥 Data

* **PhysioNet 2019 ICU Dataset**
* 40,336 patients | 1M+ hourly records
* 47 features (clinical + engineered)

---

### ⚙️ Pipeline

1. **Data Preprocessing**

   * Missing value imputation
   * Z-score normalization
   * Leakage prevention

2. **Feature Engineering**

   * Shock Index (HR/SBP)
   * qSOFA proxy score
   * Hypotension & temperature flags
   * Rolling averages (3-hour trends)

3. **Sequence Modeling**

   * 12-hour sliding window
   * 6-hour early prediction target

---

## 🤖 Models

### 🔹 Logistic Regression (Baseline)

* Interpretable
* Uses last timestep snapshot
* Handles imbalance via class weights

### 🔹 LSTM (PyTorch)

* 2-layer LSTM (Hidden = 64)
* Dropout = 0.3
* Adam optimizer + LR scheduler
* Gradient clipping for stability
* Learns **temporal dependencies in patient vitals**

---

## ⚠️ Real-World Challenges Solved

* 🚨 Extreme class imbalance (0.87% positive cases)
* 🧩 Missing data (~94.8% lab values)
* ⏳ Time-series complexity in healthcare data

---

## 📈 Key Insights

* Temporal trends > static values (rolling vitals are critical)
* Deep learning significantly outperforms linear models
* Important predictors:

  * Calcium
  * Troponin
  * Creatinine
  * Heart rate trends

---

## 🛠 Tech Stack

* Python
* PyTorch
* Pandas, NumPy
* Scikit-learn
* Matplotlib

---

## 📂 Project Structure

```
📁 Sepsis_PredictionLSTM
 ┣ 📓 sepsis_prediction_lstm.ipynb
 ┣ 📄 README.md
```

---

## 🎯 Impact

This project demonstrates how deep learning can be applied to **clinical decision support systems**, helping in:

* Early disease detection
* Reducing ICU mortality
* Improving healthcare efficiency

---

## 🙌 Acknowledgment

* PhysioNet (CinC 2019 Dataset)
* PyTorch & open-source ML ecosystem

---

## 👩‍💻 Author

**Aashi Chaudhary**
B.Tech Computer Science
Aspiring Data Scientist | ML & AI Enthusiast

---

## ⭐ If you found this interesting

Give it a ⭐ on GitHub — it helps a lot!

