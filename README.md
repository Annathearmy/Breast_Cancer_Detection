# Breast Cancer Detection using ANN

This repository presents a **Breast Cancer Detection system** built using an **Artificial Neural Network (ANN)**. The project focuses on identifying malignant tumors based on key numerical features related to tumor size, shape, and boundary irregularities.

The objective is to achieve **high classification accuracy** while also providing **interpretable insights** into the most influential features.

---

## Dataset Description :

The dataset consists of numerical features extracted from breast tumor images. Each feature represents a specific physical characteristic of the tumor.

**Target Variable:**

* `Diagnosis`

  * `0` → Benign (B)
  * `1` → Malignant (M)

All input features are **numerical**, making the dataset well-suited for ANN-based classification after scaling.

---

## Key Features and Risk Insights :

The following features were found to be highly influential. Values **greater than the given thresholds** indicate a **higher risk of breast cancer**.

### Mean Features :

| Feature             | Threshold | Risk Interpretation   |
| ------------------- | --------- | --------------------- |
| radius_mean         | > 15      | Higher risk of cancer |
| perimeter_mean      | > 100     | Higher risk of cancer |
| area_mean           | > 700     | Higher risk of cancer |
| concavity_mean      | > 0.1     | Higher risk of cancer |
| concave_points_mean | > 0.05    | Higher risk of cancer |

### Worst Features :

| Feature              | Threshold | Risk Interpretation   |
| -------------------- | --------- | --------------------- |
| radius_worst         | > 17      | Higher risk of cancer |
| perimeter_worst      | > 115     | Higher risk of cancer |
| area_worst           | > 900     | Higher risk of cancer |
| concavity_worst      | > 0.3     | Higher risk of cancer |
| concave_points_worst | > 0.15    | Higher risk of cancer |

**Insight:** Malignant tumors tend to be **larger** and have **more irregular, concave boundaries** compared to benign tumors.

---

# ANN Model Configuration :
The Artificial Neural Network was trained on **standard-scaled features** to ensure stable and efficient learning.

# Hyperparameters :
hidden_layer_sizes = (50, 4)
learning_rate_init = 0.001
max_iter = 150
random_state = 2

# Model Performance :
The trained ANN achieved the following performance on the test dataset:

* **Accuracy:** 0.9737
* **Precision:** 1.00
* **Recall:** 0.9231
* **F1 Score:** 0.96

# Confusion Matrix :
  [[75  0]
   [ 3 36]]


# Performance Interpretation :
* No benign cases were misclassified as malignant (**zero false positives**)
* High recall ensures most malignant cases are correctly detected
* Strong F1 score reflects a good balance between precision and recall

---

