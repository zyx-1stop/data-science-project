# data-science-project
# Does Education Still Pay Off? A Statistical Analysis of Education Level and Income in the United States

## Problem / Research Question

Does highest education level significantly affect annual income in the United States, after controlling for age and gender?

## Dataset Source and Usage Permissions

This project uses two public datasets:

1. **College Scorecard** — U.S. Department of Education
   - Source: https://collegescorecard.ed.gov/data/
   - Public domain, free to use.
   - Used to compare median earnings 10 years after entry across institution degree levels.

2. **IPUMS USA** — University of Minnesota
   - Source: https://usa.ipums.org/usa/
   - Free for academic use with registration.
   - Used to analyze individual income by education level, age, and sex (2017–2024 sample).

No passwords, API keys, personal data, or restricted datasets are included in this repository.

## Methods and Tools

- **Python 3** (pandas, numpy, matplotlib, seaborn, statsmodels, scipy)
- Data cleaning: recoded education levels, log-transformed income, removed missing/invalid values
- Statistical analysis: ANOVA, OLS regression, Pearson correlation
- Visualization: box plots, scatter plots, bar charts

## Key Findings and One Limitation

**Key findings:**
- ANOVA confirms median earnings differ significantly across education levels (F = 598.13, p < 0.001).
- After controlling for age and gender, Bachelor's degree holders earn about 33.25% more than the "Less than HS" reference group (p < 0.001), and Graduate degree holders earn about 65.15% more (p < 0.001).
- Graduation rate and median earnings are positively correlated (Pearson r = 0.5529, p < 0.001).

**One limitation:**
The IPUMS regression R-squared is only 0.158, meaning education, age, and gender together explain about 15.8% of income variance. Other important factors (occupation, industry, region) are not included.

## Instructions for Running the Analysis

1. Clone this repository:
git clone https://github.com/zyx-1stop/data-science-project.git
2. Install dependencies:
pip install -r requirements.txt
3. Open the notebooks:
jupyter notebook Education_Level_and_Income.ipynb
jupyter notebook edu_age_sex_income.ipynb
4. Run all cells in order. Outputs (tables and figures) will be generated.

## Files

- `Education_Level_and_Income.ipynb` — College Scorecard analysis
- `edu_age_sex_income.ipynb` — IPUMS USA analysis
- `requirements.txt` — Python dependencies
- `earnings_by_education.png` — Box plot of earnings by degree level
- `graduation_rate_vs_earnings.png` — Scatter plot of graduation rate vs earnings
