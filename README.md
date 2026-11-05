<div align="center">

<a href="https://ahmed-al-rafsan.github.io/"><img src="assets/hero.svg" width="100%" alt="Ahmed Al Rafsan, data analyst in Melbourne, Australia, open to data analyst and junior data engineer roles. Making data make sense. The path: aeronautical engineering, HR and KPI reporting, data analytics, and data engineering, which he is building now. SQL, Python, Power BI, ETL pipelines." /></a>

<a href="https://ahmed-al-rafsan.github.io/"><img src="assets/btn-portfolio.svg" height="44" alt="Portfolio" /></a>&nbsp;
<a href="https://www.linkedin.com/in/ahmed-al-rafsan-/"><img src="assets/btn-linkedin.svg" height="44" alt="LinkedIn" /></a>&nbsp;
<a href="https://www.youtube.com/@AhmedAlRafsan"><img src="assets/btn-youtube.svg" height="44" alt="YouTube" /></a>&nbsp;
<a href="mailto:ahmed.rafsan108@gmail.com"><img src="assets/btn-email.svg" height="44" alt="Email" /></a>

<br />

![SQL](https://img.shields.io/badge/SQL-0f2250?style=for-the-badge&logo=mysql&logoColor=white)
![Python](https://img.shields.io/badge/Python-0f2250?style=for-the-badge&logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-0f2250?style=for-the-badge&logo=pandas&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-0f2250?style=for-the-badge&logo=powerbi&logoColor=F2C811)
![Excel](https://img.shields.io/badge/Excel-0f2250?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-0f2250?style=for-the-badge&logo=jupyter&logoColor=F37626)
![Git](https://img.shields.io/badge/Git%20%26%20GitHub-0f2250?style=for-the-badge&logo=github&logoColor=white)

<sub>Melbourne, Australia · Open to Data Analyst and Junior Data Engineer roles</sub>

</div>

## From a business question to a useful answer — and now, to a reliable pipeline

I'm Rafsan, a **data analyst with an aeronautical engineering degree and a background in HR reporting**, now building **data engineering** foundations. I work in SQL, Python and Power BI to explore data, explain what is driving a pattern, and turn the findings into recommendations someone can act on.

Before analytics, I owned KPI reporting and performance evaluation for **500+ employees** at Kazi Farms Group, reporting to CEO and GM level. More recently I led a **six-person industry capstone team** at the Australian Institute of Higher Education, where I completed my **Master of Business Information Systems (Data Analytics)** in 2026.

My current focus is the engineering side of data: pipelines that are repeatable, explain what they rejected, and prove that every row is accounted for.

<table>
  <tr>
    <td width="33%" valign="top"><b>🔨&nbsp; Building now</b><br />Data engineering foundations in Python: ETL, data-quality rules, logging and error handling.</td>
    <td width="33%" valign="top"><b>📚&nbsp; Learning next</b><br />Python for data engineering and APIs, then Azure Data Factory, Databricks and PySpark. Planned, not yet used in a project.</td>
    <td width="33%" valign="top"><b>🎯&nbsp; Open to</b><br />Data Analyst and Junior Data Engineer roles, anywhere in Australia or remote.</td>
  </tr>
</table>

## Latest build — data engineering

<a href="https://github.com/Ahmed-Al-Rafsan/retail-sales-etl-pipeline"><img src="assets/card-etl.svg" width="100%" alt="Data engineering, Python ETL. Retail Sales ETL Pipeline: which sales records can the business actually trust? 58 raw rows, 2 exact duplicate copies removed, 53 accepted, typed and exported, 3 quarantined with a reason. Extract with try/except and logging, clean, cast types, a quantity and price gate, then load to CSV and JSON, read back, check and log. Synthetic 58-row sample, learning build, AI-assisted code review and documentation." /></a>

**The question.** A retail export arrives with duplicate orders, missing quantities and a price typed as text. Which records are safe to report on, and what happens to the rest?

**What I built.** A batch ETL pipeline in a Jupyter notebook with Python, pandas and NumPy. It loads the CSV inside `try/except` with logging, profiles nulls and types, removes exact duplicates, converts types with `errors="coerce"` and a nullable `Int64`, splits the rows with a boolean mask, labels every rejected row with a reason using `np.select`, exports both sets to CSV and JSON, then reads the files back and checks the counts.

**The decision I'd defend.** Quarantine, don't impute. A missing quantity or price is never filled with zero, because that would quietly understate revenue. Those rows go to a separate file with the reason attached, a missing discount stays unknown rather than becoming 0%, and the counts reconcile: `58 = 2 duplicates + 53 accepted + 3 quarantined`.

**[Explore the pipeline →](https://github.com/Ahmed-Al-Rafsan/retail-sales-etl-pipeline)** &nbsp;·&nbsp; [Notebook](https://github.com/Ahmed-Al-Rafsan/retail-sales-etl-pipeline/blob/main/notebooks/retail_sales_ETL_pipeline.ipynb) &nbsp;·&nbsp; [Sample output](https://github.com/Ahmed-Al-Rafsan/retail-sales-etl-pipeline/tree/main/sample_output) &nbsp;·&nbsp; [Data quality rules](https://github.com/Ahmed-Al-Rafsan/retail-sales-etl-pipeline#-data-quality-rules)

*A learning build on a deliberately small, synthetic 58-row dataset. I wrote the pipeline step by step; AI (ChatGPT) reviewed the code and helped with the documentation and GitHub publishing.*

## Featured analytics work

<a href="https://github.com/Ahmed-Al-Rafsan/schools-priority-segmentation-analysis"><img src="assets/card-schools.svg" width="100%" alt="Industry capstone, Australia. Schools priority targeting: which schools should a small business approach first? Team lead and data analyst, six-person team. 9,855 schools in the national dataset, 3,344 met the high-priority threshold, ROC-AUC 0.972 on held-out data, 200 prioritised for CRM outreach." /></a>

**The question.** A small Australian business was approaching a national list of schools one by one, with no targeting logic. Which schools should it approach first?

**What I did.** Led the team and the analytics workstream: merged and cleaned eight state and territory files, built a transparent priority score the client can read and challenge, segmented the market with K-Means (k = 4), and used a Random Forest to test whether the priority pattern holds up. We delivered a Top 200 outreach list, which was loaded into the client's CRM, a two-page Power BI executive dashboard, and support after handover.

**The decision I'd defend.** The high-priority label is derived from a single variable, so that variable is excluded from the Random Forest inputs — otherwise the model would simply look up the answer. The held-out **ROC-AUC of 0.972** measures how well the label is recovered from the rest of the school profile. It does **not** measure sales conversion.

**[Explore the project →](https://github.com/Ahmed-Al-Rafsan/schools-priority-segmentation-analysis)** &nbsp;·&nbsp; [Analysis code](https://github.com/Ahmed-Al-Rafsan/schools-priority-segmentation-analysis/blob/main/analysis/priority_scoring_analysis.py) &nbsp;·&nbsp; [Methodology](https://github.com/Ahmed-Al-Rafsan/schools-priority-segmentation-analysis/blob/main/docs/methodology.md)

*The client's data and dashboard stay private. The repository runs end to end on a synthetic demo dataset; the engagement metrics above are not a benchmark for that demo.*

<br />

<a href="https://github.com/Ahmed-Al-Rafsan/Customer-Segmentation-RFM-Analysis"><img src="assets/card-rfm.svg" width="100%" alt="Portfolio study, customer analytics. Customer segmentation and RFM: which customers hold the value, and where does it leak? Over 1 million transaction rows, 5,878 customers scored with RFM, 7 behavioural segments, a 177 times average lifetime-value gap between Champions and Lost customers. Champions are 25 percent of customers and 69.3 percent of revenue; 75 to 80 percent of new customers are lost within month one." /></a>

**The question.** In a UK online retailer's transactions, which customers hold the value — and where is it leaking?

**What I did.** A seven-script Python pipeline cleaned 1,067,371 rows down to 805,549, scored 5,878 customers with RFM and grouped them into seven behavioural segments, with cohort retention and lifetime-value analysis alongside. Eight SQL queries in MySQL and a three-page Power BI dashboard carry the findings.

**What it found.** 1,482 Champions — a quarter of customers — account for 69.3% of revenue, while 75–80% of new customers are lost within their first month, which points at onboarding.

**[Explore the project →](https://github.com/Ahmed-Al-Rafsan/Customer-Segmentation-RFM-Analysis)** &nbsp;·&nbsp; [Python scripts](https://github.com/Ahmed-Al-Rafsan/Customer-Segmentation-RFM-Analysis/tree/main/python) &nbsp;·&nbsp; [SQL](https://github.com/Ahmed-Al-Rafsan/Customer-Segmentation-RFM-Analysis/tree/main/SQL) &nbsp;·&nbsp; [Watch the walkthrough](https://youtu.be/27dancSDNOo)

*An analytical portfolio study on public data. The recommendations are analysis, not measured commercial outcomes.*

<br />

<a href="https://github.com/Ahmed-Al-Rafsan/HR-Employee-Attrition-Predictor"><img src="assets/card-hr.svg" width="100%" alt="Portfolio study, people analytics. HR employee attrition: who is likely to leave, and what is driving it? 1,470 employee records, 344 scored as high risk, 352 medium, 774 low; 11 SQL business queries; 8 custom DAX measures." /></a>

**The question.** Which employees are most likely to leave, and what is driving it?

**What I did.** Logistic Regression and Random Forest models with balanced class weights on the 1,470-row IBM HR attrition dataset, prioritising recall on the leaver class over raw accuracy. Eleven SQL business queries and a two-page Power BI dashboard with eight DAX measures connect the model to stakeholder reporting. My HR background shaped the questions and how the findings are presented.

**[Explore the project →](https://github.com/Ahmed-Al-Rafsan/HR-Employee-Attrition-Predictor)** &nbsp;·&nbsp; [SQL analysis](https://github.com/Ahmed-Al-Rafsan/HR-Employee-Attrition-Predictor/blob/main/p4_HR_Attrition_Project.sql) &nbsp;·&nbsp; [Notebook](https://github.com/Ahmed-Al-Rafsan/HR-Employee-Attrition-Predictor/blob/main/P4_HR_Attrition_Predictor.ipynb) &nbsp;·&nbsp; [Watch the walkthrough](https://youtu.be/V1bS9olSKx8)

*Scores are a demonstration on a public sample dataset, not a deployed decision system.*

<details>
<summary><strong>More projects, practice builds and job simulations</strong></summary>

<br />

| Project | Focus | Type |
| :--- | :--- | :--- |
| [Fashion Retail Intelligence](https://github.com/Ahmed-Al-Rafsan/Fashion-Retail-Intelligence) | Root cause of an 89% revenue decline · SQL, Power BI | Portfolio project |
| [Melbourne CBD Business Analysis](https://github.com/Ahmed-Al-Rafsan/melbourne-cbd-business-analysis) | 20+ years of Victorian Government open data · Python, Power BI | Portfolio project |
| [Auto Sales data cleaning](https://github.com/Ahmed-Al-Rafsan/Data-to-AI/tree/main/01-auto-sales-data-cleaning) | 2,723 order lines cleaned with quarantine instead of deletion · pandas | Practice build |
| [Quantium retail analytics](https://github.com/Ahmed-Al-Rafsan/quantium-retail-analytics) | Customer segments and trial-store uplift | Forage simulation |
| [Commonwealth Bank data science](https://github.com/Ahmed-Al-Rafsan/commbank-data-science-simulation) | Aggregation, anonymisation and 3NF schema design | Forage simulation |
| [Deloitte forensic analytics](https://github.com/Ahmed-Al-Rafsan/deloitte-forensic-analytics) | Tableau telemetry dashboard and pay-equity classification | Forage simulation |

The Forage projects are learning simulations, not employment with those organisations.

</details>

## Toolkit

<img src="assets/toolkit.svg" width="100%" alt="T-shaped skills map. Depth, used in every project: SQL and MySQL, Python with pandas, NumPy, logging and try/except, Power BI and DAX, Excel. Breadth applied in projects: Python ETL, applied machine learning with scikit-learn, statistics, Tableau, Git and GitHub, relational data design, AI-assisted work. Learning next, not yet used in a project: Python for data engineering and APIs, Azure Data Factory, Databricks and PySpark, Delta Lake, CI/CD. Long-term interest: data analysis and ML applied to aerospace." />

**Learning next:** Python for data engineering and APIs, then a cloud pipeline on Azure Data Factory and Databricks with PySpark and Delta Lake. These are a roadmap, not completed experience.

**Long-term interest:** applying data and AI to aerospace problems, building on my engineering education.

## How I approach the work

<img src="assets/approach.svg" width="100%" alt="Four steps. Define the decision. Examine the data with PCUVCOD: profile, completeness, uniqueness, validity, consistency, outliers, document. Explain the reasoning. Make the handover useful." />

<details>
<summary><strong>Education and professional learning</strong></summary>

<br />

- **Master of Business Information Systems (Data Analytics)** — Australian Institute of Higher Education, Melbourne · completed 2026
- **MBA in Human Resource Management** — North South University
- **Bachelor of Engineering, Aircraft Design & Engineering** — Nanchang Hangkong University, China
- **Google Advanced Data Analytics Professional Certificate** — Coursera
- **IBM Data Analyst Professional Certificate** — Coursera
- **Creative Designing in Power BI** — Microsoft / Coursera
- **Data engineering** — self-directed study, 2026: Python ETL, data quality, logging and error handling

</details>

<br />

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Ahmed-Al-Rafsan/Ahmed-Al-Rafsan/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Ahmed-Al-Rafsan/Ahmed-Al-Rafsan/output/github-snake.svg" />
  <img alt="Animation of my GitHub contribution graph" src="https://raw.githubusercontent.com/Ahmed-Al-Rafsan/Ahmed-Al-Rafsan/output/github-snake.svg" width="100%" />
</picture>

<div align="center">

**Let's connect.** I'm interested in work where careful analysis, reliable data and clear communication make a difference.

[Portfolio](https://ahmed-al-rafsan.github.io/) · [LinkedIn](https://www.linkedin.com/in/ahmed-al-rafsan-/) · [YouTube](https://www.youtube.com/@AhmedAlRafsan) · [ahmed.rafsan108@gmail.com](mailto:ahmed.rafsan108@gmail.com)

</div>
