# Cleared for Launch: AI Governance Assessment

Conduct a comprehensive AI governance assessment for a healthcare generative AI system preparing for EU market launch.

---

## Overview

### What You'll Learn

You will apply real-world AI governance frameworks to assess a clinical decision support system called ClinicalCompanion. By the end of this project, you will have produced a complete governance package — code-driven analysis with professional visualizations and a written assessment workbook — covering regulatory compliance, risk management, vendor governance, model documentation, and post-deployment monitoring.

Learning objectives:
- Classify an AI system under the EU AI Act risk framework and perform a compliance gap analysis
- Assess AI risks using the NIST AI Risk Management Framework and visualize them with a risk heatmap
- Evaluate a third-party AI model vendor across governance categories
- Document disaggregated model performance using the Model Card framework (Mitchell et al., 2019)
- Design a post-deployment monitoring dashboard and incident response plan
- Synthesize governance findings into a board-ready executive summary

### Prerequisites

- Comfortable loading CSV files with pandas and creating plots with matplotlib/seaborn
- Familiar with Python dictionaries and JSON data
- All governance concepts are covered in the course modules

---

## Understanding the Concept

### The Problem

MedAssist AI is preparing to launch ClinicalCompanion — a generative AI clinical decision support system — in the European Union within 3 months. ClinicalCompanion uses a third-party foundation model to analyze patient records and generate diagnostic suggestions for physicians. Before the board meeting next week, leadership needs to understand: Is this system ready for launch? What are the regulatory risks? Where are the compliance gaps?

### The Solution

A structured governance assessment that evaluates the system across six areas: EU AI Act compliance, risk management, vendor governance, model documentation, monitoring, and executive readiness. This produces the evidence package a board needs to make an informed launch decision.

### How It Works

The assessment follows a systematic workflow that mirrors how governance analysts work in practice:

**Step 1: System Understanding**
Load the system specification and training data summary to establish what you're assessing — the system type, architecture, intended users, and data sources.

**Step 2: Regulatory Classification**
Walk through the EU AI Act decision tree (Article 5 prohibited practices → Article 6(1) safety component → Annex III high-risk categories) to classify the system, then analyze compliance gaps against Articles 8-15.

**Step 3: Risk Assessment**
Load the risk register, compute statistics across NIST AI RMF functions (Govern, Map, Measure, Manage), and analyze mitigation effectiveness by comparing pre- and post-mitigation scores.

**Step 4: Risk Visualization**
Create a 5×5 risk heatmap plotting individual risks by likelihood and impact, plus a grouped bar chart comparing pre- vs. post-mitigation scores.

**Step 5: Vendor Evaluation**
Calculate category-level and overall vendor scores, then visualize the governance scorecard with a bar chart and radar/spider chart.

**Step 6: Model Card Performance**
Analyze disaggregated Top-3 Diagnostic Accuracy across subgroups, identify underperforming groups, and create a color-coded performance bar chart.

**Step 7: Monitoring Dashboard**
Build a 4-panel dashboard covering KPI status vs. targets, incident distribution, response time SLAs, and monitoring coverage by dimension.

**Step 8: Executive Dashboard**
Assign readiness percentages to 6 compliance areas based on your analysis and create a readiness bar chart with a governance gauge.

### Key Terms

**EU AI Act**: European Union regulation classifying AI systems by risk level (prohibited, high-risk, limited, minimal) with compliance requirements for each tier.

**NIST AI Risk Management Framework (AI RMF)**: A framework with four functions — Govern, Map, Measure, Manage — for identifying, assessing, and mitigating AI risks using a 5×5 likelihood × impact scoring matrix.

**Model Card**: A documentation framework (Mitchell et al., 2019) for reporting model details, intended use, disaggregated performance metrics, fairness considerations, and limitations.

**Third-Party AI Vendor Governance**: The process of evaluating external AI model providers across transparency, security, governance, contractual protections, and ethics.

**Post-Deployment Monitoring**: Ongoing measurement of AI system performance using KPIs, incident taxonomies, severity classifications, and escalation procedures.

---

## Exercise Instructions

### Your Task

Build a comprehensive AI governance assessment for ClinicalCompanion by completing two deliverable files: a Jupyter Notebook with code-driven analysis and visualizations, and an Excel workbook with written governance assessments across six areas.

### Requirements

Your implementation must:
1. Complete all 🔧 TODO cells in `governance_assessment.ipynb` so the notebook runs end-to-end
2. Generate 6 PNG visualizations saved to the `results/` folder
3. Fill in all yellow cells across 6 sheets in `governance_workbook.xlsx` (no remaining `[prompt]` text)
4. Use data from the provided CSV and JSON files in the `data/` directory (do not modify these files)

### Repository Structure

```
starter/
├── README.md                      ← You are here
├── data/                          ← Input datasets (DO NOT MODIFY)
│   ├── system_spec.json           ← ClinicalCompanion system specification
│   ├── training_data_summary.csv  ← Training data sources and volumes
│   ├── performance_metrics.csv    ← Model performance by subgroup (20 metrics)
│   ├── risk_register.csv          ← 8 risks scored via NIST AI RMF
│   ├── vendor_assessment.csv      ← 27 vendor evaluation criteria with scores
│   ├── vendor_profile.json        ← FoundationHealth Inc. company profile
│   ├── eu_ai_act_requirements.csv ← 16 EU AI Act compliance requirements
│   ├── monitoring_kpis.csv        ← 16 monitoring KPI definitions
│   ├── incident_types.csv         ← 10 AI-specific incident types
│   └── severity_levels.csv        ← S1-S4 severity classifications
├── results/                       ← Your outputs go here (6 PNG visualizations)
├── governance_assessment.ipynb    ← YOUR CODE DELIVERABLE (complete the TODOs)
└── governance_workbook.xlsx       ← YOUR WRITTEN DELIVERABLE (fill yellow cells)
```

