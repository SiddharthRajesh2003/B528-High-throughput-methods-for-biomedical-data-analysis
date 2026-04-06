# B528 High Throughput Methods for Biomedical Data Analysis – Assignment 3

**Author:** Siddharth Rajesh

**Date:** 12 March 2026

---

## Languages, Tools, and Packages

**Language**

- Python (v3.11.11)

**Packages**

- collections (standard library — `defaultdict`)

**Tools**

- Jupyter Notebook
- VS Code

---

## Program Overview

The program predicts operons — defined as the longest contiguous multi-gene transcriptional units — across five microbial genomes.

The workflow consists of parsing gene annotation files (PTT and GFF formats), sorting genes by chromosomal position within each contig, and applying a sliding-window rule: adjacent co-directional genes whose intervening intergenic distance is less than 50 bp are grouped into the same operon. Only groups of two or more genes are reported as operons.

Additional considerations include the metagenome case (Hoatzin crop microbiome), where genes are distributed across many contigs. Contig boundaries are strictly respected — genes on different contigs are never merged — before applying the same operon-calling logic.

---

## Inputs

**Files**:

- `data/E_coli_K12_MG1655.ptt`: PTT gene annotation file for *Escherichia coli* K-12 MG1655 (NCBI PTT format)
- `data/B_subtilis_168.ptt`: PTT gene annotation file for *Bacillus subtilis* 168
- `data/Halobacterium_NRC1.ptt`: PTT gene annotation file for *Halobacterium* sp. NRC-1
- `data/Synechocystis_PCC6803_uid159873.ptt`: PTT gene annotation file for *Synechocystis* sp. PCC 6803
- `data/2088090036.gff`: GFF3 gene annotation file for the Hoatzin crop microbiome

**Parameters**:

- `distance_threshold`: Maximum intergenic distance (bp) for two genes to be considered co-operonic / default value: `50`

---

## Outputs

- Printed operon table per genome: contig (GFF only), operon start..end coordinates, gene count, and gene names/locus tags
- Final line per genome: total number of predicted operons

---

## Generative AI Disclosure

Generative AI tools were used for code generation and documentation. All analysis logic, results, and interpretations were reviewed and verified by the author.
