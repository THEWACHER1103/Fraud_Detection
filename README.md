##🚨 Fraud Detection with Machine Learning

📌 Overview

Financial institutions face a constant challenge: detecting fraudulent transactions in highly imbalanced environments.

This project focuses on building a machine learning model capable of identifying fraud while balancing detection performance and customer experience.

⸻

🎯 Objective

Develop a fraud detection system that:
	•	Maximizes fraud detection (Recall)
	•	Controls false positives (Precision)
	•	Handles extreme class imbalance (~0.5% fraud)

⸻

📊 Dataset

The dataset simulates real-world financial transactions, including:
	•	Transaction amount (amt)
	•	Customer location (latitude/longitude)
	•	Merchant location
	•	Transaction timestamp
	•	Customer demographics

⸻

🧠 Methodology

1. Exploratory Data Analysis (EDA)
	•	Analysis of class imbalance
	•	Correlation matrix
	•	Behavioral patterns detection

⸻

2. Feature Engineering

Key features were created to capture fraud patterns:
	•	distance_km → Distance between customer and transaction location (Haversine formula)
	•	far_night_flag → Binary variable for suspicious transactions (far distance + night hours)
	•	Behavioral features based on transaction context

⸻

3. Model
	•	Algorithm: XGBoost
	•	Optimization: Optuna
	•	Evaluation metric: PR-AUC (suitable for imbalanced datasets)

⸻

4. Model Evaluation

To ensure real-world applicability, multiple metrics were used:
	•	Precision & Recall
	•	F1-Score
	•	PR-AUC
	•	ROC-AUC
	•	KS Statistic (Kolmogorov-Smirnov) → measures class separation

⸻

5. Threshold Tuning

Instead of using the default threshold (0.5), a custom threshold was selected to:
	•	Prioritize fraud detection
	•	Maintain acceptable false positives

⸻

📈 Results
	•	✔ Strong fraud detection capability
	•	✔ Balanced Precision / Recall
	•	✔ High KS → good separation between fraud and non-fraud

⸻

💡 Key Insights
	•	Fraud detection is context-driven, not variable-driven
	•	Distance alone is weak, but combined with time becomes powerful
	•	Threshold selection is critical for real-world deployment

⸻

⚠️ Data Leakage Prevention

To avoid data leakage:
	•	All preprocessing steps were implemented using pipelines
	•	Transformations were fitted only on training data
	•	No target leakage was introduced during feature engineering

⸻

🚀 Conclusion

This model demonstrates that effective fraud detection relies on:
	•	Understanding behavioral patterns
	•	Proper feature engineering
	•	Business-aligned model calibration

It can be used as a real-time fraud alert system, balancing risk detection and customer experience.

⸻

🛠️ Tech Stack
	•	Python
	•	Pandas / NumPy
	•	Scikit-learn
	•	XGBoost
	•	Optuna
	•	Matplotlib / Seaborn

⸻

📌 Next Steps
	•	Deploy model as an API
	•	Add real-time scoring
	•	Incorporate more behavioral features

⸻

👤 Author

Otoniel Ditren
Data Analyst | Aspiring Data Scientist
