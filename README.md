# Beyond Bias Detection: AI Recruitment Fairness & Governance Audit

## Overview

An independent AI governance research project investigating fairness, accountability and responsible deployment in AI-driven recruitment systems.

The project uses a controlled synthetic recruitment dataset to evaluate how deliberately introduced historical decision bias can affect AI-assisted candidate selection.

## Research Objectives

- Evaluate demographic differences in recruitment selection outcomes.
- Investigate intersectional fairness across gender and race groups.
- Compare baseline, biased and mitigated model decisions.
- Examine limitations of statistical fairness metrics.
- Analyse regulatory approaches and governance safeguards.

## Methodology

**Dataset:** 5,000 synthetically generated applicant records.

**Tools:** Python, Pandas, NumPy, Scikit-learn, Fairlearn, Matplotlib and Seaborn.

**Experimental scenarios:**
1. Baseline recruitment model.
2. Model trained on deliberately biased historical decisions.
3. Fairness-mitigated model using Fairlearn's ExponentiatedGradient.

## Preliminary Results

| Metric | Baseline | Biased | Mitigated |
|---|---:|---:|---:|
| Accuracy | 83.30% | 72.30% | 73.50% |
| Recall | 71.84% | 53.29% | 60.20% |
| F1 Score | 83.61% | 69.53% | 72.93% |
| Gender DP Difference | 0.0214 | 0.2227 | 0.0269 |

The experiment demonstrates that the deliberately introduced decision bias increases the gender selection-rate disparity, while the mitigation approach reduces the measured demographic parity difference.

## Governance Research

The policy analysis examines:

- NYC Local Law 144 and automated employment decision tools.
- NIST AI Risk Management Framework.
- Accountability and human oversight.
- Transparency and continuous fairness monitoring.

## Limitations

- The dataset is synthetic and does not represent actual recruitment outcomes.
- The experiment uses a simplified recruitment decision process.
- Statistical parity does not establish overall fairness.
- Fairness mitigation can introduce trade-offs in predictive performance and other fairness measures.
- Findings should not be interpreted as evidence of discrimination by any real organisation.

## Research Purpose

This project is an independent educational research exercise exploring the intersection of AI evaluation, algorithmic fairness and public policy.

All experimental results are based on simulated data.

## Author

Independent AI Governance Research Project | 2026
