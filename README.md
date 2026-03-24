# Antibiotic-Resistant-Code
The project aims to identify new growth-inhibitory molecules against E. coli using a deep learning pipeline, specifically a Directed Message Passing Neural Network (D-MPNN).
Tech Stack: The workflow utilizes RDKit for chemical informatics, the ChEMBL API for data retrieval, and Chemprop for training the deep learning model.

2. Data Foundation (Training & Screening)
Training Library: The model was trained on a primary screening dataset of 2,560 molecules.

Data Structure: The dataset includes chemical names, SMILES strings, and their mean inhibition values against E. coli. Molecules with high inhibition were categorized as "Active" to train the classifier.
Model Training & Augmentation
Feature Engineering: To improve the D-MPNN, molecular features were augmented using RDKit descriptors such as BalabanJ, BertzCT, and various Chi indices.

Model Comparison: The project evaluated several modeling approaches, including:

D-MPNN (learned features vs. augmented RDKit features).

Feed-forward Deep Neural Networks (DNN) using Morgan fingerprints.

Random Forest and Support Vector Machine (SVM) models.
Discovery of Halicin & Predictive Screening
The Breakthrough: A key highlight is the discovery of Halicin, a molecule with high potency and low similarity to existing antibiotics.

Similarity Analysis: Tanimoto similarity scores were calculated to compare training molecules to Halicin, demonstrating its structural novelty (e.g., Nithiamide showed a low similarity of only 0.37).

Large-Scale Prediction: The trained model was used to screen vast databases:

Drug Repurposing Hub: Identified top candidates like Ulifloxacin and Cefmenoxime.

ZINC15 & WuXi Libraries: Screened millions of molecules, identifying thousands with high prediction scores (>0.7) for potential antibiotic activity.
