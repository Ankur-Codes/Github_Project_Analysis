# GitHub Project Recommender System

## 📌 Project Objective

Help developers, students, and tech enthusiasts explore **lesser-known but valuable GitHub repositories** by identifying underexplored topics in their preferred programming language.

This project uses real-world data exploration techniques, recommendation logic, and basic NLP to mimic the decision-making mindset of a product-focused analyst or researcher.

---

## 📊 Dataset Overview

* **Source**: GitHub API (Python script-based scraping)
* **Total Repositories**: \~12,000
* **Fields Used**: `Name`, `Language`, `Stars`, `Forks`, `Topics`, `Description`, `README`
* **Preprocessing Performed**:

  * Dropped missing values (e.g., missing topics)
  * Exploded comma-separated topic strings into individual rows
  * Cleaned and normalized text for downstream analysis

---

## 🛠️ Tech Stack

* **SQL** – for initial filtering and data pull (simulated in script form)
* **Python (Pandas)** – for data wrangling, cleaning, transformation
* **Matplotlib & Seaborn** – for topic/language heatmaps and visualizations
* **Jupyter Notebook** – for analysis, testing, and iterative prototyping
* **NLP Tools (Planned)** – for semantic search (TF-IDF)

---

## 🔍 Feature: Recommend Projects by Language

When the user inputs a programming language:

1. Show **Top 5 most common topics** in that language
2. Show **5 lesser-known topics** with fewer projects
3. Recommend 5 GitHub projects from one of the lesser-known topics (must have 2+ projects)

This logic helps highlight what’s popular, what’s rare, and what might be worth exploring—just like a data/product analyst might investigate usage clusters or gaps.

---

## 🧪 Sample Output

> **Language Chosen**: Python

**Top 5 Common Topics:**

* python: 255 repos
* deep-learning: 127
* machine-learning: 121
* pytorch: 93
* django: 83

**Lesser-known Topics:**

* voiceconversion: 1
* crnn: 1
* zits: 1
* adapter: 1
* gemini: 1

**Recommended Projects for 'zits':**

* Sanster/IOPaint → [https://github.com/Sanster/IOPaint](https://github.com/Sanster/IOPaint)

---

## 🚧 Future Work

### 🔹 Topic Search (via TF-IDF)

Allow users to enter project ideas (e.g., `chatbot`, `ecommerce`) and return matching repositories by analyzing README content semantically.

### 🔹 Topic Clustering

Use ML (KMeans or DBSCAN) to group similar project types and visualize tech landscape.

### 🔹 EDA Dashboard (Optional)

Build an interactive Streamlit dashboard:

* Filters: language, stars, forks, created year
* Visuals: topic distributions, growth trends

### 🔹 User Behavior Tracking (Simulated)

Track which topics/languages users are searching most. Log and analyze those queries to simulate product usage.

---

## 🧑‍💼 Why This Project Matters (For Internships / Analyst Roles)

This project demonstrates:

* End-to-end analysis from raw GitHub data
* Data wrangling, transformation, and visualization
* Smart filtering and recommendation logic
* Beginner-friendly NLP planning (TF-IDF based search)
* Clean code structure and clear output readability

It shows how a data analyst can think like a product analyst—by asking what’s common, what’s rare, and what’s worth recommending.

---

## 📁 Folder Structure

```
├── github_scraper.py         # API collection script
├── github_projects.csv       # Final dataset (12k repos)
├── language_topic_analysis.ipynb
├── tfidf_topic_search.ipynb  # (Planned)
├── heatmap_visuals.png       # Saved heatmap output
└── README.md
```

---

## 🚀 How to Run This Project

1. Clone this repo
2. Run the notebook `language_topic_analysis.ipynb`
3. Follow the prompt to enter a language
4. View recommended rare topics + GitHub projects

> Bonus: To run future semantic search, load `tfidf_topic_search.ipynb` (coming soon).

---

## 🎯 Key Takeaways for Interviews

* You’ve explored a real-world dataset with thousands of records
* You’ve built something useful—not just analysis, but **actionable suggestions**
* You’ve shown product thinking (topic gaps, segmentation, usage insights)
* You’ve layered basic NLP planning to expand the tool’s capability

---

## 👤 Creator

Built by a data-analyst-in-progress passionate about combining data exploration, product thinking, and recommendation logic to deliver practical tools that actually help people discover new ideas.
