P1 · Credit-risk model validation (Responsible AI)

Status: In progress · Author: Andrii Zhehestovskyi · Portfolio

Purpose

An independent evaluation of a credit-scoring model on a public dataset, written the way a model validator at a UK lender would approach it. The work is aligned with PRA SS1/23 principles on model development and independent validation.

Scope
Model under review: a gradient-boosted classifier trained on a public credit dataset (e.g. UCI German Credit or Home Credit).
Validation areas: performance, calibration, stability, fairness across groups, explainability.
Regulatory context: PRA SS1/23; EU AI Act Annex III (creditworthiness assessment of natural persons as high-risk); UK GDPR data protection by design and by default.
Acceptance criteria
ID	Criterion	Evidence
AC1	Discrimination reported (AUC, KS) with confidence intervals	Notebook + report table
AC2	Calibration assessed (reliability curve, Brier score)	Plot + metric
AC3	Stability tested across time or resamples (PSI)	Table of PSI values
AC4	Group fairness metrics computed with Fairlearn (demographic parity difference, equalised odds difference)	Fairness table per group
AC5	Global and local explanations with SHAP and LIME, with agreement between them discussed	Plots + commentary
AC6	Limitations and residual risks documented	Report section
Plan
[ ] Specification and acceptance criteria (this README)
[ ] Data preparation and baseline model
[ ] Performance and calibration tests
[ ] Stability tests
[ ] Fairness assessment
[ ] SHAP and LIME explanations
[ ] Validation report with limitations
Tools

Python, pandas, scikit-learn, Fairlearn, SHAP, LIME, Jupyter, Git.

Repository structure (planned)
data/        # download script only, no raw personal data committed
notebooks/   # exploratory and validation notebooks
src/         # reusable test functions
reports/     # validation report (Markdown/PDF)
