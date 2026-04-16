# Goodreads-Book-Analysis
Exploratory analysis of 52,448 Goodreads books — ratings, publishers &amp; publication trends | ALY 6000
**Course:** ALY 6000 | **Date:** March 8, 2026  
**Author:** Fatemeh Shahabdehkordi  
**Tools:** R, RStudio, tidyverse, ggplot2, janitor, lubridate

---

## Project Overview

An exploratory data analysis of 52,448 books from the Goodreads 
platform (sourced via Kaggle). After thorough data cleaning — filtering 
to books published 1990–2020, removing books over 700 pages, 
standardizing column names, and handling missing values — the final 
dataset consisted of 8,490 books across 17 variables.

---

## Key Statistical Findings

### Book Ratings
| Statistic | Value |
|-----------|-------|
| Mean | 4.02 |
| Median | 4.03 |
| Min | 1.99 |
| Max | 5.00 |
| Q1 | 3.86 |
| Q3 | 4.19 |

### Page Counts
| Statistic | Value |
|-----------|-------|
| Mean | 329.7 pages |
| Median | 328 pages |
| Q1 | 240 pages |
| Q3 | 405 pages |

- **Liked Percent:** Mean 92.87% · Median 94%
- **Publication Year:** Range 1990–2020 · Median year 2007

---

## Visualizations Produced

**Figure 1 — Histogram of Book Ratings**  
Most books rated between 3.75–4.50. Peak bin (4.00–4.25) 
contains ~3,200 books. Distribution is unimodal and slightly 
left-skewed — Goodreads users are generous raters.

**Figure 2 — Box Plot of Page Counts**  
Median 328 pages · IQR of 165 pages (240–405). Symmetric 
distribution with outlier cluster near 650–699 pages.

**Figure 3 — Books Published Per Year (1990–2020)**  
Clear growth from ~125 books in 1990 to a peak of ~625 in 2011. 
Sharp post-2011 decline is a data artifact — newer books have had 
less time to accumulate ratings.

**Figure 4 — Pareto Chart by Publisher**  
Random House (~1,150 books) and Harper Collins (~750 books) 
dominate. Cumulative ogive confirms heavy industry concentration 
in the top two publishers.

**Figure 5 — Top 10 Publishers by Book Count**  
Random House leads with ~1,175 books. Steep drop-off after 
the top two publishers reinforces publishing industry concentration.

**Figure 6 — Average Rating Per Year (1990–2020)**  
Ratings stable near 4.00–4.05 from 1990–2014. Notable upward 
shift from 2015 onward, peaking at 4.19 in 2017 — likely 
reflects selection bias toward popular newer titles.

---

## R Packages Used

- `tidyverse` — data manipulation and pipeline operations
- `ggplot2` — all visualizations (histogram, boxplot, 
  line plots, bar chart, Pareto chart)
- `janitor` — column name standardization with `clean_names()`
- `lubridate` — date format conversion and year extraction

---

## Files in this Repository

| File | Description |
|------|-------------|
| `Shahabdehkordi_Project3.Rproj` | RStudio project file |
| `Shahabdehkordi_Project3_Report.pdf` | Full written report with all figures |

---

## Key Conclusions

- Goodreads users rate books positively on average (4.02/5.00) 
  likely due to self-selection — readers review books they 
  already expected to enjoy
- Publishing activity peaked around 2010–2012, coinciding with 
  Goodreads' rapid platform growth
- Random House and Harper Collins dominate the publishing 
  landscape, accounting for a disproportionate share of titles
- The post-2012 decline in book counts is a **data artifact**, 
  not a true publishing trend

---

## What I Learned

This project developed my ability to clean and reshape a large, 
messy real-world dataset before analysis. Working with 52,448 
raw records down to 8,490 clean observations taught me how 
critical data preparation is before drawing any conclusions. 
Building a Pareto chart from scratch in ggplot2 — combining 
bars with a cumulative ogive line — was a key technical 
skill gained in this project.
