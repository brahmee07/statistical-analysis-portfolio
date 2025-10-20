# Simulating Diagnostic Tests and Bayesian Inference

This exercise explores how **prevalence** affects the **interpretation of test results**, even when tests are very accurate. You'll simulate test outcomes for three hypothetical diseases, each with a different prevalence, and use your results to estimate the probability that someone **actually has the disease given they tested positive**.

This is a practical application of **Bayes' Theorem**, grounded in simulation rather than formulas.

---

## Instructions & Policies
- **AI use:** This assignment has a more liberal AI policy than our last couple of assignments. I'd
like you to come up with the algorithm and instructions on how the simulation and analyses will
work, but you're welcome to use AI to directly write small sections of the code. My recommendation 
is to keep ask the AI to write code in 3-5 line chunks, so you remain in control of the plan.
- **Questions:** Look for cells marked with `Q:`. These contain questions you should answer, typically in Markdown.
- **Output:** Ensure your notebook runs top-to-bottom without errors. Remove stray debug code before submitting. When ready to submit, do a "restart and clear outputs," then run everything through sequentially.

---

### 🧪 The Setup

You’ll simulate a population of 100,000 people being tested for each of the following diseases:

| Disease | Prevalence | Sensitivity | Specificity | Real Life Analog | 
|---------|------------|-------------|-------------|------------------|
| Disease A | 5%        | 99%         | 99%         | Type 2 Diabetes | 
| Disease B | 0.5%      | 99%         | 99%         | Celiac Disease | 
| Disease C | 0.05%     | 99%         | 99%         | ALS is about 0.01% | 

These sensitivity and specificity measures mean that the test is 99% accurate both ways. If someone has the disease, they'll get a positive test result 99% of the time. If they don't, they'll get a true negative 99% of the time.

For each disease, simulate:
1. Who actually has the disease.
2. Who tests positive or negative based on the test characteristics.
3. Among those who test positive, what proportion truly have the disease?

---

### 📌 Your Tasks

- Simulate the testing process for each disease scenario.
- Estimate `P(Disease | Test Positive)` for each case.
- Reflect on the results. What’s surprising? How does prevalence affect trust in the test?

---

### ✍️ Deliverables

You'll fill in the cells in the notebook. Focus on:
- Running the simulations.
- Clearly labeling your code and results.
- Writing a short reflection at the end.

---

### 🧠 Concepts Reinforced

- Bayesian reasoning in real-world decision making.
- Base rate fallacy and why even accurate tests can mislead.
- The power of simulations when dealing with probabilities.

Have fun!
