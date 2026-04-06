# B528 High Throughput Methods for Biomedical Data Analysis – Assignment 4

**Author:** Siddharth Rajesh

**Date:** 19 March 2026

---

## Languages, Tools, and Packages

**Language**

- Python (v3.11.11)

**Packages**

- numpy
- pandas

**Tools**

- Jupyter Notebook
- VS Code

---

## Program Overview

This assignment implements a **Position-Specific Weight Matrix (PSWM)** scoring pipeline to identify transcription factor binding sites in *E. coli* K-12 genomic sequences.

1. **Frequency Matrix** – A raw nucleotide counts matrix for the ArgR transcription factor motif is loaded and converted to a frequency matrix using pseudocount smoothing (add-one/Laplace correction).
2. **Scoring Matrix** – Each frequency is converted to a log-odds score: `log2(f / 0.25)`, where 0.25 is the uniform background frequency. Positive scores indicate positions enriched relative to background.
3. **Sequence Scoring** – A sliding window of the motif width (18 bp) is applied across all upstream sequences in the *E. coli* genome. Each window is scored by summing the PWM log-odds values at each position.
4. **Top Hits** – The top 30 highest-scoring segments are reported with their gene ID and score.

---

## Inputs

**Files**:

- `data/argR-counts-matrix.txt` – Tab-separated nucleotide counts matrix (4 rows × 18 columns) for the ArgR binding motif.
- `data/E_coli_K12_MG1655.400_50` – Upstream promoter sequences for *E. coli* K-12 MG1655 genes (400 bp upstream, 50 bp downstream of TSS).

**Parameters**:

- **Pseudocount:** 1 (added to all counts before frequency calculation)
- **Background frequency:** 0.25 (uniform distribution assumed for all four nucleotides)
- **Top-k motifs returned:** 30

---

## Outputs

- **Scoring Matrix** – A styled 4 × 18 DataFrame (rows: A/C/G/T; columns: Pos 1–18) with color-coded log-odds scores (red = negative, green = positive).
- **Top 30 Scoring Segments** – Gene ID and PWM log-odds score for the 30 highest-scoring 18-mer windows found across all input sequences.

---

## Generative AI Disclosure

Generative AI tools were used for code generation and documentation. All analysis logic, results, and interpretations were reviewed and verified by the author.