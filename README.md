# Heart Disease Classification using Decision Tree

## Overview

This project implements a **Decision Tree classifier** to predict heart disease using patient health data.  
The goal is to explore **tree-based models** for medical classification and evaluate performance with different impurity metrics — **Gini Index** and **Entropy**.

The notebook visualizes the generated tree structure, compares training and testing accuracy, and analyzes how hyperparameters (like `max_depth`) affect model performance.

---

## Table of Contents
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Technologies Used](#technologies-used)
- [Usage](#usage)

---

## Dataset

The dataset used contains anonymized medical attributes for heart disease diagnosis.  
Each record includes measurements such as:

- **Age**  
- **Sex**  
- **Chest Pain Type**  
- **Resting Blood Pressure**  
- **Cholesterol Level**  
- **Fasting Blood Sugar**  
- **Max Heart Rate Achieved**  
- **Exercise Induced Angina**  
- **Target:** 1 = Heart Disease Present, 0 = No Heart Disease

---

## Methodology

1. **Data Preprocessing**
   - Imported and cleaned the dataset.
   - Encoded categorical variables.
   - Split data into **training (70%)** and **testing (30%)** sets.

2. **Model Building**
   - Implemented two Decision Tree classifiers using `sklearn.tree.DecisionTreeClassifier`:
     - Criterion = `"gini"`  
     - Criterion = `"entropy"`
   - Tuned the `max_depth` hyperparameter to balance underfitting and overfitting.

3. **Model Evaluation**
   - Computed **Accuracy**, **Precision**, **Recall**, and **Confusion Matrix**.
   - Visualized the Decision Tree using `Graphviz` / `pydotplus`.
   - Compared training vs. testing accuracy for each configuration.

---

## Results

- **Best Accuracy:** ~85% on test data.  
- **Entropy-based tree** performed slightly better in overall classification accuracy.  
- **Optimal max_depth:** Found to be between **3–5**, balancing interpretability and accuracy.  
- The generated tree shows key decision nodes such as **age**, **cholesterol**, and **max heart rate**.

✅ The model successfully classifies patients into heart disease vs. no heart disease categories with strong accuracy and interpretability.

---

## Technologies Used

- **Language:** Python 3.9+  
- **Libraries:**
  - Pandas
  - NumPy
  - Matplotlib / Seaborn
  - Scikit-learn
  - Graphviz / pydotplus
- **Tool:** Jupyter Notebook

---

## Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/mehmet-akif/heart-disease-decision-tree.git
   cd heart-disease-decision-tree
   ```

2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn graphviz pydotplus
   ```

3. Launch the notebook:
   ```bash
   jupyter notebook Lab08-AKIF_SIPAHI.ipynb
   ```

4. Run all cells to:
   - Preprocess the dataset  
   - Train and test Decision Tree models  
   - Visualize the resulting decision tree  


---


## License

© 2025 Mehmet Akif Sipahi. All rights reserved.  
This project is shared for educational and portfolio demonstration purposes only.  
Reproduction, redistribution, or submission of this material for academic credit is strictly prohibited.
