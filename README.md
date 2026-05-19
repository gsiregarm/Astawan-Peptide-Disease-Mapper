# Astawan-Peptide-Disease-Mapper
# Functional Biomimetic Peptides & Network Pharmacology Pipeline

**Author:** M. Ghassan Fattah
**Institution:** Master's Program in Food Science, IPB University  

## 🔬 Overview
This repository contains a comprehensive, state-of-the-art computational pipeline designed to process mass spectrometry-derived peptide sequences (specifically from complex degradomes like fermented *Tempe*) and transform them into actionable polypharmacological networks. 

The pipeline integrates sequence alignment, target prediction, and systems biology to bridge the gap between ultra-short bioactive peptides and complex human disease pathways.

## ✨ Key Features
* **Automated Data Sanitization:** Cleans raw peptide sequences, removes PTMs, and filters out statistically ambiguous fragments ($< 6$ amino acids by default, adjustable for functional tetrapeptides).
* **Heuristic Alignment Engine:** Utilizes multiprocessing and the Smith-Waterman algorithm (BLOSUM62) to map short bioactive peptides to human proteome targets.
* **Deep Disease Mapping:** Queries the Open Targets GraphQL API to dynamically extract gold-standard disease associations and secondary targets.
* **Master Heterogeneous Network Generation:** Merges bipartite connections (Peptide $\rightarrow$ Protein $\rightarrow$ Disease) with unipartite Protein-Protein Interactions (PPI) via the STRING API.
* **Cytoscape & Arena3D Ready:** Automatically formats and exports node and edge tables with assigned topological properties and shapes for immediate 2D/3D visualization.

## 🛠️ Prerequisites & Installation
This pipeline is optimized for **Google Colab** but can be run locally via Jupyter Notebook. 

**Required Python Packages:**
```bash
pip install biopython requests pandas tqdm
