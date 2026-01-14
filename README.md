# Australia Weather Rain Prediction

This project builds and evaluates a machine learning classification model to predict whether it will rain tomorrow in Australia based on historical weather data.

The goal is not just to train a model, but to correctly evaluate its performance using appropriate metrics such as confusion matrix, precision, recall, and true positive rate.

---

## Dataset

- Source: Australian weather dataset
- Target variable: `RainTomorrow`
- Classes:
  - 0 → No rain
  - 1 → Rain

The dataset contains numerical and categorical weather features such as temperature, humidity, wind speed, pressure, and rainfall.

---

## Problem Type

- Binary Classification
- Imbalanced dataset (No Rain is the majority class)

---

## Workflow

1. Data loading and inspection  
2. Data cleaning and preprocessing  
   - Handling missing values  
   - Encoding categorical variables  
3. Train-test split  
4. Model training using Random Forest Classifier  
5. Model evaluation using:
   - Confusion Matrix
   - Accuracy
   - Precision
   - Recall (True Positive Rate)

---

## Model Used

- Random Forest Classifier

Random Forest was chosen for its ability to handle non-linear relationships and mixed feature types with minimal feature scaling.

---

## Results

Confusion Matrix (Test Set):

|                | Predicted No Rain | Predicted Rain |
|----------------|------------------|----------------|
| Actual No Rain | 1090             | 64             |
| Actual Rain    | 175              | 183            |

- True Positive Rate (Recall for Rain): **51%**
- Observation:  
  While overall accuracy is high due to class imbalance, the model struggles to correctly identify rainy days. This highlights the importance of evaluating recall instead of relying solely on accuracy.

---

## Key Learnings

- Accuracy can be misleading for imbalanced datasets  
- Confusion matrix provides deeper insight into model performance  
- Improving recall is critical when false negatives are costly  

---

## Possible Improvements

- Handle class imbalance using techniques like:
  - Class weighting
  - SMOTE
- Try alternative models such as:
  - Gradient Boosting
  - XGBoost
- Hyperparameter tuning

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn

---

## Author

Nikhil Gopi
