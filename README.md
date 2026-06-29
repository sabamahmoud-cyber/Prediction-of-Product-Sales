# Prediction of Product Sales

## Project Overview

This project aims to predict product sales using machine learning techniques based on product and outlet characteristics. Multiple regression models were developed and evaluated to determine the most effective approach for sales prediction.

---

## Dataset

The dataset contains 8,523 records and includes product and outlet-related information such as:

* Item Weight
* Item Fat Content
* Item Visibility
* Item Type
* Outlet Characteristics
* Item Outlet Sales (Target Variable)

---

## Key Insights

### Insight 1: Outlet Type Influences Product Sales

Sales varied across outlet categories. Supermarket Type 3 generally achieved higher sales values, while Grocery Stores showed lower sales performance. This indicates that outlet characteristics contribute significantly to predicting product sales.

<img width="804" height="470" alt="image" src="https://github.com/user-attachments/assets/c8c0891d-ca4f-4f7a-b38c-52cd7f46f0af" />


---

### Insight 2: Item MRP Shows the Strongest Relationship with Sales

The correlation heatmap indicates that Item_MRP has the strongest positive relationship with Item_Outlet_Sales (correlation ≈ 0.57), while the remaining numerical variables showed relatively weak relationships. This suggests that product pricing is an important predictor of sales.

<img width="936" height="853" alt="image" src="https://github.com/user-attachments/assets/bde9e452-fe62-4b2c-8cb8-8dcc3136231d" />


---

## Model Summary

Three regression models were evaluated:

| Model                 | Test R²    | Test RMSE   | Assessment      |
| --------------------- | ---------- | ----------- | --------------- |
| Linear Regression     | 0.5792     | 1069.42     | Stable baseline |
| Default Random Forest | 0.5702     | 1080.86     | Overfitting     |
| Tuned Random Forest   | **0.6183** | **1018.59** | Recommended     |

### Final Selected Model

**Tuned Random Forest Regressor**

Parameters:

* max_depth = 5
* min_samples_leaf = 10
* n_estimators = 200

### Evaluation

The optimized Random Forest model achieved the best balance between training and testing performance and demonstrated stronger generalization capability compared with baseline models.

---

## Repository Contents

* Data preprocessing notebook
* Machine learning notebook
* Visualizations
* Final model evaluation

---

## Conclusion

This project demonstrated the use of machine learning techniques to predict product sales and highlighted the importance of model tuning to improve predictive performance and reduce overfitting.
