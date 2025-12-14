# Text Classification with LLM Prompt Engineering

This repository contains prompt-engineering experiments using Large Language Models (LLMs) for **text classification of business event descriptions**, conducted as part of ongoing research work.

The project evaluates **zero-shot and few-shot prompting strategies**, focusing on producing both a predicted class and a coherent natural-language explanation.

---

## Project Overview

The task involves classifying business-related text into predefined categories using structured prompts.  
The same prompt template is reused across datasets, while the input text fields vary depending on the data source.

Experiments are organized to clearly separate:
- Prompt design
- Model execution (zero-shot vs few-shot)
- Prediction outputs

---

## Repository Structure

```
Text-Classification-with-LLM-Prompt-Engineering/
├── notebooks/         # Few-shot prompting scripts (Jupyter notebooks)
├── predictions/       # Zero-shot prediction outputs (CSV / XLSX)
├── prompt-template/   # Prompt templates used for classification
└── README.md
```

---

## Notebooks (`notebooks/`)

This folder contains **few-shot prompting scripts** implemented as Jupyter notebooks.

Each notebook:
1. Loads the dataset
2. Applies a few-shot prompt template
3. Runs LLM inference
4. Saves model predictions for analysis

These notebooks are designed to extend and compare against zero-shot results.

---

## Predictions (`predictions/`)

This folder contains **zero-shot prediction outputs** generated using prompt-only classification.

The prediction files include:
- Predicted class labels
- Model-generated explanations
- Timestamped outputs for traceability

These results are used for comparison against few-shot prompting methods.

---

## Prompt Template (`prompt-template/`)

This folder contains the **prompt template** used across all experiments.

The template:
- Defines the classification task
- Specifies the expected output format
- Enforces internal consistency between predicted category and explanation

Dataset-specific input fields are substituted into this template as needed.

---

## Status

- Zero-shot prompting: **Completed**
- Few-shot prompting: **In progress**

The repository will be updated as experiments continue.
