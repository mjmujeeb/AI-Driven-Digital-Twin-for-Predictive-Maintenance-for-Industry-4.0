Machine Learning Techniques for Voice-Based Parkinson's Disease Detection

A machine-learning project that explores the use of voice-related biomedical measurements to distinguish between healthy individuals and individuals with Parkinson's disease.

The project uses the Parkinson's Speech Dataset from the UCI Machine Learning Repository and compares multiple classification algorithms.

Overview

Parkinson's disease can affect speech production and vocal characteristics. Certain measurable properties of voice recordings may contain patterns that are useful for research into automated classification.

This project applies machine-learning techniques to a dataset of voice measurements and evaluates how different classifiers perform on the classification task.

The project is intended for educational and research purposes. It is not a clinical diagnostic tool.

Dataset

The notebook loads the Parkinson's dataset from the UCI Machine Learning Repository.

The dataset contains voice-related measurements and a target variable indicating the class.

The notebook identifies the target column using the "status" or "class" field when available. It also removes the "name" field from the predictive features when present.

Dataset source:

"UCI Parkinson's Speech Dataset" (https://archive.ics.uci.edu/ml/machine-learning-databases/parkinsons/parkinsons.data)

Workflow

UCI Voice Dataset
       |
       v
Data Loading and Exploration
       |
       v
Preprocessing
       |
       v
Feature Selection
       |
       v
Feature Scaling
       |
       v
Train / Test Split
       |
       v
Model Training
       |
       v
Model Evaluation
       |
       v
Visual Analysis and Report

Data Preprocessing

The notebook includes the following preprocessing steps:

- Load and inspect the dataset.
- Identify the target variable.
- Remove non-predictive identifier fields where applicable.
- Encode class labels.
- Examine correlations between features.
- Remove highly correlated features using a correlation threshold.
- Standardize the feature values.
- Split the data into training and testing sets.

Machine Learning Models

The notebook imports and explores several classification algorithms:

Algorithm| Purpose
Logistic Regression| Linear classification baseline
Support Vector Machine| Classification using decision boundaries
Random Forest| Ensemble learning using decision trees
Gradient Boosting| Sequential ensemble learning
Multi-Layer Perceptron| Neural-network-based classification

The notebook evaluates the models and identifies a best-performing model based on the implemented evaluation workflow.

Evaluation Metrics

The project includes multiple evaluation measures:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- ROC curve
- Area Under the ROC Curve (ROC-AUC)

These metrics provide a broader view of classification performance than accuracy alone.

Visualization

The notebook includes visual analysis to help interpret model behavior, including:

- Model performance comparisons
- Confusion matrices
- ROC curves
- PCA-based feature visualization
- t-SNE-based visualization
- Feature exploration and correlation analysis

SHAP is also imported for model explainability exploration.

Technology Stack

Area| Technology
Language| Python
Data processing| Pandas, NumPy
Visualization| Matplotlib, Seaborn
Machine learning| scikit-learn
Dimensionality reduction| PCA, t-SNE
Explainability| SHAP
Dataset| UCI Parkinson's Speech Dataset
Environment| Jupyter Notebook / Google Colab

Getting Started

1. Clone the repository

git clone https://github.com/mjmujeeb/Parkinson-s-Disease-Voice-Based-Detection.git
cd Parkinson-s-Disease-Voice-Based-Detection

2. Install dependencies

pip install pandas numpy matplotlib seaborn scikit-learn shap

3. Open the notebook

jupyter notebook Final.ipynb

Alternatively, upload the notebook to Google Colab.

4. Run the notebook

Execute the cells in sequence.

The notebook downloads the dataset from the UCI repository, performs preprocessing, trains the classification models, and generates evaluation visualizations.

An active internet connection is required for the dataset download.

Expected Outputs

Running the notebook produces:

- Dataset exploration and class distribution
- Preprocessed training and testing data
- Trained classification models
- Model evaluation metrics
- Confusion matrices
- ROC curves
- Dimensionality-reduction visualizations
- A final model comparison report

Limitations

- Results depend on the dataset and its size.
- Model performance on this dataset does not establish clinical effectiveness.
- The project does not provide a validated diagnosis from a new voice recording.
- External validation on independent datasets would be required before any real-world clinical use.

Future Improvements

- Add a user interface for uploading voice recordings.
- Build a validated audio feature extraction pipeline.
- Evaluate generalization using independent datasets.
- Improve explainability and feature importance analysis.
- Add reproducible experiment tracking.
- Package the workflow as a deployable application.

License

See the "LICENSE" file in this repository.
