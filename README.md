# Exploring the Integration of Single-Cell RNA Sequencing Datasets: Human Lung Cell Atlas (HLCA)

This project is an in-depth exploration of the integration of multiple single-cell RNA sequencing (scRNA-seq) datasets, inspired by the [Human Lung Cell Atlas (HLCA)](https://doi.org/10.1038/s41591-023-02327-2) study published in *Nature Medicine* last year. The HLCA successfully integrated 49 datasets, representing data from 49 independent studies, into a unified atlas, enabling unprecedented insights into lung cell biology.

In this repository, we focus on understanding and reproducing the integration process of the core HLCA dataset, which comprises 13 datasets of healthy lung scRNA-seq studies. This exploration emphasizes how different decisions in preprocessing, normalization, batch-effect correction, clustering, and annotation affect the resulting integrated dataset.

---

## Methodology

The project leverages the raw matrices, metadata, and code provided by the HLCA study. The analysis is implemented in Python, using **Polars** for handling tabular data and **Scanpy** for single-cell analysis workflows. The computations are performed in a **Jupyter Notebook** environment, running on a remote Linux server equipped with an NVIDIA 4090 GPU.

---

## Progress and Status

This project is a work in progress, and the current focus is on:

- **Reproducing** the construction of the core HLCA dataset.
- **Implementing** initial comparisons of normalization, batch-effect correction, and clustering results.
- **Expanding** the analysis to explore more recent integration or interpretability techniques.

---

## Current Explorations

To better understand the differences among the 13 datasets in the core HLCA, we have conducted several analyses. First, we analyzed the number of donors per study and the total cells per study, which revealed substantial variability in sample sizes across studies. Next, we examined the total counts per study, the total counts per donor within a single study, and the total counts per cell in a single donor. These metrics demonstrated significant differences in library size, not only across datasets but also within individual datasets. Additionally, we observed the effects of different sequencing chemistries, such as 10X Genomics v2 vs. v3, within the same study. These differences in cell numbers and counts highlighted the challenges in normalizing and correcting for library size variations.

![Dataset Statistics](./figures/datasets_statistics.png)

---

## Contributions and Learning Goals

This project is aimed at enhancing understanding and accessibility of large-scale scRNA-seq dataset integration for both personal learning and the broader research community. Contributions, discussions, and collaborations are welcome to refine and expand this exploration.

---
