# 🏨 Hotel Price Prediction and Classification

This machine learning project predicts hotel price categories (e.g., **low**, **medium**, **high**) using various features like hotel type, star rating, facilities, location, and user reviews.

> 📘 Course Project  
> Instructor: Dr. YaghoobZadeh  
> University of Tehran – School of Electrical & Computer Engineering

---

## 🎯 Objectives

- Preprocess real-world hotel data and extract informative features  
- Classify hotels into price brackets using supervised learning  
- Evaluate and compare multiple classification models

---

## 🧹 Data Preprocessing

- Handled missing values (e.g., `star_rating`, `review_score`)
- Applied **label encoding** and **one-hot encoding** to:
  - `hotel_type`
  - `location`
- Normalized numerical features like:
  - `review_count`
  - `distance_from_city_center`

---

## ⚙️ Feature Engineering

- Added custom features:
  - `is_luxury`: Derived from amenities + star rating
  - `review_per_star`: Ratio of reviews to rating level
- Removed outliers using IQR filtering on price-based fields

---

## 🧠 Models Used

| Model                   | Performance Notes                         |
|-------------------------|-------------------------------------------|
| Logistic Regression     | Baseline classifier                       |
| Random Forest Classifier| **Best accuracy**: 85.3%                  |
| XGBoost                 | High precision for **high-price** hotels  |
| SVM                     | Underperformed on imbalanced data         |

✅ **Evaluation Metrics**:
- Accuracy  
- Precision / Recall  
- Confusion Matrix  
- Cross-validation (**k=5**)

---

## 📊 Results Summary

- **Random Forest**: Most balanced and accurate model  
- **XGBoost**: Best for identifying high-end hotels  
- **SVM**: Struggled with class imbalance

---

## 🛠️ Tech Stack

- **Python** (Jupyter Notebook)  
- `pandas`, `numpy`  
- `scikit-learn`, `xgboost`  
- `matplotlib`, `seaborn` for visualization

---

## 🔮 Future Enhancements

- Switch to deep learning models (e.g., MLP)  
- Add **NLP-based sentiment analysis** from user reviews  
- Implement price **regression model** to predict actual value
