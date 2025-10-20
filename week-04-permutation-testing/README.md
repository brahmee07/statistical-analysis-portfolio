# Week 4 Required Assignment: Hypotheses from Raw Listings Data

This week you’ll begin working with **real-world car listings data** pulled through our self-serve system.

You can access the self-serve form [here](https://docs.google.com/forms/d/e/1FAIpQLSdQQMShcp2OaFkdOclqkJN5hmWjWsowEte62WrglmW1S61Vkw/viewform?usp=header).

Note, this assignment is required for everyone, regardless of grade. The first draft is due before next week's class.

---

## Instructions & Policies
- **AI use:** You may use AI to ask questions if you are stuck or need clarification. However, do not use AI code-completion or copy/paste code from AI. We're still working on gaining fluency in pandas.
- **Output:** Ensure your notebook runs top-to-bottom without errors. Remove stray debug code before submitting. When ready to submit, do a "restart and clear outputs," then run everything through sequentially.

---

## The Setup

- Data is available via a [**Google Form**](https://docs.google.com/forms/d/e/1FAIpQLSdQQMShcp2OaFkdOclqkJN5hmWjWsowEte62WrglmW1S61Vkw/viewform?usp=header).
- After submitting the form, you’ll receive your dataset by email. Check your spam folder if it doesn’t show up!
- Each pull is limited to **100,000 rows**. If you’re unsure your pull worked, do a quick test run first.

You can filter the raw listings data by:
- **Time**  
- **Make/Model**  
- **State**  

---

## Important Note on Hypotheses

We are **not yet in position** to directly compare *entire populations* (e.g., *“all F-150s in Wisconsin vs. all F-150s in Wyoming”*).  
Instead, you’ll frame hypotheses about **samples** from your data.

Example:  
*A sample of 30 F-150s from Wisconsin is cheaper than the distribution of samples of 30 from Wyoming.*

---

## Your Tasks

1. **Pull one or more datasets** using the Google Form.  
   - Verify you receive the file by email.  
   - Import it into your notebook.

2. **Explore the dataset**:  
   - Basic summaries (`.describe()`, histograms, averages, etc.).  
   - Identify any quirks in the data (missing values, odd entries, etc.).

3. **Clean the dataset**:  
   - Turn this data set into a clean data frame that supports the analysis you'd like to do. 
   - This may involve all the tricks we've done before:
      - Dropping certain observations
      - Doing missing value imputation
      - Truncating data to a particular range


3. **Formulate a hypothesis** related to **samples** from your group’s dataset.  
   - Phrase these clearly in writing.  
   - The hypothesis should state both a statistic and a data generating process that will give you a reference distribution. 
   - Examples:  
     - *A sample of 50 Camrys from 2015–2020 in California will have higher mileage than a sample of 50 Camrys from Texas.*  
     - *In samples of 20 trucks from the Midwest, the average asking price exceeds $20,000.*

4. **Test your hypotheses informally** using the tools you know so far (sampling, grouping, simple comparisons).  
   - Formal inference will come later.  
   - For now, focus on setting up the problem and seeing what the data suggests.

5. **Reflect**:  
   - What did you conclude?
   - Go back and run all of your code without any of the cleaning (or with minimal cleaning). Do the conclusions change at all?  
   - How did the sample framing change the way you thought about your comparisons?

---

## Deliverables

- A Jupyter notebook that:  
  - Runs top-to-bottom without errors.  
  - Contains your data pull and exploratory summaries.  
  - Clearly labels your hypotheses and results.  
  - Includes a short written reflection.

## Feedback 

Nice job on the exploration and cleaning. 

I really like this hypothesis.

Your analysis is missing one thing, which is some comparison that takes into account potential variability in your samples. It's going to be too much work to do this for all the pairwise comparisons, so I recommend doing high-effiency vehicles compared to one of your other categories. Maybe Trucks, since that difference is smaller.

You can follow the structure we've done in class. 

1. Create an empty list to hold the differences in means.
2. Take samples from each of your groups.
3. Calculate the average odometer per group.
4. Subtract those and store the differences.
5. Then plot the values, paying attention to the zero value, since that's the value with no difference in the means.
6. Calculate the fraction of replicates that are more extreme than the value you found. 
