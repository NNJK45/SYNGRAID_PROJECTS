# SYNGRAID_PROJECTS
The official code implementation of SYNGRAID from our paper:

SYNGRAID: A Retrosynthetic AI Model for Small Molecule Detection Using a Biomedical Knowledge Graph Integrating Diseases, Drugs, and Genes

## Model Description
The SYNGRAID model (Synthesis Graph-based Retrosynthetic AI Designer) is a novel architecture designed to predict relevant small molecules (e.g., drugs) by leveraging a heterogeneous biomedical knowledge graph that integrates diseases, drugs, and genes.

## The model combines:

Graph Neural Networks (GNN) for node-type-specific embeddings,

Graph Attention Networks (GAT) for relation weighting, and

XGBoost for the final classification of molecular associations.

This approach enables precise detection of candidate small molecules associated with diseases through a deep understanding of gene–disease–drug interactions.

##  Architecture Steps
Step 1: Knowledge graph construction from tripartite relationships (disease-drug, gene-disease, gene-drug)
Step 2: Node-type-specific embedding with GNN modules
Step 3: Graph attention fusion to highlight biologically relevant interactions
Step 4: Classification via XGBoost to detect drug–disease associations
 Final output: Probability scores indicating how likely a drug (small molecule) is to be therapeutically associated with a disease.

# Setup
First, clone this repository:

bash
Copier
Modifier
git clone[ https://github.com/<your-org-or-username>/SYNGRAID.git](https://github.com/NNJK45/SYNGRAID_PROJECTS.git)
cd SYNGRAID
bash
Copier
Modifier
pip install -r requirements

## Environment Requirement
- tensorflow-gpu == 1.13.1
- keras == 2.2.4
- scikit-learn == 0.22.2


## Files and Notebooks
main.py: Main training and evaluation script

loader.py: Prepares graph and datasets (supports gene/drug/disease integration)

model.py: Model definition (GNNs, GAT, classifier)

ANALYSIS.py and evaluation.py: Complete training pipeline

data: Contains processed datasets (Fdataset, Cdataset, LRSSL)


## Datasets
Fdataset/, Cdataset/, LRSSL/: Biomedical knowledge graphs with disease-drug-gene relationships


## Evaluation Metrics
SYNGRAID is evaluated on 3 public datasets using:

AUROC (Area Under Receiver Operating Curve)

AUPR (Area Under Precision-Recall Curve)

## SYNGRAID achieves AUROC = 0.99421 and AUPR = 0.84684, outperforming several state-of-the-art models.

📖 Citation
If you use this work, please cite:

