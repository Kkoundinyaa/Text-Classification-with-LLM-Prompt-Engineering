# Text Classification with LLM Prompt Engineering

This repository contains prompt-based text classification experiments using Large Language Models (LLMs), conducted as part of an ongoing research collaboration with **Fisher College of Business**.

The focus of this work is to evaluate **zero-shot and few-shot prompting strategies** for classifying business event descriptions into predefined categories, along with generating concise, internally consistent explanations.

---

## Project Overview

The classification task is applied to three types of business events:
- Acquisitions
- Venture Capital Investments
- Strategic Alliances

Each dataset is handled using a **separate script/notebook** for clarity and controlled experimentation.  
The same base prompt structure is reused across datasets, with only the input field descriptions adapted as required.

---

## Repository Structure

```
Text-Classification-with-LLM-Prompt-Engineering/
├── notebooks/     # Zero-shot / few-shot prompting experiments
├── predictions/   # Model outputs (CSV / XLSX)
├── reports/       # Evaluation reports and analysis
├── prompts/       # Prompt versions used in experiments
├── results/       # High-level summaries (ongoing)
└── README.md
```

---

## Notebooks

The core experiments are implemented as Jupyter notebooks.

### Zero-shot Classification
- One notebook per dataset
- Uses a single prompt with no labeled examples
- Produces a predicted category and a natural-language explanation

### Few-shot Classification (In Progress)
- Extends the same prompt with a small number of labeled examples
- Enables direct comparison against zero-shot performance

Each notebook follows the same pipeline:
1. Load dataset
2. Construct prompt
3. Run LLM inference
4. Save predictions to disk

---

## Predictions

The `predictions/` directory contains model outputs for each dataset, including:
- Predicted class labels
- Model-generated explanations
- Timestamped result files for traceability

These outputs are used for downstream evaluation and error analysis.

---

## Reports

The `reports/` directory contains evaluation summaries, including:
- Overall accuracy and class-wise metrics
- Confusion matrices
- Qualitative observations from prompt-based classification

---

## Status

- Zero-shot prompting: **Completed**
- Few-shot prompting: **In progress**
- Document-level analysis: **Upcoming**

This repository will be updated incrementally as experiments continue.
