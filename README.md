# Predicting-Protein-Ligand-Binding-Affinity-with-Machine-Learning

# Project Overview
This project focuses on developing RF-Score, a machine learning-based scoring function to predict protein-ligand binding affinities. Traditional scoring functions in molecular docking often rely on rigid theoretical models, leading to inaccuracies. RF-Score leverages **Random Forest** regression to learn complex binding interactions directly from data, offering a more accurate and scalable alternative for drug discovery applications.

# Key Features
- Data-Driven Approach: Uses the PDBbind v2007 dataset, comprising 1,105 training complexes and 195 test complexes, to train and validate the model.
- Feature Engineering: Represents protein-ligand interactions using 36 intermolecular features based on elemental atom pairs (e.g., C-C, N-O) within a 12 Å cutoff.
- Model Performance: Achieves a Pearson correlation coefficient (R) of 0.634 on the training set and 0.41 on the test set, demonstrating robust predictive accuracy.
- Interpretability: Identifies key interactions (e.g., hydrophobic C-C and hydrogen-bonding N-O pairs) through feature importance analysis.

# Methodology
- Data Preparation: High-resolution crystal structures (≤2.5 Å) with reliable binding affinity measurements (Kd/Ki) were selected.
- Feature Extraction: Counts of atom-pair interactions (e.g., C-N, O-O) within 12 Å were computed for each complex.
- Model Training: A Random Forest regressor with 400 decision trees was trained on the extracted features.
- Validation: Performance was evaluated using Pearson's R and RMSE, with additional validation via Y-scrambling to ensure robustness.

# Results
- Training Set: R = 0.634, RMSE = 1.662 log units.
- Test Set: R = 0.41, RMSE = 2.27 log units.
- Scalability: Model performance improves with larger training datasets, suggesting potential for further enhancement with more data.

# Dependencies
- Python (with libraries such as scikit-learn, pandas, numpy).
- PDBbind dataset (available upon request from PDBbind).

# Author
- **Monuj Gogoi**
- Indian Institute of Technology Guwahati
- Under the guidance of **Prof. Debasis Manna**



