# Week 8 Required Assignment: Bootstrapping Credit Union Survey

This week you’ll work with real survey data from a credit union in Washington State. As we discussed in class, we're interested in learning about the political attitudes of the credit union members and about their support for education. 

You’ll use this dataset to practice *bootstrapping* (with a smidge of permutation testing).

**WARNING**: In this assignment, I'm not giving you starter code in a notebook. I expect you to create a well-formed notebook using both code and markdown cells. Add some commentary to your code, make it look somewhat nice, and pay attention to formatting. 

Ultimately in life you're going to want to be able to generate nice-looking code from scratch. That starts now!

---

## Instructions & Policies

- **AI use:** You may use AI for help with syntax or debugging, but do not ask AI to write complete solutions. Avoid copying-and-pasting from AI. 
  The goal is to practice reasoning about sampling, uncertainty, and resampling.
- **Output:** Your notebook must run top-to-bottom without errors.  
  Before submitting, “Restart & Clear Outputs,” then re-run everything sequentially.

---

## The Data

The data you’ll receive contains **2,421 survey respondents** and includes variables such as:

- **Demographics:** `age`, `gender`, `region`, `public.sector`  
- **Institution Relationship:** `engagement`, `account.age`, `channel`  
- **Values:** `harm`, `fair`, `in.group`, `authority`, `purity`  
- **Institutional Priorities:** `localism`, `sustainability`  
- **Outcomes:**  
  - `main.focal.value` — The respondent’s chosen top cause or area of concern.  
  - `support.of.focal.value` — Level of support for that focal cause.

Each row represents **one member**.

---

## Learning Goals

By the end of this assignment, you should be able to:

1. Compute a composite measure from raw items.  
2. Use **bootstrapping** to estimate uncertainty in summary statistics.  
3. Use a **permutation test** to assess group differences.

---

## Your Tasks

### 1. Calculate the *Progressivism* Measure
The original survey included the *Moral Foundations Questionnaire* and a summary measure of **progressivism**.  
You’ll recreate it from the five foundation scores:

`harm`, `fair`, `in.group`, `authority`, `purity`

> Hint: Your reading tells you about the `progressivism` calculation. It's the average of the `harm` and `fair` columns minus the average of the other three Moral Foundations Theory dimensions (`purity`, `in.group`, `authority`).

Store your computed score in a new column:  
`survey['progressivism'] = ...`

---

### 2. Bootstrap the Mean Progressivism by Region
Use **bootstrapping** to estimate the mean and 95% confidence interval of `progressivism` for each `region`.

- Draw at least 1,000 bootstrap samples.  
- Plot a histogram of bootstrap means for one region.  
- Create a summary table or chart showing each region’s estimated mean and CI. Use `quantile` on your bootstrap replicates to calculate a 95% confidence interval.

---

### 3. Bootstrap the Fraction Supporting Education
Estimate the **fraction of members** in each region whose `main.focal.value == "Education"`.  
Use bootstrapping to generate a confidence interval for this proportion.

> Example statistic (with made up numbers):  
> *In W WA Metro, 10% of members support education as their focal value, with a 95% confidence interval of 8% to 25%.*

---

### 4. Permutation Test: Metro vs. Non-Metro
Group the regions into two groups:  
- **Group 1:** W WA Metro and Thurston  
- **Group 2:** W WA Non-metro, E WA Non-metro, and E WA Metro

Perform a **permutation test** to determine whether the proportion supporting Education differs between these two groups.

Fill in a table like this one from the Permutation Test assignment: 

| Element from OOT | In your example |
|:--|:--|
| **1. Data** | |
| **2. Test statistic** | |
| **3. Observed value or effect** | |
| **4. Null hypothesis** | |
| **5. How you simulate data under the null** | |
| **6. Description of the reference distribution** | |
| **7. p-value from comparing observed to simulated** | |


---

### 5. Reflect
Write a short paragraph summarizing what you learned:  

- How long did the assignment take you?
- What was the hardest part of doing it?
- Do you have any unresolved questions?

---

## Deliverables

- A Jupyter notebook that:  
  - Runs top-to-bottom without errors  
  - Calculates all requested quantities  
  - Includes clear comments and visualizations  
  - Concludes with a short written reflection

## Feedback 

Great work on this assignment. 

On your final point, I think it'd be worthwhile to ask about this in class, but I'll also give you a response here. You write: 
> The assignment did not take long once I got started, although I spent some time revising bootstrapping beforehand so it felt a bit longer. I started around 4 PM and finished around 8 PM. The hardest part was probably figuring out how to loop through regions and get the progressivism values correctly. It was not conceptually difficult, but I got a bit stuck on the syntax. I am still a little unsure about the bigger purpose of bootstrapping. I understand how it gives a confidence interval, but I am thinking about why we would do it in real life. I am assuming it is to understand the uncertainty in our estimates and to see how reliable our sample statistics are, but I am still a little unsure about its practical use case. I am not confused about how bootstrapping is done, just why it is applied in real-world scenarios.
>

You’re exactly right: bootstrapping helps us quantify uncertainty, especially when we don’t have strong theoretical formulas for a statistic’s sampling distribution (or when the data aren’t cleanly normal). In practice, we use it all the time to gauge how stable an estimate is. Sometimes this is for a hypothesis (e.g., if this regression coefficient is zero then a given variable may not matter much in a model, which can be important). Other times it's just to know the uncertainty. If I forecast revenue is going to be $50M next year, it matters a LOT if the standard error is $1M vs $20M. The bootstrap tells us how much to "trust" our statistics.
