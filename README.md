# Infrequent Voter Analysis: Predictive Modeling for Strategic Outreach

## Project Overview
This project investigates the demographic and political factors that characterize "infrequent voters" in the United States. Utilizing survey data from a joint **FiveThirtyEight** and **Ipsos** poll of over 5,000 U.S. citizens, I developed a logistic regression model to identify individuals with a low propensity to vote. 

The primary objectives were to:
1.  Analyze the relationship between political party affiliation and voting frequency.
2.  Build a classification system to identify potential infrequent voters from a new mailing list for targeted outreach.

---

## Dataset
The analysis is based on the 2020 Ipsos poll dataset. Key features include:
* **Demographics:** Age (`ppage`), Education (`educ`), Race (`race`), Gender (`gender`), and Household Income (`income_cat`).
* **Political Affiliation:** `Q30` (Republican, Democrat, Independent, Another party, or No preference).
* **Target Variable:** `infrequent_voter` (Binary: 1 for "rarely/never" voters, 0 for "always/sporadic").

---

## Methodology
The analysis was performed in **R** using the **Quarto** publishing system.

### Statistical Approach
* **Logistic Regression:** Used to estimate the log-odds of being an infrequent voter based on socio-economic and political variables.
* **Likelihood Ratio Test:** Conducted to confirm that adding political affiliation significantly improves model fit ($\chi^2 = 142.03, p < 0.001$).
* **Model Interpretation:** Analyzed via Odds Ratios and 95% Confidence Intervals to ensure statistical rigor.

### Evaluation Metrics
* **Classification Threshold:** Set at **0.45** to maximize sensitivity for outreach prioritization.
* **Confusion Matrix:** Used to evaluate true positives vs. false negatives.
* **ROC Curve & AUC:** The model achieved an **AUC of 0.73**, indicating fair-to-good discriminatory power.

---

## Key Findings
* **Political Predictors:** Voters identifying with a major party (Democrat or Republican) are significantly less likely to be infrequent voters compared to those with no affiliation.
* **Socio-Economic Barriers:** Lower education and income levels are strong predictors of non-participation, suggesting a cycle of political alienation.
* **Actionable Results:** The model successfully identified 76 high-priority targets from a 500-person mailing list, providing a data-driven path for personalized communication.

---

## Technical Stack
* **Language:** R
* **Core Libraries:** `tidyverse`, `pROC`, `knitr`
* **Output Format:** Quarto HTML (Self-contained)

## How to Reproduce
1. Clone this repository.
2. Ensure R and the `tidyverse`, `pROC`, and `knitr` packages are installed.
3. Open `CaseStudy3.qmd` in RStudio.
4. Render the document to view the complete statistical report and visualizations.

---

### Author
**Swikriti Dumre** *Undergraduate Student, Smith College* *Double Major: Computer Science & Mathematics-Statistics*
