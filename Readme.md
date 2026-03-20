# Customer Retention Analysis (Churn Prediction)

## Deskripsi
Project ini adalah analisis churn prediction pada dataset pelanggan 
perusahaan telekomunikasi. Tujuannya untuk memahami faktor-faktor 
apa yang bikin customer memilih berhenti berlangganan, dan membangun 
model machine learning yang bisa memprediksi customer mana yang 
berpotensi churn.

Project ini merupakan projek data science pertama saya, mencakup 
keseluruhan pipeline dari data cleaning, exploratory data analysis, 
feature engineering, hingga modeling dan evaluasi.

## Dataset
Dataset yang dipakai adalah Telco Customer Churn dari Kaggle.
Link: https://www.kaggle.com/datasets/blastchar/telco-customer-churn

Total data: 7.043 baris, 21 kolom

## Tahapan Project
1. **Data Ingestion**: pemuatan data dan inspeksi awal
2. **Data Cleaning**: handling missing values, standarisasi kategorikal, validasi tipe data
3. **Exploratory Data Analysis (EDA)**: univariate, bivariate, multivariate analysis, class imbalance check, outlier analysis
4. **Feature Engineering & Preprocessing**: categorical encoding, scaling, SMOTE
5. **Modeling**: Logistic Regression, Random Forest, XGBoost

## Hasil
| Model | Accuracy | Recall | ROC-AUC |
|---|---|---|---|
| Logistic Regression | 79% | 82% | 88% |
| Random Forest | 83% | 86% | 91% |
| XGBoost | 83% | 85% | 91% |

Model terbaik: **Random Forest** dengan ROC-AUC 91% dan Recall 85%

## Kesimpulan
Faktor utama yang mempengaruhi churn:
- Tenure (lama berlangganan)
- TotalCharges & MonthlyCharges
- Jenis Contract (month-to-month paling berisiko)

## Key Insights
- Customer dengan tenure rendah (0-20 bulan) + monthly charges tinggi 
  paling berisiko churn
- Kombinasi month-to-month + fiber optic punya churn rate tertinggi 54.5%
- Semakin lama customer berlangganan, semakin kecil kemungkinan churn
- Contract type adalah faktor kategorikal paling berpengaruh terhadap churn
- Gender hampir tidak berpengaruh terhadap keputusan churn

## Tools
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn, XGBoost
- Imbalanced-learn (SMOTE)

