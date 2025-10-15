

# 📘 Course: **Data Analytics for Product Development (SQL + Python + Power BI)**

---

## 🎯 Course Goal

Equip learners to use data to drive product strategy and decision-making. By course end, students will be able to:

* Design and compute product metrics (DAU/MAU, retention, funnel conversions, churn).
* Query and analyze user / event data using **SQL**.
* Perform data exploration, feature engineering, and predictive modeling in **Python**.
* Build interactive product dashboards using **Power BI**.
* Integrate SQL, Python, and Power BI into an analytics pipeline and deliver a full product case study.

---

## 🧠 Learning Outcomes

After completing this course, learners will:

1. Understand key product analytics concepts (activation, retention, engagement, churn).
2. Develop skills in writing analytical SQL queries on user & event datasets.
3. Use Python for data cleaning, EDA, feature engineering, and modeling.
4. Build dashboards and reports tailored to product / growth metrics in Power BI.
5. Build and deploy an end-to-end analytics workflow linking SQL, Python, and Power BI.
6. Present data-driven product insights and recommendations in a polished deliverable.

---

## 🗓️ 10-Week Syllabus Overview

| Week | Theme / Focus                                     | Core Tools                           | Project / Emphasis                                               |
| ---- | ------------------------------------------------- | ------------------------------------ | ---------------------------------------------------------------- |
| 1    | Product Analytics Foundations & Metrics           | SQL / CSV / Python (for exploration) | Metrics dictionary, explore raw user event data                  |
| 2    | SQL for Product Analytics (Event / Feature Usage) | SQL                                  | Feature usage queries, user activity aggregations                |
| 3    | Funnels, Cohorts & Retention in SQL               | SQL                                  | Build funnel conversions, cohort retention tables                |
| 4    | Python for Product Data Exploration & EDA         | Python (Pandas, Seaborn)             | Feature adoption, usage trends, correlations                     |
| 5    | Experimentation & A/B Testing Analysis            | Python (SciPy, statsmodels)          | A/B test evaluation, significance, effect size                   |
| 6    | Power BI for Product Dashboards                   | Power BI (data modeling + DAX)       | Build dashboards for product metrics                             |
| 7    | Growth & Retention Modeling                       | Python (scikit-learn)                | Churn prediction, feature importance, segmentation               |
| 8    | Integrating SQL, Python & Power BI Pipelines      | All tools                            | Automate data extraction → transformation → dashboard refresh    |
| 9    | Capstone Project Start                            | All tools                            | Begin end-to-end product analytics case                          |
| 10   | Capstone Delivery & Presentation                  | All tools                            | Final deliverables: dashboard, analysis, recommendations, slides |

---

## 📖 Detailed Weekly Breakdown

Below is a week-by-week breakdown: topics, deliverables, pointers, and dataset mapping.

---

### **Week 1 – Foundations & Product Metrics**

**Topics:**

* Introduction to product analytics and the role of data in product decisions
* Core metrics: DAU, WAU, MAU, activation, retention, churn, engagement
* Data types in product analytics: user tables, event logs, session logs
* Event schema, timestamp handling

**Deliverables:**

* **Metrics Dictionary**: define 6–10 key product metrics with formulas, data sources, and rationale
* **Exploratory Report**: load a raw event dataset and explore patterns (event counts over time, user-level summary)

**Datasets / Resources (Week 1):**

