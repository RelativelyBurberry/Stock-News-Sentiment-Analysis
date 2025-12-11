# 📰 Stock News Sentiment Analysis


## 📌 Overview

This project performs sentiment analysis on financial news headlines for major tech stocks.  
News is scraped from **FinViz**, parsed using **BeautifulSoup**, processed with **Pandas**, analyzed using **NLTK VADER**, and visualized using **Matplotlib**.

The project was developed on **Kaggle Notebook**.

---

## 🛠️ Technologies Used

- **Python 3**
- **Pandas**
- **NumPy**
- **BeautifulSoup (bs4)**
- **urllib.request**
- **NLTK VADER Sentiment Analyzer**
- **Matplotlib**
- **FinViz.com (News Source)**

---

## ✨ Features

### 🔍 Web Scraping
- Fetches live financial news headlines from FinViz.
- Uses custom `user-agent` to avoid access restrictions.

### 📰 Headline Extraction
- Parses each row of the news table for:
  - Ticker
  - Date
  - Time
  - News Headline

### 😊 Sentiment Analysis
- Computes **VADER compound sentiment score** for each headline.
- Classifies headlines into positive, negative, or neutral sentiment.

### 📊 Visualization
- Groups sentiment by ticker and date.
- Plots bar charts comparing company sentiment trends.

---

## 🏗️ How I Built It

### 1️⃣ Fetching and Parsing Data  
I created FinViz URLs for each ticker and fetched the HTML using `urllib.request` with a custom user-agent.  
Then, using **BeautifulSoup**, I located the `news-table` containing all news rows.

### 2️⃣ Cleaning and Structuring Data  
For each news row, I extracted:
- Headline text  
- Date and time  
- Corresponding ticker  

All entries were stored in a **Pandas DataFrame**.

### 3️⃣ Sentiment scoring
Using VADER's polarity_scores(), I computed the compound score for each headline and appended it to the DataFrame.

### 5. Visualization
To analyze trends, I grouped sentiment by ticker and date and plotted the results using Matplotlib.

---

## 📚 What I Learned
### 🧠 BeautifulSoup Parsing
How to navigate HTML structures and extract specific tables/rows.
Understanding how FinViz organizes its data.

### 🔧 Data Cleaning & Manipulation
Handling missing values, converting text dates, and structuring scraped data.
Using groupby() and .unstack() for pivot-style analysis.

### 💬 Sentiment Analysis
Understanding VADER’s scoring system (neg, neu, pos, compound).
How sentiment scores correlate with financial news headlines.

### 🖼️ Visualization
Creating grouped bar charts to compare sentiment over time.
Understanding how aggregated sentiment differs per ticker.

### 🌐 Working with HTTP Requests
Importance of user-agent headers
Handling potential blocked requests

---

## 🚀 How It Can Be Improved

- Add real-time updates using scheduled scrapers (cron / Airflow).

- Expand from FinViz to APIs like NewsAPI, Reddit, Twitter, etc.

- Build a dashboard using Streamlit or Dash.

- Add machine learning models to predict future price movement from sentiment.

- Integrate word clouds or topic modeling (LDA).

- Apply custom lexicons for finance-specific sentiment.

- Store data in SQL/NoSQL for historical tracking.

---

## 🧭 Project Roadmap (Upcoming Features)

Here are the features I plan to add in future updates:

- [ ] **Normalized Sentiment Score**  
      Convert raw VADER compound values into a scaled or standardized metric for easier comparison.

- [ ] **Sentiment & Emotion Graphs**  
      Add multi-line graphs showing positive/negative/neutral sentiment trends and emotion breakdowns.

- [ ] **Dataset-Based Analysis**  
      Instead of only live scraping, add sentiment analysis using uploaded or external datasets for larger sample sizes.

- [ ] **Indian Stock Market Support**  
      Extend scraping and sentiment processing to NSE/BSE tickers.

---
## 📈 Sentiment Analysis Graph
![Sentiment Graph](images/sentiment_graph.jpg)

*Figure 1: Average sentiment score per stock per day.*



