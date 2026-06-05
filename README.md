# Machine-Learning-Neural-Network-Models-for-Diabetes-Prediction
A Business Intelligence project that predicts diabetes using the **Pima Indians Diabetes Dataset**. The goal is to compare a traditional ML model with a neural network and identify which model performs better for early diabetes risk prediction.

## Dataset

- Dataset: Pima Indians Diabetes Dataset
- Records: 768
- Features: 8 medical variables
- Target: `Outcome`  
  - `0` = Non-diabetic  
  - `1` = Diabetic

Key features include:

- Glucose
- BMI
- Age
- BloodPressure
- Insulin
- SkinThickness
- DiabetesPedigreeFunction
- Pregnancies

## Methodology

1. Performed Exploratory Data Analysis
2. Checked missing values
3. Detected outliers using boxplots
4. Applied IQR-based clipping on:
   - Insulin
   - DiabetesPedigreeFunction
5. Split data into 80% train and 20% test
6. Trained and compared:
   - Logistic Regression
   - Neural Network

## Models

### Logistic Regression

- Regularization: L2
- Solver: liblinear
- Training Accuracy: 77.04%
- Validation Accuracy: 81.17%

### Neural Network

Architecture:

- Dense(128, ReLU)
- Dropout(0.2)
- Dense(64, ReLU)
- Dense(1, Sigmoid)

Validation Accuracy: around 73-76%

## Results

| Model | Validation Accuracy |
|---|---:|
| Logistic Regression | 81.17% |
| Neural Network | 73-76% |

Logistic Regression performed better because the dataset is small and easier to model with a simpler classifier.

## Key Findings

- Glucose is the strongest predictor.
- BMI and Age also influence diabetes risk.
- Neural Network did not outperform Logistic Regression.
- Simple ML model is more reliable for this dataset.

## Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow / Keras
- Matplotlib / Seaborn

## Conclusion

This project shows how machine learning can support early diabetes risk prediction. Logistic Regression achieved the best result and is more suitable than the neural network for this dataset.
```
