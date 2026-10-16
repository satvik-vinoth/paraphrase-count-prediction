# Notebooks

This folder contains Jupyter notebooks used for various stages of the project, including dataset creation, enrichment with linguistic features, and model training and evaluation.

## Notebooks Overview

### 1. `dataset_creation_small.ipynb`
- **Purpose**: 
  - Generates a small subset of paraphrase data for initial testing and development.
  - Uses the Pegasus model to create paraphrases and applies filtering to ensure quality.
- **Inputs**:
  - A small set of original sentences for paraphrasing.
- **Outputs**:
  - A sample dataset containing sentences and their generated paraphrases.

### 2. `enriching_dataset_linguistic_features.ipynb`
- **Purpose**:
  - Enriches the dataset with additional linguistic features like:
    - Part-of-speech (POS) tags.
    - Dependency structures.
    - Readability scores.
  - Prepares the dataset for input into the BERT-based regression model.
- **Inputs**:
  - The dataset created from `dataset_creation_small.ipynb`.
- **Outputs**:
  - An enriched dataset with linguistic feature columns, ready for model training.

### 3. `model_training_evaluation.ipynb`
- **Purpose**:
  - Trains a BERT-based regression model to predict the number of paraphrases for a given sentence.
  - Evaluates model performance using metrics like R², MSE, precision, recall, and F1-score.
  - Visualizes results with plots (e.g., loss curves, predicted vs actual values).
- **Inputs**:
  - The enriched dataset from `enriching_dataset_linguistic_features.ipynb`.
- **Outputs**:
  - Model performance metrics.
  - Saved plots and predictions.
  - A trained BERT-based regression model.
 
### 4. `EXPERIMENT FOR FILTERING THRESHOLDS.ipynb`
- **Purpose**:
  - Evaluates different Levenshtein distance and semantic similarity thresholds to determine their effect on paraphrase filtering.
  - Uses MiniLM-L12 and MPNet similarity scores, along with keyword-preservation and numerical consistency checks.
  - Includes manual review of generated paraphrases to assess semantic preservation and meaningful variation.
- **Inputs**:
  - Original sentences from the Operating Systems domain.
  - Paraphrases generated using the PEGASUS model.
- **Outputs**:
  - Comparison of paraphrase retention across different threshold configurations.
  - Excel results containing retention statistics, candidate details, and manual-review fields.
  - Evidence to support the selection of filtering thresholds for the PARC dataset.
   

