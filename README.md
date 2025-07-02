# Reliable Annotations with Less Effort: Evaluating LLM-Human Collaboration in Search Clarifications

**Authors:**  
Leila Tavakoli (Services Australia)  
Hamed Zamani (University of Massachusetts Amherst)  

**[paper](https://arxiv.org/abs/2507.00543)**

---

## Overview

This repository accompanies the paper:

> **Reliable Annotations with Less Effort: Evaluating LLM-Human Collaboration in Search Clarifications**  
> Proceedings of the 2025 International ACM SIGIR Conference on Innovative Concepts and Theories in Information Retrieval (ICTIR '25), Padua, Italy.  
> [[ACM DL]](https://doi.org/10.1145/3731120.3744574) | [[arXiv]](https://arxiv.org/abs/2507.00543)

We present a lightweight **human-in-the-loop (HITL) annotation framework** for complex IR tasks, combining multiple LLMs, confidence aggregation, and selective human review to reduce annotation effort by up to 45% while preserving quality.  
This repo provides **all data, code, prompts, and analyses** needed to reproduce our main results.

---

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Leila-Ta/HITL-Framework-Search-Clarification.git
   cd HITL-Framework-Search-Clarification

---

## Install Dependencies

Most code is in Python and requires standard NLP/data science libraries, such as:
- `pandas`
- `numpy`
- `scikit-learn`

For running LLMs, you will need API access for **GPT-4o**, **Claude 3**, **Cohere Command R**, or **Mistral 7B**, or you may use your own open-source model.

---

## Reproducing Results

- **Run scripts in `Code/`** to preprocess the dataset and run the annotation pipeline.
- **Use prompts in `Prompt/`** for replicating LLM-based annotation and sensitivity studies.
- **Intermediate and final outputs** are stored in `Result/`.

---

## Datasets

- The primary dataset is **[MIMICS-Duo](https://github.com/Leila-Ta/MIMICS-Duo)**, used in compliance with its license.
- Processed subsets and sample files are provided under `Analyses/`.

---

## Main Features

- **HITL Workflow:** Modular implementation for annotation with confidence and inter-model disagreement thresholding.
- **Prompt Sensitivity:** Multiple prompt templates and ablations.
- **Reproducibility:** All major findings and plots are reproducible from the provided scripts and data.
- **Evaluation:** Scripts to compute macro-F1, weighted Cohen’s kappa, confusion matrices, human effort reduction (HER), and more.

---

## Citation

If you use this codebase, data, or prompts, please cite:

```bibtex
@inproceedings{tavakoli2025hitl,
  author    = {Leila Tavakoli and Hamed Zamani},
  title     = {Reliable Annotations with Less Effort: Evaluating LLM-Human Collaboration in Search Clarifications},
  booktitle = {Proceedings of the 2025 International ACM SIGIR Conference on Innovative Concepts and Theories in Information Retrieval (ICTIR)},
  year      = {2025},
  location  = {Padua, Italy},
  doi       = {10.1145/3731120.3744574}
}
