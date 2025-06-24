# Introvert vs. Extrovert Personality Prediction

This project uses behavioral data to classify individuals as **introverts** or **extroverts** using machine learning. It also applies two statistical techniques—**Theil's U** and **Point-Biserial Correlation**—to select features that strongly relate to personality traits.

## 🔍 Project Overview

- **Goal**: Predict personality type (Introvert/Extrovert) from behavioral traits
- **Dataset**: [Kaggle - Extrovert vs Introvert Behavior Data](https://www.kaggle.com/datasets/rakeshkapilavai/extrovert-vs-introvert-behavior-data)
- **Model**: RandomForestClassifier (without hyperparameter tuning)
- **Core Techniques**: Feature selection using Theil’s U and Point-Biserial Correlation

---

## 📊 Features in the Dataset

| Feature                     | Description                                      |
|-----------------------------|--------------------------------------------------|
| `Time_spent_Alone`          | Daily hours spent alone (0–11)                   |
| `Stage_fear`                | Stage fright presence (Yes/No)                   |
| `Social_event_attendance`   | Frequency of attending social events (0–10)      |
| `Going_outside`             | Days going outside per week (0–7)                |
| `Drained_after_socializing`| Feeling drained after socializing (Yes/No)       |
| `Friends_circle_size`       | Number of close friends (0–15)                   |
| `Post_frequency`            | Social media post frequency (0–10)               |
| `Personality`               | Target variable: Introvert or Extrovert          |

---

## 🧠 Correlation Techniques Used

### 1. Theil's U (Uncertainty Coefficient)
- A directional measure for **categorical vs. categorical** variables.
- Quantifies how much knowing one variable (e.g., `Stage_fear`) reduces uncertainty about another (e.g., `Personality`).
- Unlike symmetric metrics, Theil’s U captures how *predictable* one variable is from another.

### 2. Point-Biserial Correlation
- Designed for **numeric vs. binary** variable relationships.
- Similar to Pearson correlation but works when one variable is binary (e.g., `Personality`) and the other is continuous (e.g., `Post_frequency`).
- Helps assess linear relationships between behavior traits and personality types.

---

## ⚙️ Workflow

1. Preprocess dataset:
   - Handle null values
   - Split features into numerical and categorical
2. Perform correlation analysis:
   - Use Theil’s U and Point-Biserial Correlation for feature selection
3. Train model:
   - Train RandomForestClassifier on selected features
4. Evaluate:
   - Use confusion matrix and classification report to assess performance

---

## ✅ Results

- The Random Forest model performed well without hyperparameter tuning.
- Feature selection based on correlation measures improved interpretability and focused the model on meaningful inputs.

---

## 📦 Dependencies

To run the notebook, install the following Python packages:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