### Starter Code

The notebook has 8 steps (Steps 0–8) with provided scaffolding — imports, data loading, axis formatting, and save commands are already in place. You complete the TODO sections. Here is a representative example from Step 1a:

```python
# Step 1a: Load and display system overview

# Load the system specification JSON
with open(DATA_DIR / 'system_spec.json') as f:
    spec = json.load(f)

# Print a formatted header
print("=" * 70)
print("CLINICALCOMPANION v1.0 — SYSTEM OVERVIEW")
print("=" * 70)

# 🔧 TODO: Create a dictionary of key system facts by accessing nested keys in `spec`.
# Extract at minimum: System name+version, Type, Developer, Foundation Model name,
# Parameters, Access Method, Cloud Region, Encryption, Target Launch Date.
overview = {
    # Add your key-value pairs here
}

# 🔧 TODO: Loop through the overview dict and print each fact in a formatted way.
```

The workbook (`governance_workbook.xlsx`) has two types of content:
- **Grey sections** — pre-filled reference data from the CSV/JSON files. Use as context. Do not modify.
- **Yellow cells** — your work. Replace the prompts with your own governance analysis.

| Sheet | Pre-filled for You | Your Work (yellow cells) |
|-------|-------------------|--------------------------|
| EU AI Act Classification | Article numbers, requirement names, descriptions | Classification reasoning, compliance status, severity ratings, remediation plans |
| Risk Register | Risk IDs, categories, descriptions, likelihood, impact, risk scores | Priority determination, mitigation strategies, residual risk estimates |
| Vendor Evaluation | Vendor profile, category names, max scores | Category scores, risk level ratings, recommendation narrative |
| Model Card | Model details, intended use, training data, raw performance metrics | Fairness analysis, ethical considerations, limitations, recommendations |
| Monitoring & Incidents | All KPIs, incident types, severity levels | Escalation procedures, regulatory notification plan, monitoring gap analysis |
| Executive Summary | Nothing — this is entirely your synthesis | Classification, risks, readiness, vendor, performance, board recommendation |

### Expected Behavior

When all notebook cells run successfully, 6 PNG files appear in `results/`:

```bash
ls results/
```

```
executive_dashboard.png
model_card_performance.png
monitoring_dashboard.png
risk_heatmap.png
risk_mitigation_comparison.png
vendor_evaluation_chart.png
```

The notebook prints formatted summaries at each step (system overview, compliance gaps, risk statistics, vendor scores, subgroup performance, KPI summaries). The workbook contains your written governance analysis across all 6 sheets with no remaining placeholder text.

### Implementation Hints

1. Before coding each step, load the relevant data file and run `.head()`, `.columns`, and `.shape` to understand the column names and structure
2. The JSON files have nested keys — explore with `spec.keys()` and `spec['system'].keys()` before trying to access specific values
3. For the risk heatmap, plot risks at `(likelihood-1, impact-1)` positions (0-indexed) and use `imshow()` with `origin='lower'` for the background gradient
4. For the vendor radar chart, close the polygon by appending the first value and angle to the end of their respective lists
5. Use your notebook analysis numbers directly in the workbook — governance analysts cite specific data points, not vague observations

---

## Important Details

### Common Misconceptions

**Misconception**: "ClinicalCompanion is a minimal-risk system because physicians make the final decision"
**Reality**: The EU AI Act classifies based on the system's domain and function, not the presence of human oversight. A clinical decision support system falls under medical device regulation (MDR 2017/745), making it high-risk under Article 6(1) regardless of the physician-in-the-loop design.

**Misconception**: "The workbook is just restating numbers from the notebook"
**Reality**: The notebook produces quantitative analysis; the workbook requires qualitative governance judgment. A governance analyst interprets what a 71.2% accuracy rate on rare diseases *means* for patient safety and regulatory compliance, not just reports the number.

### Best Practices

1. **Cite specific numbers in governance writing**: Instead of "the model has performance gaps," write "Top-3 accuracy for Rare Diseases (71.2%) is 20.5 percentage points below the 90% target, creating an Article 10 compliance gap requiring additional training data from underrepresented populations."
2. **Use consistent data across deliverables**: Your notebook analysis and workbook should reference the same values — if your notebook calculates an overall vendor score of 68%, the workbook vendor evaluation should cite that same 68%.

### Common Errors

**Error**: Risk heatmap plots risks at wrong positions
- **Cause**: Using raw likelihood/impact values (1-5) instead of 0-indexed positions (0-4) for the scatter plot
- **Solution**: Plot each risk at `(likelihood - 1, impact - 1)` to align with the `imshow()` grid

**Error**: Radar chart polygon is open (gap between last and first point)
- **Cause**: Not closing the polygon by repeating the first data point
- **Solution**: Append `values[0]` to the values list and `angles[0]` to the angles list before plotting

**Error**: Workbook still contains `[prompt]` placeholder text
- **Cause**: Skipping yellow cells or not noticing all prompts across 6 sheets
- **Solution**: Search for `[prompt]` or `[` across all sheets before submitting

---

## Submission Checklist

Before submitting, verify:

- [ ] `governance_assessment.ipynb` — All TODO cells completed and runnable
- [ ] `governance_workbook.xlsx` — All 6 sheets filled in (no remaining `[prompt]` text)
- [ ] `results/` folder contains 6 PNG files:
  - `risk_heatmap.png`
  - `risk_mitigation_comparison.png`
  - `vendor_evaluation_chart.png`
  - `model_card_performance.png`
  - `monitoring_dashboard.png`
  - `executive_dashboard.png`
