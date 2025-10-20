
# Assignment 2: EDA and Data Visualization

## Overview
In this assignment, you will continue working with the Craigslist car listings dataset. You’ll practice inspecting, cleaning, transforming, and analyzing the data with pandas, and create publication-quality visualizations.

**Estimated time:** 2–3 hours. Please let me know if you spend much longer so I can calibrate future assignments.

---

## Instructions & Policies
- **AI use:** You may use AI to ask questions if you are stuck or need clarification. However, do not use AI code-completion or copy/paste code from AI. The purpose is for you to gain fluency with matplotlib and advanced pandas operations by writing code yourself.
- **Questions:** Look for cells marked with `Q:`. These contain questions you must answer, either in code or Markdown.
- **Figures:** Save all your final plots to a subfolder called `figures/` with descriptive filenames. This folder is included in the repo.
- **Output:** Ensure your notebook runs top-to-bottom without errors. Remove stray debug code before submitting. When ready to submit, do a "restart and clear outputs," then run everything through sequentially.

---

## Assignment Structure

### Part 0: Setup
- Import libraries and load the dataset (`car_listings.csv`).

### Part 1: Data Quality and Missing Data Strategy
- Drop duplicates and standardize string values.
- Remove clearly unrealistic outliers.
- Implement a targeted missing data strategy.

### Part 2: Grouping Operations and Categorical Data
- Convert locations, makes, and models to categorical variables, and compare memory usage before and after.
- Restrict data to two make/model combinations for focused analysis.
- Perform grouped aggregations, including custom functions (e.g., IQR).

### Part 3: Bivariate Relationships & Smoothing
- Explore price vs. mileage using both linear regression and LOWESS smoothing.
- Create scatterplots and interpret the results.

### Part 4: Price Distributions by City
- Use `qcut` to create price deciles and analyze distribution by city for your chosen vehicles.
- Visualize and interpret the results.

### Part 5: Reflection
- Write a brief reflection on your analysis and findings.

---

## Data
Use the provided `car_listings.csv`. Choose two contrasting make/model combinations (e.g., economy car vs. truck/SUV) for focused analysis. Ensure each has at least 250 listings.

---

## Requirements
- Complete all work in the provided Jupyter notebook (`EDA and Data Viz.ipynb`).
- Save all final plots to the `figures/` subfolder with descriptive names.
- Implement all custom functions as specified in the notebook.
- Answer all questions marked with `Q:` in code or Markdown.

---

## Deliverables
- Commit and push your completed notebook with all outputs and the `figures/` directory containing your saved visualizations.