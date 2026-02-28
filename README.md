# 🎓 Student Success Prediction Using EDA & Machine Learning

This project applies **Exploratory Data Analysis (EDA)** and **Machine Learning models** to predict student academic success based on performance metrics.

---

## 📂 Project Structure

```
Student-Success-Prediction/
│
├── student_performance.csv
├── cleaned_student_data.csv
├── student_performance_analysis.ipynb
├── requirements.txt
└── outputs/
  │
  ├── cleaned_student_data.csv
  ├── confusion_matrix.png
  ├── correlation_heatmap.png
  ├── feature_importances.png
  ├── model_comparison.png
  ├── score_by_schooltype.png
  └── score_distribution.png
```

## 🧠 Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

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


## 📊 Model Performance

| Model | Accuracy | F1 Score | ROC-AUC |
|-------|----------|----------|---------|
| Logistic Regression | 0.54 | 0.49 | 0.54 |
| Random Forest | 0.54 | 0.59 | 0.55 |
| XGBoost | **0.56** | **0.63** | **0.56** |


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

✔ Performed detailed EDA  
✔ Applied hyperparameter tuning (GridSearchCV)  
✔ Compared multiple ML models  
✔ Evaluated using Accuracy, F1-score & ROC-AUC  
✔ Visualized feature relationships  


## 📌 Future Improvements

- Handle class imbalance
- Apply SMOTE
- Deploy using Streamlit
- Convert into API

## 🪪 License

This project is licensed under the [MIT License](./LICENSE) © 2025 \[Sathish R\].

## 👤 Author
- Sathish R B.Tech(Artificial Intelligence and Data Science)
- 📧 Email: [sathxsh57@gmail.com]
- 🌐 GitHub: https://github.com/sathishr-ai
- 💼 LinkedIn: www.linkedin.com/in/sathish-r-2393412a5
