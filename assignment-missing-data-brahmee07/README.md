# Missing Data and Merging Assignment

You’re working with car listing data from five Upper Midwest states. The goal is to merge several datasets and investigate patterns of missing data.

## Files
- `missing-data-assignment.zip` – main listings data (TSV inside)  
- `car-buying-location-summary.csv` – average price by location  
- `SQINC1.xlsx` – quarterly per-capita income by state  

## Tasks

### 1. Merge the data
1. Read all three datasets.  
2. From the income file, keep rows just the rows with per capita personal income and
   just the 50 states.  
3. Rename `GeoName` → `state` and compute the median across the quarterly columns (`2015:Q1`–`2025:Q2`).  
4. Merge:
   - `main` + `location` on `location`  
   - result + `income` on `state`  
5. Verify that the merges worked (row counts, expected new columns).

### 2. Explore missingness
Investigate the following columns:
`price`, `odometer`, `title`, `model`, `year`.

For each:
- Create an indicator (`isna()` → 0/1).  
- Compare missing vs. non-missing groups using covariates. 
- Visualize or summarize any patterns.  
- Briefly describe whether the missingness seems MCAR, MAR, or MNAR — and why.

### 3. Impute Missing Data

For any variables you believe are **MCAR**, perform imputation.  
Use something more granular than a simple mean or median — for example, impute using the mean value **by state and model**.

For variables you believe are **MAR**, use an imputation method that you think will fill in the data **without introducing bias** (i.e., group-specific imputation).

Leave any **MNAR** variables **unimputed**, but explain briefly *why* imputing them would be problematic.
