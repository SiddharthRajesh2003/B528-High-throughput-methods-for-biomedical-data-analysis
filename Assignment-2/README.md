---
title: Assignment-2
author: Siddharth Rajesh
date: 18-02-2026
---

# B528 - Assignment-2

## Languages, tools, and packages

### Language

1. Python

### Packages

1. NumPy
2. Pandas - For loading the data and performing data analysis
3. Scipy - For fitting the data into the exponential decay function
4. gProfiler-official - for Gene Ontology
5. Matplotlib - for visualization

### Tools

1. VS Code

---

## Program Overview

1. This program takes time-series data from [DecayTimecourse.txt](data/DecayTimecourse.txt) and fits the data into an exponential decay model to calculate the half-life of transcripts.
2. Calculates mRNA transcript half-lives for yeast genes using 60-minute decay time series data across 3 replicates.
3. The code is stored in various code blocks to perform some of the following actions: Load the data, Splitting the data into 3 since there are 3 replicates, calculating the half-life of each transcript for each replicate, calculating the average half-life from the 3 replicates, and performing gene ontology enrichment.

---

## Input

**Files:**

1. [DecayTimecourse.txt](data/DecayTimecourse.txt)

---

## Outputs

1. `results/bottom_10_percent_half_life.csv`: Dataframe of genes in the bottom 10% average half-life (most unstable transcripts)
2. `results/top_10_percent_half_life.csv`: Dataframe of genes in the top 10% average half-life (most stable transcripts)
3. `top/bottom_10_gene_list.txt`: Gene list to submit to gProfiler/GOTermFinder
4. `Gene Ontology barplots`: GO enrichment results and bar plots for top and bottom 10% gene sets
5. Half-life summary dataframe with per-replicate and average half-lives for all genes

---

## Generative AI Disclosure

AI tools were used for debugging assistance and for printing the GO enrichment results. All analysis logic, results, and interpretations were reviewed and verified by me.