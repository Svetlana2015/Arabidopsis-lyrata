# Genome-wide Analysis of Gene Duplication in *Arabidopsis lyrata*

This repository contains **Jupyter notebooks**, **analysis scripts**, and **selected results** from a genome-wide study of gene duplication patterns in *Arabidopsis lyrata*.

The project focuses on **gene family inference using Markov Clustering (MCL)** under different **BLAST homology filtering stringencies**, and on the **genomic distribution and synteny of duplicated genes**.

The repository is designed to host **fully reproducible analysis code** and **lightweight result files** suitable for upload to GitHub.

---

## Project Overview

Gene duplication is a major driver of genome evolution in plants. In this project, we analyzed duplication patterns in *Arabidopsis lyrata* by:

- Inferring gene families using **Markov Clustering (MCL)**
- Comparing **strict**, **medium**, and **lenient BLAST filtering regimes**
- Quantifying **gene family size distributions**
- Classifying genes as **singletons** or **duplicated**
- Assessing **chromosomal and local genomic distributions**
- Investigating **synteny and collinearity** using dotplot analyses

The analysis highlights how methodological choices in homology detection influence inferred duplication patterns and reveals both global and local structure in the duplicated gene landscape.

## Key Results Summary

### Gene family inference

- Across all datasets, MCL identified approximately **4,700–5,000 gene families**.
- As BLAST filtering became more permissive:
  - Duplicated genes increased from **17,931 (strict)** to **24,111 (lenient)**.
  - Maximum gene family size increased from **70** to **462 genes**.
- Median gene family size showed only a modest increase (**2 → 3 genes**).
- The majority of duplicated genes belong to **small gene families**.

### Gene family size distributions

- Gene family sizes are **strongly right-skewed**.
- Most non-singleton families contain **two genes**.
- Lenient filtering extends the **right tail**, revealing larger and more diverged families.

### Singleton vs duplicated genes

- Under strict filtering, singleton and duplicated genes occur in **comparable proportions**.
- Under lenient filtering, **>75% of genes** are classified as duplicated.

### Chromosomal distribution

- Duplicated genes account for approximately **70–73%** of genes on each chromosome.
- Statistical testing (chi-square and permutation tests) shows:
  - **No significant association** between chromosome and duplication status
  - **Extremely small effect size** (Cramér’s V ≈ **0.02**)

### Local genomic patterns

- Sliding-window analyses reveal **strong local heterogeneity**.
- Regions enriched or depleted in duplicated genes form **local duplication hotspots**.
- Patterns vary across chromosomes and correlate with **gene density**.

### Synteny and collinearity

- Intrachromosomal dotplots show **strong diagonals** and **secondary collinear blocks**.
- Interchromosomal dotplots reveal **fragmented diagonal patterns**.
- Results are consistent with **ancient large-scale duplication events** and subsequent genome rearrangements.

## Methods Overview

- **Homology detection:** BLAST with strict, medium, and lenient filtering thresholds
- **Clustering:** Markov Clustering (MCL)
- **Statistical analyses:**
  - Chi-square tests
  - Permutation-based testing
  - Effect size estimation
- **Genomic analyses:**
  - Sliding-window approaches
  - Chromosome-level summaries
- **Synteny analysis:** Dotplot-based visualization of duplicated genes

All analyses were performed using **custom Python code**.

---

## Requirements

The main analyses were performed using:

- Python ≥ 3.8
- numpy
- pandas
- scipy
- matplotlib
- seaborn
- networkx (for graph-based analyses)
- jupyter

## Reproducibility

All figures and statistics reported in the accompanying report can be reproduced by running the notebooks in the order provided.

Notebooks are **self-contained** and include explanations of each analysis step.

## Contact

For questions or suggestions, feel free to open an issue or contact the repository owner sannikovasvetlana777@gmail.com.
