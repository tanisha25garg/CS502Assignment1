# CS502 Assignment – 1  

---

## 📌 Overview  
This assignment demonstrates the use of **Logistic Regression** on the **Breast Cancer Wisconsin dataset**.  
The task is to classify tumors as **Malignant (cancerous)** or **Benign (non-cancerous)** based on 30 features extracted from cell nuclei images.  

---

## 📂 Dataset  
- **Source:** [Breast Cancer Wisconsin Dataset (UCI ML Repository via Kaggle)](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)  
- **Download Method:** [`kagglehub`](https://pypi.org/project/kagglehub/)  
- **Total Records:** 569  
- **Features:** 30 (radius, texture, smoothness, concavity, etc.)  
- **Target Variable:**  
  - `M → 1` (Malignant)  
  - `B → 0` (Benign)  

---

## ⚙️ Methodology  
1. **Data Collection**  
   - Dataset downloaded using `kagglehub`.  

2. **Data Preprocessing**  
   - Dropped irrelevant columns (`id`, `Unnamed: 32`).  
   - Encoded target values (M=1, B=0).  
   - Standardized features using `StandardScaler`.  

3. **Data Splitting**  
   - **85%** → Training + Validation  
   - **15%** → Test  
   - From Training, **15%** further used as Validation  
   - Final split:  
     - Training Set: ~70%  
     - Validation Set: ~15%  
     - Test Set: ~15%  

4. **Model Training**  
   - Logistic Regression model with hyperparameter tuning using `GridSearchCV`.  
   - Parameters tested: `C = [0.01, 0.1, 1, 10, 100]`.  

5. **Model Evaluation**  
   - Accuracy, Classification Report, Confusion Matrix.  
   - Visualization using **Seaborn heatmap**.  

---

## 📊 Results  
- **Best Hyperparameters:** Found using GridSearchCV  
- **Validation Accuracy:** ~97%  
- **Test Accuracy:** ~98%  
- **Conclusion:** Logistic Regression proved highly effective for binary medical classification tasks.  

---

## 🚀 How to Run  

1. Clone this repository:  
   ```bash
   git clone https://github.com/tanisha25garg/CS603Assignment1.git
   cd CS603Assignment1

2. Run the script:
   ```bash
   python Assignment1_Code.ipynb

---

## ✨ Author

Tanisha Garg - 2201AI40

B.Tech - Artificial Intelligence and Data Science
