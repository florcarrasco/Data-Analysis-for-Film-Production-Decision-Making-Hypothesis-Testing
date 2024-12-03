# Movie Production Company - Investment Analysis

## Overview

This repository contains an analysis of movie metadata to provide actionable insights for future investments in the production company. The goal is to identify key factors that contribute to profitable outcomes, with a focus on movie directors and their relationship with profitability. The analysis was based on a dataset of movie metadata, specifically focusing on the relationship between the budget, profits, and other features such as director name and genre.

---

## Key Objectives

1. **Data Cleaning and Preparation**:
   - Removed rows with missing values.
   - Dropped duplicates to ensure the dataset was clean.
   - Split and exploded the 'genre' column, as it contained multiple values per row.
   
2. **Exploratory Data Analysis (EDA)**:
   - Conducted a correlation analysis to understand relationships between numerical features.
   - Explored the distribution of features to find patterns between high-profit and low-profit movies.
   
3. **Statistical Testing**:
   - Performed Kolmogorov-Smirnov, D'Agostino's Ksquared, and Lilliefors tests to determine the distribution of features.
   - Applied **bootstrapping** to test hypotheses about the relationship between movie features (especially director) and profitability.

4. **Actionable Insights**:
   - Determined that movie directors significantly impact profitability, with specific directors showing higher average profits.
   - Generated a top 20 list of directors whose films, with a budget of £1.5 million, are more likely to yield higher profits.

---

## Features

- **Data Cleaning**: Missing values and duplicates are removed, ensuring a clean dataset for analysis.
- **Genre Handling**: The 'genre' column is split into multiple entries to analyze each genre individually.
- **Profit Calculation**: A new column was added to calculate profit (gross earnings minus budget).
- **Statistical Analysis**:
   - Kolmogorov-Smirnoff and normality tests were performed to assess feature distributions.
   - Bootstrapping was used to evaluate whether the average profitability of high and low profit movies differs.
   
- **Top Directors for Profit**:
   - A list of the top 20 directors is presented, along with their average profits, based on a budget of £1.5M.

---

## Methodology

1. **Data Preparation**: 
   - The data was cleaned by removing missing values and duplicates. 
   - The 'genre' column was split and expanded to better analyze movie features.

2. **Exploratory Data Analysis**:
   - Correlation heatmaps and distribution plots were generated to visually analyze the relationships between features.
   - ECDF (Empirical Cumulative Distribution Functions) were used to measure the dissimilarity between high-profit and low-profit movies.

3. **Statistical Tests**:
   - The Kolmogorov-Smirnoff test was used to determine if the distributions of high-profit and low-profit movies are significantly different.
   - The D'Agostino's Ksquared and Lilliefors tests were conducted to confirm that none of the features followed a normal distribution.

4. **Bootstrapping**:
   - Bootstrapping was used to compare the means of high-profit and low-profit datasets for each feature.
   - The director was identified as a significant feature impacting profitability.

---

## Results

- **Top Directors**:
   - The director is a significant factor in determining profitability. Using a budget of £1.5M, directors in the top 20 are more likely to generate higher profits.
   
- **Profitability Insights**:
   - The analysis revealed that, while no feature followed a normal distribution, there are actionable insights that can help predict profitability. Specifically, the choice of director plays a crucial role in the success of a movie.

- **Statistical Significance**:
   - Bootstrapping tests showed that directors with higher social media likes (e.g., Facebook, IMDb) are linked with higher profits. This insight can be used to inform future investment decisions in movie production.

---

## Conclusion

This report provides a data-driven approach to understanding movie profitability and guides future investment strategies for the production company. By identifying key factors like the director’s influence on profitability, the report offers actionable recommendations. The final analysis, which ranks the top 20 directors for profitability based on a £1.5M budget, can serve as a useful resource for making more informed production decisions.

---

## Repository Contents

- **`movie_metadata.csv`**: The dataset containing movie metadata.
- **`data_cleaning.py`**: Script for cleaning and preparing the data.
- **`eda_analysis.py`**: Exploratory data analysis, including correlation and distribution visualizations.
- **`statistical_tests.py`**: Scripts for performing Kolmogorov-Smirnoff, D'Agostino's Ksquared, and Lilliefors tests.
- **`bootstrapping.py`**: Code to perform bootstrapping for hypothesis testing.
- **`top_directors.py`**: Script to generate the top 20 profitable directors based on analysis.

---

## Future Work
1. Incorporate additional features (e.g., marketing budget, actor popularity) to refine profitability predictions.
2. Extend the analysis to include other genres and countries to provide a more comprehensive view of the movie industry.
3. Implement machine learning models to predict profitability based on past performance and other factors.
This repository aims to provide insights for production companies, to make informed decisions on future movie investments.
