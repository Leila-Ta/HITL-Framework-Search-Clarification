# HITL-Framework-Search-Clarification

## Bridging Human Judgments and LLMs: A Human-In-The-Loop Framework for Search Clarifications

This repository contains the dataset, prompt templates, and implementation details for the paper:

**Bridging Human Judgments and LLMs: A Human-In-The-Loop Framework for Search Clarifications**   

The paper introduces a **Human-In-The-Loop (HITL) workflow** for improving annotation quality in search clarification tasks. We evaluate multiple **Large Language Models (LLMs)** to assess their ability to replicate human judgments and propose an efficient **hybrid approach** that reduces human effort while maintaining annotation quality.

---

## 📌 Repository Contents

### 📂 **Data**
- **`MIMICS-Duo-HITL.csv`**: Preprocessed dataset based on the **MIMICS-Duo** dataset, annotated for preference ranking, quality assessment, and aspect labelling (coverage, diversity, option order).
- **`sample_annotation_examples.json`**: Example query-clarification pairs and corresponding human labels.

### 📜 **Prompts**
- **`zero_shot_prompt.txt`**: Prompt template for zero-shot annotation.
- **`few_shot_prompt.txt`**: Optimized prompt with few-shot examples.
- **`prompt_variations/`**: Sensitivity analysis prompts to evaluate the effect of different phrasing.

### 🔧 **Code**
- **`annotation_pipeline.py`**: Python script to run annotation tasks using LLMs (GPT-4o, Claude 3, Cohere Command R, Mistral 7B).
- **`hitl_framework.py`**: Implementation of the **Human-In-The-Loop (HITL) system**, integrating confidence thresholding.
- **`evaluation_metrics.py`**: Scripts to compute **accuracy, Cohen’s Kappa, Pearson correlation**, and other evaluation metrics.

### 📊 **Results**
- **`model_comparison.csv`**: Performance of LLMs across different annotation tasks.
- **`HITL_performance_analysis.csv`**: Results from the HITL system showing a reduction in human effort while maintaining annotation quality.

---

## 🚀 How to Use
### 1️⃣ Clone the repository 

---

## 🔬 Research Highlights  
- 🏆 **Human-In-The-Loop (HITL) Workflow** reduces **human annotation efforts by 40%** while maintaining high agreement with human labels.  
- 📝 **Prompt sensitivity analysis** reveals significant performance variations based on phrasing.  
- ⚖️ **LLM limitations**: While **GPT-4o** and **Claude 3** perform well, open-source models like **Mistral 7B** struggle with fine-grained annotations.  

---

## 📄 Citation  
If you find this work useful, please cite:
bibtex
@inproceedings{,
  author = {},
  title = {Bridging Human Judgments and LLMs: A Human-In-The-Loop Framework for Search Clarifications},
}

## 📬 Contact  

For questions or collaboration, feel free to reach out to:  
👩‍💻 **
"
