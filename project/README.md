# Cleared for Launch: AI Governance Assessment

## Project Overview

You are an **AI Governance Analyst at MedAssist AI**, preparing **ClinicalCompanion** — a generative AI clinical decision support system — for EU market launch within 3 months. Your manager needs a governance assessment before the board meeting next week.

ClinicalCompanion is powered by a third-party foundation model and analyzes patient records to generate diagnostic suggestions for physicians. You must deliver a comprehensive governance package covering regulatory compliance, risk assessment, vendor governance, model documentation, and ongoing monitoring.

## Project Structure

```
project/
├── README.md                 ← You are here
├── starter/                  ← STUDENT WORKSPACE (start here)
│   ├── README.md             ← Detailed instructions and step-by-step guide
│   ├── data/                 ← Input datasets (10 files — do not modify)
│   ├── results/              ← Your visualizations go here
│   ├── governance_assessment.ipynb   ← Code deliverable (TODO stubs)
│   └── governance_workbook.xlsx      ← Written deliverable (blank templates)
│
└── solution/                 ← SOLUTION KEY (for reviewers only)
    ├── README.md             ← Reviewer guide
    ├── data/                 ← Same input datasets
    ├── results/              ← Completed visualizations (6 PNGs)
    ├── governance_assessment.ipynb   ← Complete notebook
    └── governance_workbook.xlsx      ← Complete workbook
```

## Getting Started

### Dependencies

```
Python 3.8+
pandas
matplotlib
seaborn
numpy
jupyter
openpyxl
```

### Installation

1. Install the required Python packages:

```bash
pip install -r requirements.txt
```

2. Navigate to the **starter** directory and launch Jupyter Notebook:

```bash
cd project/starter
jupyter notebook governance_assessment.ipynb
```

3. Read `starter/README.md` for the full step-by-step guide.

## Student Deliverables (2 files)

| # | Governance Area | Notebook | Workbook |
|---|---|---|---|
| 1 | EU AI Act Classification | Compliance gap analysis | Classification reasoning + gap table |
| 2 | Risk Register + Heatmap | Risk heatmap + mitigation chart | Risk details, scores, mitigations |
| 3 | Vendor Evaluation | Vendor scorecard visualizations | Evaluation narrative + recommendation |
| 4 | Model Card | Disaggregated performance chart | Full Model Card (Mitchell et al.) |
| 5 | Monitoring & Incident Response | 4-panel monitoring dashboard | KPI definitions + incident plan |
| 6 | Executive Summary | Readiness gauge dashboard | Board-ready narrative |

## Estimated Time: ~5 hours

- Notebook (code + analysis): ~3.5 hours
- Workbook (written deliverables): ~1.5 hours

## Built With

* [Python 3.8+](https://www.python.org/) — Programming language
* [pandas](https://pandas.pydata.org/) — Data analysis and manipulation
* [matplotlib](https://matplotlib.org/) — Data visualization
* [seaborn](https://seaborn.pydata.org/) — Statistical data visualization
* [Jupyter Notebook](https://jupyter.org/) — Interactive computing environment

## License
[License](../LICENSE.md)
