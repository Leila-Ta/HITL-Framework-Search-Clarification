# HITL-Framework-Search-Clarification

## Bridging Human Judgments and LLMs: A Human-In-The-Loop Framework for Search Clarifications

This repository contains the dataset, prompt templates, and implementation details for the paper:

**Bridging Human Judgments and LLMs: A Human-In-The-Loop Framework for Search Clarifications**  
Leila Tavakoli, Hamed Zamani  

The paper introduces a **Human-In-The-Loop (HITL) workflow** for improving annotation quality in search clarification tasks. We evaluate multiple **Large Language Models (LLMs)** to assess their ability to replicate human judgments and propose an efficient **hybrid approach** that reduces human effort while maintaining annotation quality.

---

## 📌 Repository Contents

### 📂 **Data**
- **`MIMICS-Duo-HITL.csv`**: Preprocessed dataset based on the **MIMICS-Duo** dataset, annotated for preference ranking, quality assessment, and aspect labeling (coverage, diversity, option order).
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
- **`HITL_performance_analysis.csv`**: Results from HITL system showing reduction in human effort while maintaining annotation quality.

---

## 🚀 How to Use

### 1️⃣ Clone the repository
```bash
git clone https://github.com/Leila-Ta/HITL-Framework-Search-Clarification.git
cd HITL-Framework-Search-Clarification
## 🚀 Installation & Usage

### 2️⃣ Install Dependencies
Ensure you have **Python 3.8+** and install the required packages:

```bash
pip install -r requirements.txt
## 🚀 Running the HITL Framework

### 3️⃣ Run LLM-Based Annotations
Modify **`annotation_pipeline.py`** with your **OpenAI API key** and run:

```bash
python annotation_pipeline.py
## 📊 4️⃣ Evaluate Performance  
Run the following command:  

```bash
python evaluation_metrics.py
## 🏗️ 5️⃣ Apply the HITL Framework  
Run the following command:  

```bash
python hitl_framework.py
## 📜 Script Overview  
This script:  
- 🚩 **Flags low-confidence cases** for human review.  
- 🔄 Uses **majority voting** across models to improve annotation consistency.  
- ⚖️ Helps balance **automation** and **human oversight**.  

---

## 🔬 Research Highlights  
- 🏆 **Human-In-The-Loop (HITL) Workflow** reduces **human annotation efforts by 40%** while maintaining high agreement with human labels.  
- 📝 **Prompt sensitivity analysis** reveals significant performance variations based on phrasing.  
- ⚖️ **LLM limitations**: While **GPT-4o** and **Claude 3** perform well, open-source models like **Mistral 7B** struggle with fine-grained annotations.  

---

## 📄 Citation  
If you find this work useful, please cite:  

```bibtex
@inproceedings{tavakoli2025HITL,
  author = {Tavakoli, Leila and Zamani, Hamed},
  title = {Bridging Human Judgments and LLMs: A Human-In-The-Loop Framework for Search Clarifications},
}

## 📬 Contact  

For questions or collaboration, feel free to reach out to:  
👩‍💻 **Leila Tavakoli** – [GitHub](https://github.com/Leila-Ta) | [LinkedIn](https://www.linkedin.com/in/leilatavakoli)
