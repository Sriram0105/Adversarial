Explainable and Reliable Adversarial Machine Learning for DNS Traffic Analysis
📌 Overview

This project focuses on detecting adversarial attacks in DNS traffic using Machine Learning, Explainable AI (XAI), and Ensemble Learning techniques.

The framework generates adversarial DNS samples using state-of-the-art attack methods and trains multiple machine learning models to distinguish legitimate DNS traffic from adversarially manipulated traffic.

The project also incorporates explainability techniques such as LIME and SHAP to improve model transparency and trustworthiness.

🎯 Objectives
Detect adversarial DNS traffic.
Generate adversarial examples using:
FGSM (Fast Gradient Sign Method)
Carlini & Wagner (C&W)
JSMA (Jacobian Saliency Map Attack)
Compare multiple machine learning classifiers.
Apply Explainable AI techniques.
Build an ensemble model for improved detection performance.
Evaluate anomaly detection using SVDD (One-Class SVM).
📂 Dataset

The project uses DNS traffic datasets:

legitimate.csv
fgsm_combined.csv
cw_combined.csv
jsma_combined.csv

Labels:

Class	Description
0	Legitimate DNS Traffic
1	Adversarial DNS Traffic
🏗️ Project Workflow
DNS Dataset
     │
     ▼
Data Preprocessing
     │
     ▼
Victim Neural Network
     │
     ▼
Adversarial Attack Generation
(FGSM, CW, JSMA)
     │
     ▼
Combined Dataset
     │
     ▼
Feature Scaling
     │
     ▼
Machine Learning Models
     │
     ▼
Explainability (LIME & SHAP)
     │
     ▼
Ensemble Learning
     │
     ▼
Performance Evaluation
⚙️ Technologies Used
Machine Learning
Scikit-Learn
TensorFlow
PyTorch
Adversarial ML
ART (Adversarial Robustness Toolbox)
Explainable AI
LIME
SHAP
Visualization
Matplotlib
t-SNE
🤖 Models Evaluated
Traditional Models
Logistic Regression
Decision Tree
Random Forest
K-Nearest Neighbors (KNN)
Support Vector Machine (SVM)
Gradient Boosting
Deep Learning Model
Multi-Layer Neural Network
Anomaly Detection
One-Class SVM (SVDD)
Ensemble Model

Stacking Ensemble using:

Logistic Regression
Random Forest
Gradient Boost
SVM
Decision Tree
KNN
📊 Results
Individual Model Performance
Model	Accuracy
Logistic Regression	56.7%
Random Forest	57.3%
Gradient Boost	71.6%
SVM (RBF)	75.2%
Decision Tree	56.3%
KNN	66.7%
Ensemble Model Performance
Metric	Score
Accuracy	91%
Precision	94%
Recall	94%
F1 Score	94%
ROC-AUC	97%

The stacking ensemble significantly outperformed individual classifiers.

🔍 Explainable AI
LIME

Used for local explanations of individual DNS traffic predictions.

SHAP

Used for:

Feature importance analysis
Global model explanations
Waterfall plots
Force plots
Summary plots
📈 Visualizations

The project includes:

ROC Curves
Confusion Matrices
Feature Importance Analysis
SHAP Summary Plots
SHAP Waterfall Plots
t-SNE Visualization
Ensemble Weight Analysis
🚀 Installation
git clone https://github.com/your-username/adversarial-dns-detection.git

cd adversarial-dns-detection

Install dependencies:

pip install -r requirements.txt
📦 Required Libraries
pip install numpy pandas matplotlib scikit-learn tensorflow torch

pip install adversarial-robustness-toolbox

pip install shap lime

pip install imbalanced-learn
▶️ Running the Project
python main.py

The pipeline will:

Load DNS data
Train victim model
Generate adversarial attacks
Train detection models
Evaluate performance
Generate explanations
Produce visualizations





🔬 Future Improvements
Integration with real-time DNS monitoring systems.
Transformer-based adversarial detection.
Federated learning for privacy-preserving detection.
Adversarial training for improved robustness.
Real-world deployment using cloud infrastructure.
