# 🧬 Genome Structural Variant Impact Analysis  
Proof-of-concept analysis to identify structural variants impacting regulatory elements (enhancers, TADs) in the PC-3 cell line.

---

## **Overview**
This repository presents a **proof-of-concept (PoC)** computational framework designed to explore how **structural variants (SVs)** — such as deletions, duplications, and translocations — affect **regulatory regions** of the genome.  
By integrating genomic annotations, structural variant data, and 3D regulatory maps, this project aims to uncover how **genome rearrangements** can disrupt enhancer–promoter communication and alter transcriptional programs.  

The prototype dataset focuses on the **PC-3 prostate cancer cell line**, providing an initial example of how structural variation may reshape genome topology and influence gene regulation.

---

## **Biological Motivation**
Cell identity and function depend on a stable relationship between **genome architecture** and **regulatory signaling**.  
Structural variants can rearrange chromatin topology, breaking or forming new **gene–gene and enhancer–promoter loops**.  
Understanding these changes is key to explaining **tumor plasticity**, **gene misregulation**, and **adaptive cellular behavior** in cancer.  

This project combines **wet-lab insight** with **computational modeling** to bridge this complexity.

---

## **Objectives**
- Identify and annotate SVs overlapping regulatory elements.  
- Quantify proximity of SVs to enhancers and TAD boundaries.  
- Visualize affected genomic regions as network graphs.  
- Create a flexible framework for expanding to new datasets and cancer types.  

---

## **Workflow**
1. **Input Data**
   - Structural variant (SV) calls in VCF or BEDPE format  
   - Enhancer, promoter, and TAD annotations  
   - Optional expression data  

2. **Processing**
   - Parse SV coordinates  
   - Calculate overlaps with regulatory regions  
   - Score potential impact using distance and feature weights  
   - Generate annotated output tables and network graphs  

3. **Output**
   - Annotated tables of SV–regulatory element intersections  
   - Summary plots of impact frequency per region  
   - Example interaction networks showing disrupted loops  

---

## **Example Notebook**
The included notebook [`PoC_SV_Impact_Analysis.ipynb`](./PoC_SV_Impact_Analysis.ipynb) demonstrates the workflow on simplified PC-3 cell line data.  
It is intended as a foundation for future expansions, including integration with chromatin interaction (Hi-C) and transcriptomic datasets.

---

## **Future Directions**
- Extend analysis to multi-cell datasets (ENCODE, TCGA).  
- Incorporate machine learning to predict enhancer–gene disruption probabilities.  


---

## **Technical Stack**
| Category | Tools / Libraries |
|-----------|------------------|
| **Language** | Python 3 |
| **Core Libraries** | `pandas`, `numpy`, `matplotlib`, `networkx`, `pybedtools` |
| **Environment** | Jupyter Notebook / VS Code |
