# M6 Assignment: Understanding Permutation Tests

This week’s assignment explores **permutation testing** — a flexible way to test whether an observed difference could just be due to chance.

The assignment has two parts:

**Part 1 – Survey Analysis**  
You’ll use an employee satisfaction survey to test whether satisfaction differs by gender.  
You’ll clean the data, calculate differences in mean satisfaction and proportions, and simulate the world where gender doesn't influence satisfaction.

**Part 2 – Re-doing Your “Only One Test” Analysis**  
You’ll revisit your previous *Only One Test* assignment and replace its sampling framework with a permutation test.  
Your goal is to map each step of your analysis onto the *Only One Test* logic and summarize it in a short Markdown table.

---

### Instructions & Policies
- Complete both parts in this notebook before submitting.  
- You may use AI or online resources for clarification, but all code and written explanations must be your own.  
- Comment your code briefly where needed and keep your Markdown answers concise and professional.  

---

### What You’ll Practice
- Expressing a null hypothesis in code.  
- Using shuffling to simulate data under that null.  
- Connecting simulation results to statistical inference.  
- Translating your own work into the *Only One Test* framework.

---

**Deliverable:** Submit your completed notebook with all code cells executed and reflection questions answered. Before you submit, select "clear all outputs", restart your kernel, and select "run all cells". Save that file, commit, and push it.

## Feedback 

Excellent work on this throughout. One small point: in the second part, the data you have in hand (i.e., the real data) *is* one of the permutations, so it's a best practice to include that in your `differences` data frame. That makes your p-value `1/(1 + n)`. 
