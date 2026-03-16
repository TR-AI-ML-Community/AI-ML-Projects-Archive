Blood Cell Anomaly Detection (Machine Learning)

This project is a simple machine learning experiment where a model is trained to detect blood cell anomalies using tabular data.
The goal is to classify whether a blood cell sample is anomalous or normal.

The project was created as part of practicing basic data preprocessing, feature engineering, and model training with Python and Scikit-Learn.

---

Dataset

The dataset contains different measurements and properties of blood cells such as:

- cell morphology features (diameter, circularity, eccentricity, granularity etc.)
- blood related measurements (WBC count, RBC count, hemoglobin etc.)
- microscope and staining information
- patient metadata (age group, sex)

Target column:

anomaly_label

- "0" → Normal
- "1" → Anomalous

---

Data Preprocessing

Some columns were removed because they could cause data leakage (they are directly related to the target label):

cytodiffusion_anomaly_score
cytodiffusion_classification_confidence
labeller_confidence_score
cell_type

Categorical features were encoded using OneHotEncoder.

cell_type
disease_category
patient_age_group
patient_sex
staining_protocol
microscope_model

The dataset was split into training and testing sets:

train_test_split(test_size = 0.2)

---

Model

The main model used in this project is:

RandomForestClassifier

Parameters used:

max_depth = 5
n_estimators = 5

The model was trained using:

model.fit(X_train_final, y_train)

Predictions were generated with:

model.predict(X_test_final)

---

Results

Model accuracy on the test set:

Accuracy ≈ 0.975

This means the model correctly classifies around 97.5% of the samples.

Logistic Regression was also tested but Random Forest gave better results for this dataset.

---

Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- Jupyter Notebook

---

Project Structure

blood-cell-anomaly-detection/
│
├── blood_cell_anomaly_detection.csv
├── blood_cell_model.ipynb
└── README.md

---

Notes

This project is mainly for learning purposes and experimenting with basic machine learning workflows such as:

- data preprocessing
- categorical encoding
- model training
- model evaluation

The goal was to build a simple pipeline and understand how different features affect model performance.

---
