Stability-Aware Explainable AI for IoT Intrusion Detection
 Overview
This project focuses on improving the reliability of Explainable AI (XAI) in IoT-based Intrusion Detection Systems (IDS).
While most models achieve high accuracy, their explanations are often unstable under small input changes or model compression.
We address this issue by:
Analyzing explanation instability
Measuring stability using SHAP
Proposing a Stability-Aware Training Framework (SATF) to improve consistency

Key Contributions
 Quantifies explanation instability using Jaccard Similarity
 Uses SHAP for feature-level explanation analysis
 Introduces Stability-Aware Training (SATF)
 Compares baseline vs improved model performance
 Validates results on multiple datasets

 Methodology
1. Baseline Analysis
Train model on original dataset
Generate SHAP explanations
Add noise to input data
Measure change in explanation
2. Stability Measurement
We compute stability using:
Jaccard Similarity (Top-K Features)
Mean SHAP Variation

3. Proposed Solution (SATF)
We improve stability by training the model with:
Original data
Noisy/perturbed data
This forces the model to produce consistent explanations.

Installation
pip install pandas numpy scikit-learn xgboost shap imbalanced-learn joblib


How to Run
python main.py


Output
The system provides:
Classification performance (Accuracy, Precision, Recall, F1-score)
Explanation stability score
Improvement after applying SATF

Workflow
Train Model → Explain (SHAP) → Add Noise → Explain Again → Compare → Improve Model → Re-evaluate


Datasets
UNSW-NB15 – Primary dataset for training
IoT-23 – Used for validation

Future Work
Apply advanced adversarial attacks (e.g., PGD)
Extend to real-time IoT systems
Explore other XAI methods

Contributors
Your Name
Team Members

License
This project is for academic and research purposes.

Final Note
This project goes beyond accuracy by focusing on trustworthiness and consistency of AI explanations, which is critical for real-world IoT security systems.

