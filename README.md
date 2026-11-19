# Beyond Bias Detection: AI Recruitment Fairness & Governance Audit

An independent AI governance research project examining fairness, accountability, and responsible deployment in AI-driven recruitment systems.

This project investigates how historical bias in recruitment decisions can influence AI-assisted candidate selection, evaluates fairness across demographic groups, and explores governance approaches for mitigating algorithmic risks.

## 1. Problem Statement

AI-driven recruitment systems can reproduce or amplify patterns of historical bias present in their training data.

A model may demonstrate reasonable predictive performance while producing unequal outcomes across demographic groups.

This project explores an important governance question:

**Can an AI recruitment system be considered responsible if its overall performance is acceptable but its selection outcomes differ significantly across demographic groups?**

## 2. Research Objectives

- Evaluate demographic differences in recruitment selection outcomes.
- Investigate intersectional fairness across gender and race.
- Compare baseline, biased, and fairness-mitigated model decisions.
- Examine trade-offs between predictive performance and fairness.
- Map identified governance risks to the NIST AI Risk Management Framework.
- Analyse regulatory approaches to automated employment decision tools.

## 3. Dataset

The experiment uses a synthetically generated dataset containing **5,000 applicant records**.

The dataset includes simulated applicant characteristics such as:

- Gender and race groups
- Education and experience
- Skills and assessment scores
- Recruitment qualification labels
- Simulated recruitment decisions

**Important:** This is synthetic data created for educational research. It does not represent actual applicants, employers, or real-world hiring outcomes.

## 4. Methodology

The experiment evaluates three recruitment decision scenarios:

### Scenario A — Baseline Model
A baseline recruitment model trained using simulated qualification decisions.

### Scenario B — Biased Historical Decisions
A model trained using deliberately biased simulated recruitment decisions to examine how historical decision patterns can affect outcomes.

### Scenario C — Fairness Mitigation
A fairness-mitigation approach using Fairlearn's ExponentiatedGradient with a DemographicParity constraint.

The three scenarios are compared using predictive performance and demographic fairness metrics.

## 5. Evaluation Metrics

| Metric | Purpose |
|---|---|
| Accuracy | Overall prediction correctness |
| Precision | Proportion of positive predictions that are correct |
| Recall | Proportion of qualified applicants correctly identified |
| F1 Score | Balance between precision and recall |
| Demographic Parity Difference | Difference in selection rates between demographic groups |
| True Positive Rate | Proportion of qualified applicants correctly selected |
| False Negative Rate | Proportion of qualified applicants incorrectly rejected |

## 6. Preliminary Experimental Results

| Metric | Baseline | Biased | Mitigated |
|---|---:|---:|---:|
| Accuracy | 83.30% | 72.30% | 73.50% |
| Precision | 100.00% | 100.00% | 92.49% |
| Recall | 71.84% | 53.29% | 60.20% |
| F1 Score | 83.61% | 69.53% | 72.93% |
| Gender DP Difference | 0.0214 | 0.2227 | 0.0269 |

### Key Findings

1. The simulated biased model produces a substantially larger gender selection-rate disparity than the baseline model.
2. Fairness mitigation reduces the measured demographic parity difference from 0.2227 to 0.0269.
3. Mitigation also changes predictive performance, illustrating the trade-offs involved in fairness interventions.
4. Reducing demographic parity differences does not automatically eliminate disparities in other fairness measures.

These results are specific to the synthetic experimental setup and should not be interpreted as evidence about any real recruitment organisation.

## 7. Governance and Policy Analysis

The project explores two governance frameworks:

**NIST AI Risk Management Framework (AI RMF)**

The research maps recruitment AI risks to the four core functions:

- GOVERN — Establish accountability and organisational oversight.
- MAP — Identify system context, affected stakeholders, and potential risks.
- MEASURE — Evaluate performance, fairness, and potential harms.
- MANAGE — Prioritise risks and implement mitigation measures.

**NYC Local Law 144**

The project examines the governance implications of automated employment decision tools, including bias audit requirements, transparency, and accountability.

The regulatory analysis is an educational research exercise, not legal advice or a formal compliance assessment.

## 8. Governance Recommendations

Based on the risks explored in this experiment:

- Conduct regular independent bias audits.
- Evaluate intersectional demographic outcomes.
- Maintain meaningful human oversight in hiring decisions.
- Document model limitations and fairness trade-offs.
- Monitor performance and fairness after deployment.
- Establish accountability for recruitment AI decisions.

## 9. Repository Contents

| File | Description |
|---|---|
| `Recruitment_AI_Fairness_Audit.ipynb` | Experiment notebook and analysis |
| `synthetic_recruitment_dataset.csv` | Simulated applicant dataset |
| `gender_fairness_results.csv` | Gender fairness metrics |
| `model_comparison.csv` | Model performance comparison |
| `intersectional_audit.csv` | Intersectional fairness analysis |
| `false_negative_audit.csv` | False negative analysis |
| `nist_governance_mapping.csv` | Mapping to NIST AI RMF |
| `regulatory_governance_analysis.csv` | Regulatory governance analysis |

## 10. Tools and Technologies

- Python
- Pandas and NumPy
- Scikit-learn
- Fairlearn
- Matplotlib and Seaborn
- Google Colab
- NIST AI RMF

## 11. Limitations

- The dataset is synthetic and does not represent real-world hiring data.
- The recruitment decision process is simplified.
- Results depend on the assumptions used to generate the simulated data.
- Demographic parity alone is insufficient to establish overall fairness.
- Fairness interventions can involve trade-offs across different metrics.
- The experiment does not establish legal compliance or prove discrimination by any real organisation.

## 12. Research Purpose

This independent educational research project explores the intersection of algorithmic fairness, AI accountability, responsible AI deployment, and public policy.

Its central objective is to demonstrate how technical evaluation can inform broader AI governance decisions.

**Author:** Shreyasi Doshi  
**Project Year:** 2026
