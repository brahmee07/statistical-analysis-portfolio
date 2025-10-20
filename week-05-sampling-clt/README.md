# Assignment: Sampling Distributions and the Central Limit Theorem

## Overview
This is a choice programming assignment for SEIS-631: Data Preparation and Analysis. You will explore one of the most important concepts in traditional statistics: the Central Limit Theorem (CLT). Through simulation and real data analysis, you'll see how sample means behave, understand sampling distributions, and learn why the CLT is fundamental to statistical inference.

The assignment has two parts: first, you'll simulate rolling dice to build intuition about the CLT in a controlled environment. Second, you'll apply these concepts to a real census of Honda listings from Craigslist.

This assignment is designed to take about 2–3 hours.

## Learning Objectives
By the end of this assignment you should be able to:

- Distinguish between populations and samples
- Understand and calculate standard error using the formula σ/√n
- Explain what a sampling distribution is and how to create one
- Demonstrate the Central Limit Theorem through simulation
- Apply CLT concepts to real-world data with non-normal distributions
- Determine appropriate sample sizes for a desired level of precision
- Visualize and interpret sampling distributions

---

## Data
For Part 2, you'll work with a census of Honda listings from Craigslist. This dataset contains all Honda vehicles listed in California, spanning from July 2023 through the end of data collection (approximately 111,000 listings).

The file is named `california_hondas.txt` and a zip file is on Canvas. This file contains the same columns as the "Only One Test" Assignment car listings dataset. Remember: do not commit large CSV files to Git. The `.gitignore` file is already configured to exclude them.

---

## Instructions
Complete all work in the provided Jupyter Notebook (`Sampling and CLT.ipynb`).

### Part 1: Dice Simulation

Build intuition about sampling distributions using dice rolls where we know the exact population parameters.

**1a. Single Die**
- Simulate rolling a single die 10,000 times
- Calculate and plot the distribution
- Compare empirical statistics to theoretical values

**1b. Sum of Multiple Dice**
- Write a function `roll_dice(n_dice)` that returns the sum of n dice
- Roll different numbers of dice (1, 2, 5, 10, 20, 100) many times each
- Observe how the distribution shape changes

**1c. Sampling Distribution of the Mean**
- Focus on rolling 5 dice
- Take samples of different sizes (n = 5, 10, 30, 100, 500)
- For each sample size, collect 1,000 sample means
- Plot the sampling distributions

**1d. Standard Error**
- Calculate the empirical standard error for each sample size
- Compare to the theoretical standard error: σ/√n
- Create a comparison table and plot

### Part 2: Honda Census

Apply CLT concepts to real, skewed data.

**2a. Understand the Population**
- Load and clean the Honda census data
- Calculate population parameters (mean and standard deviation) for price
- Create a histogram of the price distribution
- Assess the distribution shape

**2b. Sampling Distributions and Standard Error**
- For sample sizes [30, 50, 100, 200, 500], take 1,000 samples each
- Calculate the mean of each sample
- Plot the sampling distributions
- Compare empirical SE to theoretical SE

**2c. Different Variables (Optional Challenge)**
- Repeat the analysis using odometer readings instead of price
- Compare results

---

## Deliverables

Commit and push your completed notebook: `Sampling and CLT.ipynb`

Make sure your notebook:
- Runs top-to-bottom without errors
- Has clear markdown explanations for all questions
- Includes well-labeled visualizations
- Shows your code and outputs
