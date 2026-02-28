# 🎓 Student Success Prediction Using EDA & Machine Learning

This project applies **Exploratory Data Analysis (EDA)** and **Machine Learning models** to predict student academic success based on performance metrics.

---

## 📂 Project Structure

```
Student-Success-Prediction/
│
├── student_performance.csv          # Raw dataset
├── cleaned_student_data.csv          # Cleaned data after preprocessing
├── student_performance_analysis.ipynb # Main analysis notebook
├── requirements.txt                  # Python dependencies
└── outputs/                          # All generated plots and results
    ├── cleaned_student_data.csv
    ├── cm_Neural_Network_(MLP)_default.png
    ├── cm_Neural_Network_(MLP)_tuned.png
    ├── correlation_heatmap.png
    ├── diagnostics.txt
    ├── feature_importances.png
    ├── model_comparison_tuned.csv
    ├── score_by_schooltype.png
    ├── score_distribution.png
    ├── threshold_impact.png
    └── threshold_tune_*.png
```

## 🧠 Technologies Used

-Python – core language
-NumPy, Pandas – data manipulation
-Matplotlib, Seaborn – data visualization
-Scikit‑learn – machine learning models & preprocessing
-Imbalanced‑learn – SMOTE for handling imbalance
-Jupyter Notebook – interactive analysis

## 🚀 How to Run

```bash
git clone https://github.com/sathish-ai/Student-Success-Prediction-Using-EDA-ML
cd Student-Success-Prediction-Using-EDA-ML
pip install -r requirements.txt
jupyter notebook
```

Open:
```
student_performance_analysis.ipynb
```
Run all cells.

## 📊Dataset & Preprocessing

The dataset contains **1,200 students** with the following features:

- **Demographics:** Gender, Age, School Type, Parental Education, Socioeconomic Status  
- **Behavioral:** Study Hours, Attendance %, Extra Classes, Internet Access, Test Prep Course  
- **Academic:** Previous Score, Final Score  
- **Target:** `Pass` (1 = score ≥ 50, 0 = score < 50)

### Key Observations

- **Class imbalance:** Only about 10% of students fail – accuracy alone is misleading.  
- **Missing values** were filled with mean (numeric) or mode (categorical).  
- **One-hot encoding** applied to categorical variables.  
- **StudentID** dropped to avoid leakage.

---

## ⚖️Handling Class Imbalance

Three main techniques were used:

1. **SMOTE** (Synthetic Minority Oversampling) – applied only on the training set to create synthetic examples of failing students.  
2. **Class weighting** (`class_weight='balanced'`) in models like Logistic Regression, Random Forest, and SVM.  
3. **Threshold tuning** – after training, the optimal probability threshold for predicting the fail class was found on a validation set, maximizing the F1-score for class 0.

---

## 📈 Model Comparison
Six models were evaluated using Macro F1-score and F1-score for the minority class (Fail).
| Model                          | F1 (Fail) Default | F1 (Fail) Tuned | Macro F1  | Best Threshold (Fail) |
| ------------------------------ | ----------------- | --------------- | --------- | --------------------- |
| Neural Network (MLP)           | 0.604             | **0.663**       | **0.777** | 0.332                 |
| Random Forest (balanced)       | 0.600             | 0.641           | 0.777     | 0.386                 |
| Logistic Regression (balanced) | 0.588             | 0.638           | 0.760     | 0.359                 |
| SVM (RBF, balanced)            | 0.582             | 0.638           | 0.764     | 0.365                 |
| Gradient Boosting              | 0.545             | 0.615           | 0.743     | 0.357                 |
| Dummy (most frequent)          | 0.175             | 0.175           | 0.087     | N/A                   |

## Key Findings
- 🏆 Best minority-class F1 (tuned): Neural Network (0.663)
- 🥇 Best Macro F1: Neural Network & Random Forest (0.777)
- 📌 All models significantly outperform the Dummy baseline.

## 📈 Visual Outputs

### 🔹 Model Comparison
<img width="1902" height="856" alt="Screenshot 2026-02-28 190255" src="https://github.com/user-attachments/assets/059517b2-7316-46b1-a95c-7e4e8547ee5f" />

### 🔹 Correlation Heatmap
<img width="1200" height="900" alt="correlation_heatmap" src="https://github.com/user-attachments/assets/8b34d141-643b-4e64-99c9-79362f3fcef9" />

### 🔹 Score Distribution
<img width="1200" height="750" alt="score_distribution" src="https://github.com/user-attachments/assets/74280ec2-8968-459b-902e-7b7891d03be5" />

### 🔹 Score by schooltype
<img width="1050" height="600" alt="score_by_schooltype" src="https://github.com/user-attachments/assets/ea33d068-0780-491a-aa5a-98c142c2ff1d" />

### 🔹 Feature importance
<img width="1200" height="900" alt="feature_importances" src="https://github.com/user-attachments/assets/5e2b9757-aba4-4180-b7d1-8120305d8925" />


## 🎯 Key Highlights

✔ Performed in‑depth EDA to understand data distributions and relationships.
✔ Addressed class imbalance with SMOTE, class weighting, and threshold tuning.
✔ Compared six classification models using appropriate metrics (macro F1, per‑class F1).
✔ Visualised results with professional plots saved in outputs/.
✔ Demonstrated that accuracy alone is misleading – the models truly learn to identify failing students.


## 📌 Future Improvements

- Deploy the best model as a simple web app (Streamlit) for real‑time predictions.
- Feature engineering – create interaction terms or aggregate features.
- Try advanced algorithms like XGBoost (with scale_pos_weight) or LightGBM.
- Cross‑validation for more robust performance estimates.

## 🪪 License

This project is licensed under the [MIT License](./LICENSE) © 2025 \[Sathish R\].

## 👤 Author
- Sathish R B.Tech(Artificial Intelligence and Data Science)
- 📧 Email: [sathxsh57@gmail.com]
- 🌐 GitHub: https://github.com/sathishr-ai
- 💼 LinkedIn: www.linkedin.com/in/sathish-r-2393412a5
