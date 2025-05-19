# BF528 FINAL PROJECT (scRNA-seq)

## Project Overview

This project analyzes the single-cell transcriptomic landscape of matched primary pancreatic tumors and liver metastases from patients with pancreatic ductal adenocarcinoma (PDAC), based on the study by Zhang et al. (2023, Nature Communications). I aimed to replicate and extend key analyses from the paper, including cell type annotation, composition comparisons, pseudotime trajectory modeling, and compositional modeling. By applying tools like CellTypist, Monocle, and scCODA to the provided dataset, this work explores how immunosuppressive microenvironments and distinct cellular lineages contribute to metastatic progression in PDAC.

# Use

## Repo Contents
- analysis.ipynb: Contains all preprocessing/QC, normalization, clustering, annotation, and two reproduced results from the paper.
- analysis.pdf: Readble version of analysis
- sccoda_analysis.ipynb: Contains additional analysis on results using scCODA
- sccoda_analysis.pdf: Readable version of scCODA analysis
- envs/: contains environment files necessary for creating conda environments to use each notebook

## Creating analysis env
run
```bash
conda env create -f envs/finalproj_scrnaseq.yml
```

Open analysis.ipynb, select kernel, Python environments, finalproj_scrnaseq

## Creating sccoda env
run 
```bash
conda env create -f envs/sccoda_env.yml
```
once complete run:
```bash
conda env create -f sccoda_env.yml
conda activate sccoda_env
```

Then:
```bash
pip install sccoda --no-deps
pip install tensorflow==2.13.1 tensorflow-probability==0.21 arviz==0.15.1
```

# Source of data:
Zhang, S., Fang, W., Zhou, S. et al. Single cell transcriptomic analyses implicate an immunosuppressive tumor microenvironment in pancreatic cancer liver metastasis. Nat Commun 14, 5123 (2023). https://doi.org/10.1038/s41467-023-40727-7
