# Parkinson's Disease Detection

This project implements a machine learning model to detect Parkinson's disease based on vocal features. The dataset used for training the model was sourced from Kaggle and includes various biomedical voice measurements from people with Parkinson's disease and healthy individuals.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Model Details](#model-details)
- [Results](#results)
- [Contributing](#contributing)

## Overview

Parkinson's disease is a chronic and progressive movement disorder. Early detection is crucial for effective management. This project uses machine learning to classify whether an individual has Parkinson's disease based on vocal attributes.

The model was built using Python and popular libraries like `scikit-learn` and `pandas`. The project also involves data preprocessing, feature scaling, and model evaluation techniques.

## Dataset

The dataset is sourced from Kaggle: [Parkinson's Disease Dataset](https://www.kaggle.com/datasets/nidaguler/parkinsons-data-set).

- **Features**: The dataset includes 22 attributes extracted from voice recordings. These features include measures of fundamental frequency, amplitude perturbations, and noise-to-harmonics ratios.
- **Target Variable**: `status` (1 = Parkinson's, 0 = healthy)

## Installation

1. **Clone the repository:**

   ```bash
   git clone <https://github.com/rudrapatel001/Parkinsons-Disease-Detection>
   cd <Parkinsons-Disease-Detection>
   ```

2. **Install the required libraries:**

   ```bash
   pip install numpy pandas scikit-learn matplotlib seaborn
   ```

3. **Jupyter Notebook:**
   To run the model training and evaluation notebook, you will need to have Jupyter Notebook or JupyterLab installed. You can install Jupyter using the following command:

   ```bash
   pip install notebook
   ```

## Usage

1. **Run the Jupyter Notebook**: You can open and run the notebook file `model.ipynb` to see the data preprocessing, model training, and evaluation steps.

   ```bash
   jupyter notebook model.ipynb
   ```

2. **Predict Parkinson's Disease for New Data**:
   To predict if a new person has Parkinson's disease, provide the required voice feature values and run the prediction cell in the notebook. Example input:

   ```python
   input_data = (197.07600, 206.89600, 192.05500, 0.00289, 0.00001, 0.00166, 0.00168, 0.00498, 0.01098, 0.09700, 0.00563, 0.00680, 0.00802, 0.01689, 0.00339, 26.77500, 0.422229, 0.741367, -7.348300, 0.177551, 1.743867, 0.085569)

   # Run prediction
   prediction = model.predict([input_data])
   ```

3. **Standardizing Input**: Ensure that input features are standardized before passing them to the model for accurate predictions.

## Model Details

- **Algorithm**: The model uses a supervised learning algorithm (e.g., Support Vector Machine, Decision Tree, or Logistic Regression) to classify whether a person has Parkinson's disease.
- **Feature Scaling**: Data is standardized using `StandardScaler` to ensure that features with different ranges do not affect the model performance.
- **Cross-Validation**: K-fold cross-validation is used to validate the model performance.
- **Performance Metrics**: The model is evaluated using accuracy, precision, recall, and F1-score.

## Results

The model achieved the following performance on the test data:

**Accuracy**

- **Training**: `88.46%`
- **Testing**: `87.17%`

Visualizations such as confusion matrix and ROC curves are included in the notebook for further analysis.

## Contributing

If you would like to contribute to this project, feel free to submit issues or pull requests. Please ensure that your changes are well documented and tested.