* **User Activity** — accelerometer / behavior dataset (simulate event logs)
  → [https://www.kaggle.com/datasets/karanjakhar/user-activity](https://www.kaggle.com/datasets/karanjakhar/user-activity)
* **User Activity Log** — generic event sequences per user
  → [https://www.kaggle.com/datasets/chienhsianghung/user-activity-log](https://www.kaggle.com/datasets/chienhsianghung/user-activity-log)
* **User Sessions Data** — sessions per user (aggregateable to events)
  → [https://www.kaggle.com/datasets/pawankumar97/user-sessions-data](https://www.kaggle.com/datasets/pawankumar97/user-sessions-data)
* **Mobile Device Usage & Behavior** — usage / behavior logs for features
  → [https://www.kaggle.com/datasets/valakhorasani/mobile-device-usage-and-user-behavior-dataset](https://www.kaggle.com/datasets/valakhorasani/mobile-device-usage-and-user-behavior-dataset)

---

### **Week 2 – SQL for Product Analytics (Usage / Events)**

**Topics:**

* Loading CSV or JSON event logs into SQL (PostgreSQL, SQLite)
* Basic SELECT / WHERE / GROUP BY on user / event data
* Time-based aggregations (by day, week, user)
* Feature usage counts and user-level aggregations

**Deliverables:**

* SQL queries answering questions such as:

  * “How many users triggered Feature A vs Feature B in each week?”
  * “Which users are active more than X days?”
  * “Count events per feature per user segment”

**Dataset Use:**

* Use the same event / sessions datasets from Week 1, imported into SQL.
* Optionally simulate or derive a `feature_usage` table from the session logs.

---

### **Week 3 – Funnels, Cohorts & Retention (SQL Advanced)**

**Topics:**

* Funnel analysis: define steps (e.g. “signup → first use → second use → retention”)
* Cohort analysis: grouping users by signup period and tracking behavior over time
* Retention curves: compute % of users active in subsequent periods
* Window functions, `LEAD` / `LAG`, `ROW_NUMBER`, cumulative sums

**Deliverables:**

* SQL scripts:

  * Funnel conversion rates across steps
  * Retention tables by cohort (e.g. monthly cohorts)
  * User “churn” detection queries

**Reference / Example Datasets / Notebooks (Week 3):**

* **Cohort Analysis with Python (Online Retail II data)** — cohort techniques
  → [https://www.kaggle.com/code/ahmetokanyilmaz/cohort-analysis-with-python](https://www.kaggle.com/code/ahmetokanyilmaz/cohort-analysis-with-python)
* **Marketing Analytics: Cohort Analysis** — retention / cohorts examples
  → [https://www.kaggle.com/code/mustafacicek/marketing-analytics-cohort-analysis](https://www.kaggle.com/code/mustafacicek/marketing-analytics-cohort-analysis)
* **Cohort Analysis — Customer Retention**
  → [https://www.kaggle.com/code/nuranynovita/cohort-analysis-customer-retention](https://www.kaggle.com/code/nuranynovita/cohort-analysis-customer-retention)
* **Customer Transaction – Cohort Analysis**
  → [https://www.kaggle.com/code/kelvinprawtama/customer-transaction-cohort-analysis](https://www.kaggle.com/code/kelvinprawtama/customer-transaction-cohort-analysis)

These notebooks primarily use Python, but they illustrate logic and cohort construction you can port into SQL.

---

### **Week 4 – Python for Product Data Exploration & EDA**

**Topics:**

* Loading data from SQL or CSV into Pandas
* Cleaning event logs, timestamp conversion, deduplication
* Exploratory analysis: distribution of event counts, user-level summaries
* Visualizations: daily / weekly active users, feature usage over time, correlation plots
* Feature adoption trends

**Deliverables:**

* Jupyter notebook exploring:

  * Active users over time
  * Feature usage patterns
  * Relationships between usage of features and retention

**Dataset Use:**

* Use the same event tables (or derived CSV) from Weeks 1–3
* Optionally blend session + event + feature info into one analytical table

---

### **Week 5 – Experimentation & A/B Testing Analysis**

**Topics:**

* Setting up experiments: test/control groups, randomization
* Hypothesis testing: t-test, chi-square, significance, p-values
* Confidence intervals, effect size
* Interpreting experiment results in product context

**Deliverables:**

* Jupyter notebook analyzing a simulated or real A/B dataset:

  * Compute metrics per arm
  * Statistical significance testing
  * Visualizations (bar charts, confidence intervals)
  * Recommendation on which variant to choose

**Suggested Dataset:**

* **A/B Test Results Dataset** — Kaggle A/B test data
  → (Search “A/B test data Kaggle”)

  * If needed, you can simulate your own experiment data by assigning random users to groups and simulating outcomes (e.g. feature adoption, conversion).

---

### **Week 6 – Power BI for Product Dashboards**

**Topics:**

* Connecting Power BI to SQL database, CSV exports, or Python output
* Data modeling in Power BI: relationships among user, event, and feature tables
* DAX basics: calculated columns, measures
* Visual elements: KPI cards, line charts, funnel visuals, slicers
* Dashboard design and storytelling principles

**Deliverables:**

* Power BI `.pbix` file with a dashboard that includes:

  * DAU / WAU / MAU trends
  * Feature usage breakdown
  * Funnel conversion visuals
  * Retention / cohort visuals
* A short document (or slide) explaining dashboard structure and design choices

**Reference Template / Inspiration:**

* Microsoft Power BI product or usage dashboards from community gallery
* Adapt visuals from tutorials in product analytics dashboards

---

### **Week 7 – Growth & Retention Modeling (Python)**

**Topics:**

* Preparing labeled data (e.g., “churned” vs “retained” users)
* Handling class imbalance (resampling, weighting)
* Logistic Regression, Random Forest, or other classifiers
* Model evaluation: accuracy, ROC AUC, precision/recall
* Feature importance / interpretation to derive actionable insights

**Deliverables:**

* Jupyter notebook building a model to predict user churn or disengagement
* Evaluation metrics, ROC curves, feature importance plots
* Written interpretation: which features drive churn, what to act on

**Dataset Use:**

* Use earlier event + user tables to derive labeled dataset
* Optionally use **Telco Customer Churn** (adapted) as a base:
  → [https://www.kaggle.com/datasets/blastchar/telco-customer-churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

---

### **Week 8 – Integrating SQL, Python & Power BI Pipelines**

**Topics:**

* Using Python (e.g. `psycopg2` or `sqlalchemy`) to query SQL and retrieve data
* Transforming / cleaning in Python, exporting to CSV / database
* Setting up Power BI to refresh from those outputs
* Automating via scheduling (cron, Azure Functions, etc.)
* Logging, error handling, versioning

**Deliverables:**

* Python script or module that:

  * Pulls data from SQL
  * Cleans / aggregates / transforms
  * Exports to a location Power BI can read
* Documentation or instructions for refreshing the pipeline
* A refreshed Power BI dashboard using the pipeline output

---

### **Weeks 9 & 10 – Capstone Project**

**Theme:** **Product Growth Strategy Case Study**
You are a product analyst in a SaaS or mobile app company facing challenges in user activation, retention, and growth.

**Deliverables:**

1. **SQL Scripts** — full data extraction, funnel, retention, cohort queries
2. **Python Notebooks / Scripts** — EDA, modeling, transformations
3. **Power BI Dashboard** (.pbix) — integrated visuals for user behavior, retention, growth
4. **Presentation / Report** — executive summary, key findings, strategic recommendations

**Suggested Workflow:**

* Week 9: Data ingestion, SQL & Python analysis
* Week 10: Dashboard build, story refinement, presentation

**Possible Extra Dataset(s):**

* **Spotify User Behavior** — real usage events
  → [https://www.kaggle.com/datasets/meeraajayakumar/spotify-user-behavior-dataset](https://www.kaggle.com/datasets/meeraajayakumar/spotify-user-behavior-dataset)
* **CLV & Cohort Analysis** dataset
  → [https://www.kaggle.com/code/haithamabadla/clv-cohort-analysis](https://www.kaggle.com/code/haithamabadla/clv-cohort-analysis)

You can combine or adapt these to fit your product case.

---

## 🗂️ GitHub / Folder Structure

Here’s the folder structure you can use for the course repository or for each student to mirror:

```
/ProductAnalytics_Course/
│
├── /01_foundations/
│   ├── raw_data/
│   ├── cleaned_data/
│   └── metrics_dictionary.xlsx
│
├── /02_sql_feature_usage/
│   └── feature_usage_queries.sql
│
├── /03_sql_funnels_retention/
│   └── funnels_cohorts_queries.sql
│
├── /04_python_eda/
│   └── eda_feature_usage.ipynb
│
├── /05_ab_testing/
│   └── ab_test_analysis.ipynb
│
├── /06_powerbi_dashboard/
│   └── product_dashboard_v1.pbix
│
├── /07_churn_modeling/
│   └── churn_modeling_notebook.ipynb
│
├── /08_integration_pipeline/
│   └── pipeline.py
│
└── /09_10_capstone/
    ├── sql_capstone.sql
    ├── python_analysis.ipynb
    ├── dashboard_capstone.pbix
    └── presentation_slides.pptx
```

Each subfolder can also include a `README.md` explaining context, instructions, and expected deliverables.

