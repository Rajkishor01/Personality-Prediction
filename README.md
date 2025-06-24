Introvert vs. Extrovert Personality Prediction
This project uses behavioral data to classify individuals as introverts or extroverts using machine learning. Along the way, it applies targeted statistical techniques—Theil's U and Point-Biserial Correlation—to select the most relevant features for prediction.

🔍 Project Overview
Goal: Predict personality type (Introvert/Extrovert) from behavioral traits

Dataset: Kaggle - Extrovert vs Introvert Behavior Data

Model: RandomForestClassifier (no hyperparameter tuning)

Focus: Correlation-based feature selection

📊 Features in the Dataset
Feature	Description
Time_spent_Alone	Daily hours spent alone (0–11)
Stage_fear	Stage fright presence (Yes/No)
Social_event_attendance	Frequency of attending social events (0–10)
Going_outside	Days going outside per week (0–7)
Drained_after_socializing	Drained feeling post-socializing (Yes/No)
Friends_circle_size	Number of close friends (0–15)
Post_frequency	Social media post frequency (0–10)
Personality	Target variable: Introvert / Extrovert

🧠 Correlation Techniques
1. Theil's U (Uncertainty Coefficient)
Used for categorical vs. categorical relationships.

Captures directional dependency—how well one variable predicts another.

Ideal for evaluating predictors like Stage_fear → Personality.

2. Point-Biserial Correlation
Applied when one variable is binary and the other is numeric.

Measures linear correlation strength (similar to Pearson, but for binary targets).

Used to assess numeric traits like Time_spent_Alone or Post_frequency.

⚙️ Methodology
Preprocessing:

Handle missing values

Separate numerical and categorical features

Feature Selection:

Use Theil’s U and Point-Biserial Correlation to assess relationship with target

Modeling:

Train a RandomForestClassifier on selected features

Evaluate with confusion_matrix and classification_report

✅ Results
The Random Forest model performed well without any hyperparameter tuning.

Feature selection using Theil's U and Point-Biserial Correlation added explainability and interpretability to the process.

📁 Requirements
Python 3.x

pandas, numpy

matplotlib, seaborn

sklearn

Install with:

bash
Copy
Edit
pip install pandas numpy matplotlib seaborn scikit-learn
📌 Conclusion
This project demonstrates how statistical correlation methods can improve machine learning workflows—not just for prediction, but for understanding why certain features matter in classification tasks.

