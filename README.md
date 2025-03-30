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
   - Statistic: Tukey's HSD test

---

## Notebooks Overview

- `DataCleaning.ipynb`  
  Performs data acquisition from public sources and preprocessing for further analysis.

- `smiles_retrieval.ipynb`  
  Retrieves SMILES representations using the PubChem API and includes manual completion steps.

- `Avaliação_de_dados_descritores.ipynb`  
  Calculates molecular descriptors using RDKit and detects toxicological alert substructures. Trains models based on these features.

- `Avaliação_de_Smiles_por_NPL.ipynb`  
  Applies SMILES tokenization and Word2Vec training to construct molecular embeddings and evaluate predictive models.

- `Avaliação_de_Smiles_por_NPL_+_descritores.ipynb`  
  Combines RDKit descriptors with Word2Vec embeddings for hybrid feature representation and model evaluation.

- `Data_analise.ipynb`  
  Explores and visualizes data distributions, correlations, and other relevant patterns.

- `Results_avaluation.ipynb`  
  Assesses model performance through various evaluation metrics and visualizations.

---

## 📊 Results

The best predictive performance was achieved using the in vivo dataset with the combined representation (descriptors + Word2Vec), reaching an average F1-score of 0.726. This integrated approach consistently outperformed isolated representations across datasets. Tukey's HSD test confirmed the statistical significance of these differences (α = 0.05).


> Performance metrics are reported in each notebook using cross-validation results.

---

## 🧑‍💻 Author

**Iuri Barbosa Pereira**  
Data Scientist | Pharmaceutical Sciences + Computer Science  
• [GitHub](https://github.com/Barboss4)
