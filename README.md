# GBMDriver_features

GBMDriver_features is a sequence-based feature extraction pipeline designed to calculate evolutionary, physicochemical, and motif-based features for protein mutations.

## Prerequisites

To use this tool, you must prepare the following data in the `data/` directory:

### 1. Sequence & Mapping
* **`whole_proteome_uniprot_id.xlsx`**: Mapping of UniProt IDs to Gene Names and Sequences.

### 2. Evolutionary Profiles
* **PSSM Files (`.pssm`)**: Generated via PSI-BLAST against the **UniRef90** database.
* **AACon Scores (`.csv`)**: Conservation metrics from the [AACon Server](http://www.compbio.dundee.ac.uk/aacon/).

### 3. Physicochemical Indices
* **Property Tables**: `49_properties_normalizedValues.csv`, `49_properties_numerical_Values.csv`, and `463_unique_numerical_properties.csv`.
* **Mutation Matrices**: `aaindex_square_diagonal_properties.csv`.

### 4. Disease-Specific Motifs
* **`BRCA_odds_ratio.xlsx`**: Odds ratio calculations for di- and tri-peptide motifs based on disease-specific datasets.

### 5. Predicted Secondary Structure
* **NetSurfP-3.0**: Predicted secondary structure for residues (used for classification). [NetSurfP-3.0 Server](https://services.healthtech.dtu.dk/service.php?NetSurfP-3.0).

## 🛠️ Installation

```bash
pip install pandas numpy openpyxl
