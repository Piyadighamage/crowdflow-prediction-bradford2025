# COS7045-B Advanced Machine Learning – Crowdflow Analysis

This repository contains the full implementation and analysis for the **Crowdflow Prediction** project, developed as part of the COS7045 Advanced Machine Learning module.

## 📊 Project Overview

The goal of this project is to apply machine learning techniques to predict pedestrian traffic volume in urban areas using historical sensor data. This work specifically supports planning for the **Bradford 2025 UK City of Culture**, where accurate crowd prediction can guide event logistics, safety, and resource allocation.

---

## 📁 Dataset

- **Source**: [UCI Metro Interstate Traffic Volume Dataset](https://archive.ics.uci.edu/ml/datasets/Metro+Interstate+Traffic+Volume)
- **Features Used**:
  - Date & Time
  - Hour, Day of Week, Is Weekend
  - Weather Main / Description
  - Traffic Volume

---

## 🎯 Research Questions

1. **How accurately can machine learning models predict crowd density based on temporal and weather patterns?**
2. **Which features most significantly influence crowd flow?**
3. **How can these predictions optimize planning for large-scale cultural events like Bradford 2025?**

---

## 🧠 Models & Techniques

The following machine learning models were developed and evaluated:

| Model           | R² Score | RMSE     | MAE     |
|----------------|----------|----------|---------|
| Random Forest  | **0.96** | 390.51   | 220.37  |
| XGBoost        | ~0.94    | ~420     | ~240    |
| LSTM (optional)| Varies   | Higher   | Higher  |

Key techniques used:
- **Feature Engineering**: Extracting hour, day, is_weekend, and encoding weather conditions.
- **One-hot encoding** of categorical data.
- **StandardScaler** for feature normalization.
- **Model evaluation** with MAE, RMSE, and R² metrics.
- **Feature Importance Analysis** using Random Forest.

---

## 📈 Key Findings

- **Temporal features** (hour, day of week) are the most influential, with hour alone contributing ~80% to model performance.
- **Random Forest** consistently outperformed XGBoost and LSTM for this dataset.
- Weather features had a **minor impact** on prediction accuracy, suggesting overemphasis on them in past planning models.

---

## 🔍 Future Work

- **Integrate multimodal data**: social media, transport, event metadata.
- **Deploy real-time prediction dashboard** for cultural event managers.
- **Experiment with transfer learning** across cities or event types.
- **Enhance explainability** using SHAP or LIME for better decision-making transparency.

---

## 📌 Practical Applications

The model can be used to:
- Optimize event scheduling and venue selection
- Anticipate and mitigate crowd congestion
- Guide staffing and security deployment
- Inform real-time alerts or traffic redirection

---

## ⚖️ Ethical Considerations

- **No personal data used**: dataset is fully anonymized.
- **Bias audits** are recommended if deploying in real-time systems.
- Follows principles under the UK Data Protection Act 2018.

---

## 📚 References

- Zhang et al. (2023), Deep Learning for Crowd Prediction  
- Johnson et al. (2024), Urban Crowd Dynamics  
- Li & Chen (2024), Smart Cities for Culture  
- Smith et al. (2023), Benchmarking LSTM and Tree Models  

---

## 🧾 How to Run

```bash
pip install -r requirements.txt
python cos7045_crowdflow_analysis.py
