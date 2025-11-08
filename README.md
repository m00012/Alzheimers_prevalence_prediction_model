# Alzheimers_prevalence_prediction_model
The purpose of this machine learning model is to predict Alzheimer’s disease prevalence based on demographic and geographic factors in the United States using Gradient Boosting.
Alzheimer’s Prevalence Prediction (Gradient Boosting)
This project trains a Gradient Boosting Regression model to predict Alzheimer’s prevalence (Data_Value) from demographic and geographic features in the Alzheimer’s Disease and Healthy Aging dataset.

Requirements

Hardware

Minimum: Dual-core CPU, 8 GB RAM, 10 GB free disk
Tested on: HP EliteBook 840 G3, Intel® Core™ i7-6600U, 16 GB RAM, 477 GB SSD

Operating System / Platform

Windows 10 Pro (64-bit) (tested)
-Also works on macOS/Linux with Python 3.10+ installed

Software

Python 3.12.5 (recommended 3.10+)
Visual Studio Code (or any IDE)
Git (to clone/push to GitLab)

Python Libraries

pandas
numpy
scikit-learn
matplotlib
seaborn


Instructions to Run the AI/ML Application
A. Clone the repository
git clone https://gitlab.com/wgu-gitlab-environment/student-repos/mkasse5/d683-advanced-ai-and-ml.git
cd d683-advanced-ai-and-ml

B. Install Python dependencies
pip install -r requirements.txt
If you don’t have a requirements.txt, install directly:
pip install pandas numpy scikit-learn matplotlib seaborn
D. Place the dataset
Extract the dataset alzheimer_s_disease_and_healthy_aging_data.csv from the zipped file archive
Ensure the raw CSV (e.g., alzheimer_s_disease_and_healthy_aging_data.csv) is in the project root (same folder as task2.py).
If your file name differs, update it inside task2.py.
E. Run preprocessing + training
The script:
drops duplicates
handles missing values in Data_Value (imputation)
one-hot encodes categorical features
trains and optimizes GradientBoostingRegressor
prints RMSE and R²
performs k-fold cross-validation
exports a preprocessed dataset for submission
Run:
python task2.py
Expected console output (example):
RMSE: 12.687...
R2 Score: 0.623..
Cross-Validation R2 Mean: 0.6250
Cross-Validation R2 Standard Deviation: 0.0033
Saved: preprocessed_alzheimers.csv
F. Upload the preprocessed dataset to GitLab
After running, you should have preprocessed_alzheimers.csv in the repo  branch working_branch
Useful Notes / Troubleshooting
Line endings (CRLF vs LF): On Windows, Git may warn about CRLF/LF. This is harmless.
Large files: If the raw CSV is very large, consider using Git LFS.
Reproducibility: Results use fixed random_state=42
