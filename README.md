# 🧪 Genotoxicity Prediction Using Hybrid SMILES Representations

This project proposes a computational pipeline for predicting the genotoxicity of chemical compounds using molecular descriptors (RDKit), toxicological alert substructures, and vector representations obtained through Word2Vec applied to SMILES strings.

---

## 🎯 Objective

To develop machine learning models capable of predicting the genotoxic potential of chemical compounds by integrating different molecular representation strategies.

---

## 📂 Data Sources

- [GENE-TOX](https://www.nlm.nih.gov/toxnet/Accessing_GENETOX_Content_from_PubChem.html)
- [CCRIS](https://www.nlm.nih.gov/toxnet/Accessing_CCRIS_Content_from_PubChem.html)
- [ECVAM](http://data.jrc.ec.europa.eu/dataset/jrc-eurl-ecvam-genotoxicity-carcinogenicity-ames)
- [ECHA](https://echa.europa.eu)
- [IRIS](https://www.epa.gov/iris)

---

## 🧪 Methodology

The pipeline is structured in the following stages:

1. **Data collection and curation**  
   - Extraction and cleaning of public dataset entries  
   - Removal of duplicates and class harmonization  
   - SMILES retrieval via PubChem API

2. **Molecular feature generation**  
   - Calculation of molecular descriptors using RDKit  
   - Detection of toxicological alert substructures  
   - SMILES tokenization and Word2Vec-based vectorization

3. **Representation fusion**  
   - Concatenation of RDKit descriptors with Word2Vec embeddings

4. **Classification**  
   - Model training using algorithms such as Random Forest and LightGBM  
   - Hyperparameter tuning with GridSearchCV  
   - 10-fold stratified cross-validation

5. **Model evaluation**  
   - Metrics: Accuracy, F1-score, ROC-AUC, Balanced Accuracy

---

## 📒 Notebooks Structure

├── 01_data_collection_and_curation.ipynb # Data acquisition from public sources and preprocessing

├── 02_smiles_retrieval.ipynb # Retrieval of SMILES using PubChem API and manual completion

├── 03_rdkit_descriptors_alerts.ipynb # Calculation of molecular descriptors with RDKit # Detection of toxicological alert substructures # Model training and evaluation based on these features

├── 04_smiles_tokenization_word2vec.ipynb # SMILES tokenization # Word2Vec training # Construction of molecular vectors and predictive evaluation

├── 05_fusion_hybrid_features.ipynb # Integration of RDKit descriptors with Word2Vec embeddings # Training and evaluation of models with hybrid representations

---

## 📊 Results

- **Best model:** Random Forest with hybrid feature vectors  
- **Combined dataset size:** 3886 compounds  
- **Total features:** 753 (369 descriptors + 384 Word2Vec)

> Performance metrics are reported in each notebook using cross-validation results.

---

## 🧑‍💻 Author

**Iuri Barbosa Pereira**  
Data Scientist | Pharmaceutical Sciences + Computer Science  
• [GitHub](https://github.com/Barboss4)
