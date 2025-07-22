# CO-CONSERVATION Analysis

This folder contains supplementary data supporting the comparative genomics analysis of NADH dehydrogenases and respiratory quinone biosynthesis genes across bacterial genomes.

---

## 🧬 Objective

To investigate the **co-conservation** of respiratory electron transport components, we systematically analyzed **9,433 bacterial genomes**, focusing on genes involved in quinone biosynthesis (NQ and UQ) and NADH dehydrogenases.

---

## 🔍 Gene Groups Analyzed

Representative genes were selected from five functional groups based on biochemical relevance and pathway specificity:

1. **Classical Menaquinone (NQ) Biosynthesis**  
   - `menB`, `menC`, `menF`

2. **Futalosine Menaquinone (NQ) Biosynthesis**  
   - `mqnA`, `mqnC`, `mqnD`

3. **Ubiquinone (UQ) Biosynthesis**  
   - `ubiA`, `ubiC`, `ubiG`

4. **Type I NADH Dehydrogenase (NDH-1)**  
   - `nuoA`, `nuoE`, `nuoJ`

5. **Type II NADH Dehydrogenase (NDH-2)**  
   - `ndh`

---

## 🧪 Method Summary

- **HMM Profile Generation**: Protein sequences were clustered at 50% identity to reduce redundancy before building HMM profiles.
- **Search & Filtering**:
  - Searches were conducted across genomes using these HMMs.
  - Hits were filtered using **gene-specific e-value thresholds** (see `Gene specific e-values.xlsx`) and a **minimum Bit score of 100**.
- **Co-Conservation Matrix**: Filtered hits were compiled into a binary presence/absence matrix (`Co-conservation table.xlsx`) across genomes for downstream correlation analysis.

---

## 📄 Files in This Folder

| Filename | Description |
|---------|-------------|
| **List of bacterial genomes used in this study.xlsx** | Metadata on 9,433 bacterial genomes used for HMM searches. Includes taxonomic information, genome size, GC content, and classification .Binary matrix of gene presence/absence across ~9,400 bacterial genomes, along with taxonomy, GC content, genome size, and Gram classification.  |
| **Co-conservation table.xlsx** | Curated binary dataset summarizing the presence (`+`) or absence (`−`) of four key respiratory components in each of the 9,433 bacterial genomes:  
- **Ubiquinone (UQ)**  
- **Menaquinone (NQ)**  
- **NDH-1 (Type I NADH dehydrogenase)**  
- **NDH-2 (Type II NADH dehydrogenase)**  
The dataset allows classification of species by their respiratory module usage (e.g., UQ+/NDH-1+, NQ+/NDH-2+), supporting correlation and evolutionary analysis. |
| **Gene specific e-values.xlsx** | Custom e-value cutoffs used to filter HMM search results per gene family. |
| **Sequence similarity and kinetic parameters of NDH-2 from Escherichia coli and Methylococcus capsulatus.xlsx** | Comparative alignment and kinetic data for NDH-2 enzymes, highlighting biochemical divergence between species. |

---

## 📈 Applications

- Identification of respiratory configurations among diverse bacterial clades.
- Discovery of patterns linking quinone usage (UQ vs. MQ) with dehydrogenase preference.
- Insight into the evolutionary flexibility and constraints in electron transport chain organization.

---

## 📌 Notes

- All genome annotations were sourced from NCBI (RefSeq or GenBank).
- The results are suitable for use in phylogenomic studies, clustering, heatmap generation, or network analysis of co-occurring respiratory modules.

