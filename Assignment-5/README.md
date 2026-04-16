# B528 High Throughput Methods for Biomedical Data Analysis – Assignment 5

**Author:** Siddharth Rajesh

**Date:** 26 March 2026


## Languages, Tools, and Packages

**Language**

- Python (v3.11.11)

**Packages**

- numpy = 2.2.6
- networkx = 3.5
- matplotlib = 3.10.1
- scipy = 1.13.1
- pandas = 2.3.3

**Tools**

- Jupyter Notebook
- VS Code


## Program Overview

This assignment creates a **Human protein-protein interaction network** and calculates some network statistics such as number of nodes/edges, average clustering coefficient, and average degree of each node in the network. It plots the degree distribution of the network and also calculates the shortest path lengths for 2 provided lists of proteins using the network and compares the distribution of the path lengths obtained from the 2 lists respectively.



## Inputs

**Files**:

- `data/Human-PPI.txt` – Tab-separated file containing the edges between proteins (Required to create the network)
- `data/protein-list1.txt` – File containing a list of proteins to be used to calculate the shortest path length between each pair within the list
- `data/protein-list2.txt` - File containing a list of proteins to be used to calculate the shortest path length between each pair within the list

**Parameters**:

- None



## Outputs

- `Network Statistics`:
  - Number of Nodes: 14666
  - Number of Edges in the Protein-Protein Interaction network: 70658
  - Average Clustering Coefficient of the entire network: 0.210
  - Average degree of nodes in the network: 4.818
- `results/degree_distribution.png`: Image of degree distribution of the network in both the normal scale as well as in the log-log scale
- `Mann Whitney U Test`: 
  - *Test Statistic*: 259326.000
  - *P-value*:  0.4879
  - **Conclusion**: The distribution of path lengths between each protein pair in `protein-list1.txt` and `protein-list2.txt` are the same (Fail to reject null hypothesis as P-value > 0.05).
- `results/path_length_comparison.png`: Histogram of obtained path lengths between the each protein pair in `protein-list1.txt` and in `protein-list2.txt` respectively.


## Generative AI Disclosure

Generative AI tools were used for code generation and documentation. All analysis logic, results, and interpretations were reviewed and verified by the author.