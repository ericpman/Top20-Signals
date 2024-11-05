# Top20-Signals

This project is a Google Sheets program designed to analyze quantitative probability data from several signals and technical indicators. It then selects stocks from the S&P 500 to form smaller, high-probability baskets of long and short stocks. The objective is to help traders build informed, data-driven portfolios with an emphasis on expected average performance, while balancing exposure across sectors.

**[Link to Google Sheet Project](https://docs.google.com/spreadsheets/d/1eEjZFbyJzosGwO3n9-C-3kTbgjESUbzgzrZwLdcv078/edit?usp=sharing)**

## Project Overview

The program consists of multiple steps to filter, sort, and refine stocks based on signals and technical data, yielding two sorted lists for potential longs and shorts. Here’s an outline of each step:

### Step 1: Import and Preprocess Data

In the first sheet, we begin by copying quantitative data into columns A-J from a larger database. This includes:
- **Stock Symbol** (column A)
- **Signal Value** (B)
- **Bin Values** (C)
- **Odds of Performance** (E)
- **Average Performance** (F)
- **Maximum Favorable and Adverse Excursions** (G-H)
- **Sector and Industry** (I-J)

![Screenshot of Initial Data Input](https://github.com/user-attachments/assets/6b0502a2-6bc5-4348-894e-7ebab0bf154f)

For program purposes, the columns of interest are **Symbol**, **Signal Value**, **Odds**, **Average Performance**, **Sector**, and **Industry**.

### Step 2: Signal Filtering

Column K automatically processes each stock's average performance based on set criteria:
- If the **Average Performance** is positive and **Odds** exceed 50, or if **Average Performance** is negative and **Odds** are below 50, the stock's performance value is added to column K.
- If not, column K displays zero.

To start data processing, enter "GO" in cell L1, which minimizes lag by preventing the program from running prematurely.

### Step 3: Generate Long and Short Candidates

Upon activation:
- **Column M** lists the top 20 stocks for potential longs (positive performance).
- **Column O** lists the top 20 stocks for potential shorts (negative performance).

This provides two initial lists for further filtering and sorting.

### Step 4: Filter and Sort Stocks

The next section refines the long and short candidates by filtering for stocks that are exclusive to each list:

![Screenshot of Long and Short Sorting](https://github.com/user-attachments/assets/65c65266-6342-42c8-9273-9e7ce957af80)

- **Column Q** (Positive Sorted) contains stocks from the longs list (column M) that do not appear in the shorts list (column O).
- **Column T** (Negative Sorted) includes stocks in the shorts list that do not appear in the longs.

Adjusted performance values are calculated in columns **S** (for longs) and **V** (for shorts), adding weight to stocks that appear multiple times within the lists. Columns **W-Z** show each stock symbol with an adjusted average, determining the top-performing stocks.

### Step 5: Final Ranking and Sector Analysis

With the refined lists in place, columns **AA** and **AB** display the final long and short candidates sorted by their probability of expected performance. This ranking hierarchy allows us to prioritize the most statistically favorable stocks.

In the next sheet tab, stocks are matched with their **Sector** and **Industry**:

![Screenshot of Sector and Industry Sorting](https://github.com/user-attachments/assets/d756d7ab-6b90-4702-812f-70f5e2282c1b)

This view enables traders to balance exposure by sector and avoid overconcentration. In **Columns G-I** (for longs) and **Columns J-L** (for shorts), stocks are categorized by sector and industry while maintaining their performance-based order within those respective sectors.

![Screenshot of Final Sector View](https://github.com/user-attachments/assets/c1278414-43df-4834-82d1-5613332f40e3)

---

## Conclusion

This Google Sheets program streamlines the process of selecting top-performing stocks based on signals and probability from our Statistical Odds database. By categorizing stocks into long and short lists and refining them through performance and sector balancing, it offers traders a systematic, data-backed approach to portfolio construction.

---
