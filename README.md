# Language Style Analysis NLP Project

This project explores the effect of prompt rephrasing and style variation on multiple-choice question answering across different large language models.  

---

## Setup Instructions

### 1. Data
- Download the **MMLU dataset** from [Hugging Face](https://huggingface.co/datasets/ncoop57/mmmlu).
- Place it in the **root of the project**.

### 2. API Keys
You will need valid API access for:
- **Hugging Face Hub** (to load models like LLaMA 2, LLaMA 3.2, BART, DeBERTa).
- **Gemini API key** (used for rephrasing prompts).

Make sure you have permission to use all the models required in this project.

Store your keys in the respective code variables in the notebooks.  

---

## Workflow

1. **Parse the dataset**  
   Run [`parse_mmmlu.ipynb`](parse_mmmlu.ipynb)  
   This will preprocess the MMLU dataset into a format used for evaluation.

2. **Evaluate baseline styles**  
   Run [`style_analysis.ipynb`](style_analysis.ipynb)  
   This notebook evaluates the models (LLaMA 2, LLaMA 3.2, BART, DeBERTa) on the styled prompts.

3. **Rephrase prompts as plain text**  
   Run [`rephrase_prompts_as_plain.ipynb`](rephrase_prompts_as_plain.ipynb)  
   This will rephrase all prompts tested in the previous step into a plain form using Gemini.  

4. **Evaluate rephrased prompts**  
   Run [`style_analysis_rephrased_plain.ipynb`](style_analysis_rephrased_plain.ipynb)  
   This notebook evaluates the models on the rephrased plain prompts.

---

## Requirements

Install dependencies from the provided `requirements.txt`:

```bash
pip install -r requirements.txt
