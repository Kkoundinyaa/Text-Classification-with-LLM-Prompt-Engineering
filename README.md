# InfoEvents Classification with LLM Prompting (Fisher Research)

**TL;DR:** Zero-shot (and soon few-shot) prompting pipeline to classify InfoEvents deals into **ICEV / EV / Neither**, with explanation consistency checks.  
**Data note:** Raw datasets are not included due to access restrictions, but notebooks, prompts, predictions, and evaluation reports are provided for reproducibility.

## Datasets (not shared)
Three internal datasets were used:
- **InfoEvents1 (Acquisitions):** fields `targetbusinessdescription`, `dealsynopsis`
- **InfoEvents2 (Venture Capital Investments):** fields `descriptionshort`, `categroup`
- **InfoEvents3 (Alliances):** fields `dealsynopsistext`, `allianceactivity`, `applicationandtechnologytext`

## Method
- Prompt-based classification (zero-shot first)
- Output schema includes **category + explanation**, with an additional instruction to ensure internal consistency between them.
- Standardized prompt format across datasets with dataset-specific input-field descriptions.

## Results (Zero-shot, prompt v1.3e, GPT-4o)
Summary from `reports/Report-8.pdf`:
- **InfoEvents1:** Accuracy **0.8976**
- **InfoEvents2:** Accuracy **0.8814**
- **InfoEvents3:** Accuracy **0.8917**

Class-wise precision/recall/F1 and confusion matrices are included in the report.

## Repository Contents
- `prompts/` — prompt versions used for experiments
- `notebooks/` — zero-shot / few-shot runs (Colab/Jupyter)
- `predictions/` — model outputs (CSV/XLSX)
- `reports/` — evaluation reports and confusion matrices
- `results/` — short “latest results” summary (human-readable)

## How to run (without the private datasets)
To reproduce the pipeline logic:
1. Open a notebook in `notebooks/`
2. Replace the dataset loading cell with your authorized dataset path or dataframe
3. Run the prompt generation + inference cells
4. Export predictions into `predictions/<dataset>/`

## Status
Ongoing research for Fisher College of Business:
- Zero-shot: complete for v1.3e
- Few-shot: in progress
- Document analysis phase: upcoming
