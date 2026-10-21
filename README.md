# Data Science Jobs: Sentiments, Salaries & Direction on Social Media

MSc Information Systems & Digital Innovation coursework (Loughborough University, 2024).

## Overview

An inductive research framework analysing **53,341 data points** across two sources to correlate Reddit sentiment with global data science salary trends. The study examines how public discourse on social media relates to compensation patterns across 152 unique data science job titles.

## Research Pipeline

1. **Data Collection** — Scraped 36,847 Reddit posts using PRAW with keyword-based enumeration across 152 job titles; integrated Kaggle salary data (16,494 rows) covering global data science roles.
2. **Sentiment Analysis** — Applied VADER (Valence Aware Dictionary and sEntiment Reasoner) to classify post titles into positive, negative and neutral sentiment, with compound score thresholds at +/- 0.05.
3. **Topic Modelling** — Implemented Latent Dirichlet Allocation (LDA) with bigram/trigram phrase detection to surface dominant discussion themes within each sentiment class.
4. **Correlation & EDA** — Merged sentiment percentages with salary data by job title, performed StandardScaler normalisation and OneHotEncoding, and computed correlation matrices to identify relationships between sentiment and compensation.
5. **Dashboard** — Built an interactive Dash/Plotly dashboard with grouped bar charts (sentiment by job nature), a correlation heatmap, and a sortable variable-correlation table.

## Key Findings

- Neutral sentiment dominates across all job categories (~69% of posts), with positive sentiment (~25%) outweighing negative (~6%).
- Machine Learning Engineer roles show the strongest positive correlation with salary (r = 0.196) and the highest neutral sentiment.
- Business Intelligence roles exhibit the highest positive sentiment but lower-than-average salaries.
- Data Analyst roles show the strongest negative correlation with salary (r = -0.256).
- LDA topics reveal "hiring" as the most prominent theme across all sentiment classes, with technical skills (Python, SQL, Spark) featuring heavily in positive-sentiment posts.

## Repository Contents

| File | Description |
|---|---|
| `DS_Code.ipynb` | Full Jupyter notebook: data collection, cleaning, VADER sentiment analysis, LDA topic modelling, correlation analysis, EDA visualisations, and Dash dashboard |
| `Report.pdf` | Final written report with methodology, analysis and discussion |
| `salaries.csv` | Kaggle dataset — 16,494 rows of global data science salaries (work year, experience level, job title, salary in USD, company size/location) |
| `reddit_search_results.csv` | Scraped Reddit data — 36,847 posts with keyword (job title), post title, and URL |

## Tech Stack

- **Languages:** Python
- **Data:** Pandas, NumPy, CSV
- **Scraping:** PRAW (Python Reddit API Wrapper)
- **NLP:** VADER Sentiment Analysis, Gensim (LDA), NLTK
- **ML/Stats:** Scikit-learn (StandardScaler, OneHotEncoder)
- **Visualisation:** Matplotlib, Seaborn, Plotly, pyLDAvis
- **Dashboard:** Dash, Dash Bootstrap Components
- **Data Sources:** Reddit API, Kaggle

## Author

**Sarthaj Aram Kuni**
MSc Information Systems & Digital Innovation, Loughborough University
