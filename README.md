Partitioned Feature Selection :Locally Uniform Feature Selection with Structured Feature Grouping for Explainable Risk Factor Identification
Overview
This repository contains the official implementation of the Partitioned Feature Selection (PFS) framework proposed for clinically interpretable depression severity prediction. The framework integrates domain knowledge with machine learning to identify informative and clinically meaningful predictors while maintaining competitive predictive performance.

Unlike conventional feature selection methods that rank all features globally, PFS first partitions features into clinically coherent domains and performs feature selection locally within each domain. The selected features are then integrated using Integrated Group Feature Importance (IGFI) to produce a unified ranking of clinically relevant predictors.

The framework is designed to improve both prediction accuracy and model interpretability, enabling transparent identification of depression-related risk factors across multiple symptom domains.

Framework Pipeline
The PFS framework consists of the following stages:

Initial Data Preparation

Missing value handling
Data encoding
Data normalization
Domain-Aware Group Formation

Partition features into clinically meaningful domains
Validate structural consistency of the generated groups
Local Uniform Feature Selection (LUFS)

Generate local target variables for each domain
Select the most informative features independently within each group
Integrated Group Feature Importance (IGFI)

Compute normalized feature importance scores
Aggregate importance across all domains
Produce a global ranking of selected features
Leakage-Free Predictive Modeling

Train machine learning classifiers using the selected features
Evaluate performance using a leakage-free validation protocol
Model Explainability

Validate selected predictors using SHAP analysis
Interpret both feature-level and domain-level contributions
Key Features
Clinically informed feature grouping
Domain-wise local feature selection
Integrated Group Feature Importance (IGFI)
Leakage-free evaluation pipeline
SHAP-based explainability
Reproducible machine learning experiments
Support for multiclass depression severity prediction
Repository Structure
PFS/
│
├── datasets/                 # Example datasets (or download instructions)
├── preprocessing/            # Data preparation scripts
├── grouping/                 # Domain-aware group formation
├── lufs/                     # Local Uniform Feature Selection
├── igfi/                     # Integrated Group Feature Importance
├── models/                   # Machine learning models
├── explainability/           # SHAP analysis
├── results/                  # Experimental results
├── notebooks/                # Jupyter notebooks
├── figures/                  # Figures used in the paper
├── requirements.txt
└── README.md
Requirements
Python 3.10+
NumPy
Pandas
Scikit-learn
XGBoost
LightGBM
CatBoost
SHAP
Matplotlib
Seaborn
Install the required packages using:

pip install -r requirements.txt
Running the Framework
Clone the repository:

git clone https://github.com/<username>/PFS.git
cd PFS
Run the complete pipeline:

python main.py
or execute the Jupyter notebooks in the notebooks/ directory for a step-by-step demonstration.

Experimental Evaluation
The proposed framework was evaluated on multiple depression severity datasets using a leakage-free experimental protocol. Performance was assessed using standard classification metrics, including:

Accuracy
Precision
Recall
F1-score
ROC-AUC (where applicable)
Interpretability was further validated through SHAP-based feature attribution analysis.

Citation
If you use this repository in your research, please cite the associated publication:

Partitioned Feature Selection: Locally Uniform Feature Selection and Integrated Group Feature Importance for Clinically Interpretable Depression Severity Prediction.

(BibTeX will be added after publication.)

License
This project is released under the MIT License.

Contact
For questions, suggestions, or collaborations, please open an Issue or contact the repository maintainer.
