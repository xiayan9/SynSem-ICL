
## 🚀 Highlights

- **Structure-aware Graph Transformer**  
  Encodes dependency trees with **tree-distance bias** and **dependency-type bias** to produce syntactic sentence embeddings.

- **Bidirectional cross-attention fusion**  
  Deeply fuses word-level syntactic representations with subword-level semantic representations via **Syn→Sem** and **Sem→Syn** attention.

- **Dual-similarity contrastive learning**  
  Aligns the fused representation space with **semantic similarity** and **syntactic similarity**, using **hard negatives** in both views.

- **Strong few-shot performance**  
  - On **ASTE-Data-V2**, with only **5 retrieved examples**, SynSem-ICL achieves F1 within **4–8%** of fully supervised models.  
  - On **SemEval-2022 Task 10** (multilingual structured sentiment), it brings up to **+8.1 SF1** improvement on morphologically rich languages.

---

## 📌 Repository Status

> **Important:**  
> This repository is currently a **placeholder** for the paper submission.  
> - The full source code will be **released after the paper is accepted and officially published**.  
> - The structure of the repository and this README already reflect the final code organization for reproducibility.

Planned release items:

- [x] Project structure and documentation  
- [x] Method overview figures  
- [ ] Training scripts for syntactic encoder and fusion model  
- [ ] Contrastive training pipeline for SynSem-ICL  
- [ ] Example retrieval pipeline and ICL prompting scripts  
- [ ] Pretrained checkpoints and configuration files  

---

## 🧠 Method Overview

### 1. Overall SynSem-ICL Framework

![SynSem-ICL Framework](Figures/SynSem-ICL_framework.pdf)

> *Figure 1. Overall architecture of SynSem-ICL, including syntactic encoder, cross-attention fusion, and dual-similarity contrastive training.*

### 2. Structure-Aware Syntactic Encoder

![Syntactic Encoding Pipeline](Figures/cross_attention_fusion.pdf)

> *Figure 2. Syntactic encoding pipeline from raw text to structure-aware sentence representations, based on a Graph Transformer with tree-distance and dependency-type biases.*

### 3. Bidirectional Cross-Attention Fusion

![Cross-Attention Fusion](Figures/syntactic_encoding_pipeline.pdf)

> *Figure 3. Bidirectional cross-attention between semantic and syntactic representations, followed by multi-granularity pooling to obtain the fused sentence representation.*

---

