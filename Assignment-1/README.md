---
title: Assignment 1
author: Siddharth Rajesh
date: 22 January 2026
---

# B528 - Assignment 1

## Languages

**Language**: Python v 3.11

**Libraries**: Pandas v2.3.2, Seaborn v0.13.2, Matplotlib v3.10.6

**Tools**: Jupyter Notebook, VS Code

---

## Program Overview

This program reads 2 matrices from tab-separated files, calculates the Pearson correlation coefficients between the columns of the matrices, and generates heatmaps to visualize the correlation matrices.

The program contains functions to load the matrices, remove the last column with missing values, compute the correlation matrix, and plot heatmaps using Seaborn.

---

### Input

1. `matrix1.txt`
2. `matrix2.txt`

### Output

1. Heatmap for correlation matrix of Matrix 1 - Head and Neck Cancer is highly correlated with stomach cancer followed by the correlation between bladder cancer with both head and neck cancer and stomach cancer.

2. Heatmap for correlation matrix of Matrix 2 - Bladder and prostate cancer are perfectly correlated with each other followed by Lung adenocarcinoma with cervical cancer showing 98% correlation with each other.

3. Heatmap for correlation matrix between columns of Matrix 1 and Matrix 2 - Uterine cancer from cohort 1 shows a strong correlation of 97% with Prostate cancer from cohort 2. Whereas, bladder cancer from cohort 1 shows similarly strong correlation with both head and neck cancer as well as stomach cancer from cohort 2. It is always important to note correlation does not always equate to causation in cases such as cancer which can be observed in the correlation between uterine and prostate cancer as the 2 cancers are almost always divided between the 2 genders.

---

### Use of generative AI

I did use generative AI to debug some of my code snippets when I was facing issues but I did not use it to generate any code for me. All the code written in the notebook is my own work.