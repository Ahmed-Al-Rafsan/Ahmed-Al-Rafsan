<div align="center">

<a href="https://ahmed-al-rafsan.github.io/"><img src="assets/hero.svg" width="100%" alt="Ahmed Al Rafsan, aeronautical engineer and AI engineer, Melbourne, Australia. A technical drawing of my conceptual aircraft with a finite-element mesh on one wing, my thesis three-ply composite laminate, and a small neural network that predicts deflection and stress. Assessed by Engineers Australia as an Aeronautical Engineer, ANZSCO 233911." /></a>

<a href="https://ahmed-al-rafsan.github.io/"><img src="assets/btn-website.svg" height="44" alt="Website" /></a>&nbsp;
<a href="https://www.linkedin.com/in/ahmed-al-rafsan-/"><img src="assets/btn-linkedin.svg" height="44" alt="LinkedIn" /></a>&nbsp;
<a href="https://www.youtube.com/@AhmedAlRafsan"><img src="assets/btn-youtube.svg" height="44" alt="YouTube" /></a>&nbsp;
<a href="mailto:ahmed.rafsan108@gmail.com"><img src="assets/btn-email.svg" height="44" alt="Email" /></a>

<sub><a href="#aeronautical-engineering">Engineering</a> &nbsp;|&nbsp; <a href="#machine-learning-and-data-projects">Projects</a> &nbsp;|&nbsp; <a href="#research">Research</a> &nbsp;|&nbsp; <a href="#skills">Skills</a> &nbsp;|&nbsp; <a href="#videos">Videos</a> &nbsp;|&nbsp; <a href="#experience">Experience</a> &nbsp;|&nbsp; <a href="#honours-and-credentials">Honours</a></sub>

</div>

## About me

I am an aeronautical engineer by training. In China I modelled a composite flapping wing in finite-element analysis, worked through the stability of a light aircraft, and learned to trust a number only after I had checked it. Back in Bangladesh, an MBA and KPI reporting for more than 500 employees, presented to a CEO, taught me how a business makes decisions. In Melbourne, a Master's in data analytics turned those habits into daily practice: cleaning messy data, building dashboards, training machine-learning models, and leading a capstone team whose priority list a client loaded into its CRM.

Now I build with AI and machine learning, and I keep returning to the place where my two fields meet: **models that make engineering analysis faster without making it any less trustworthy.**

<a href="https://ahmed-al-rafsan.github.io/"><img src="assets/route.svg" width="100%" alt="My route so far. Bangladesh, then Nanchang, China, 2014 to 2017, for aircraft design engineering. Back to Dhaka for business and people data: HR Executive and an MBA. Melbourne, 2024 to 2026, for data analytics and machine learning. Now: AI engineering." /></a>

## Aeronautical engineering

<a href="https://ahmed-al-rafsan.github.io/#engineering"><img src="assets/card-engineering.svg" width="100%" alt="Three engineering drawings from my BEng: my thesis composite laminate and 19-angle fibre sweep, the static margin and dynamic modes of a light aircraft, and three views of my conceptual aircraft. Below them, my Engineers Australia skills assessment: Professional Engineer, Aeronautical Engineer, ANZSCO 233911." /></a>

- **Composite flapping wing, my finite-element thesis.** I swept the outer-ply fibre angle of a three-ply carbon-epoxy wing from −45° to +45° in 5° steps, 19 lay-ups in ANSYS Workbench. Deformation was largest at −40° and smallest at +5°; stress was lowest near −20° to −25°. *Limits: one static load case on a simplified geometry, with no mesh-convergence check and no test data.*
- **Longitudinal stability of a light aircraft.** Static margin 18.9%. Short period: ωn 5.344 rad/s, ζ 0.702. Phugoid: ωn 0.2127 rad/s, ζ 0.106. I verified the eigenvalues in NumPy.
- **Conceptual configuration of a fighter-style aircraft.** A CATIA V5 surface model and AutoCAD three views: 8.0 m span, 12.0 m length, 18.0 m², aspect ratio 3.56. I found a 0.30 m wing-root offset in one view, traced it to its source and fixed it. *External geometry only.*
- **Aviation maintenance internship,** HNA Aviation Technic, 9 to 20 October 2017. I learned how an airline maintenance operation runs: how a jet engine is inspected and repaired part by part, and how regulation governs every step.

**[See the full engineering sheets on my website](https://ahmed-al-rafsan.github.io/#engineering)**

## Machine learning and data projects

<a href="https://github.com/Ahmed-Al-Rafsan/schools-priority-segmentation-analysis"><img src="assets/card-schools.svg" width="100%" alt="Industry capstone, team lead. Australian Schools Priority Targeting: which schools should a small business approach first? 9,855 schools, ROC-AUC 0.972, Top 200 loaded into the client's CRM, six-person team." /></a>

**What I did.** I led a six-person team through a live client engagement: merged and cleaned eight state and territory files, built a transparent priority score the client can read and challenge, segmented the market with K-Means (k = 4), and used a Random Forest to test whether the priority pattern holds up. We delivered a Top 200 outreach list, which the client loaded into its CRM, and a two-page Power BI executive dashboard.

**The decision I'd defend.** The high-priority label comes from a single variable, so I kept that variable out of the Random Forest inputs; otherwise the model would simply look up the answer. The held-out **ROC-AUC of 0.972** measures how well the label is recovered from the rest of the school profile. It does **not** measure sales conversion.

[Repository](https://github.com/Ahmed-Al-Rafsan/schools-priority-segmentation-analysis) &nbsp;|&nbsp; [Analysis code](https://github.com/Ahmed-Al-Rafsan/schools-priority-segmentation-analysis/blob/main/analysis/priority_scoring_analysis.py) &nbsp;|&nbsp; [Methodology](https://github.com/Ahmed-Al-Rafsan/schools-priority-segmentation-analysis/blob/main/docs/methodology.md)

*The client's data and dashboard stay private. The repository runs end to end on a synthetic demo dataset.*

<br />

<a href="https://github.com/Ahmed-Al-Rafsan/retail-sales-etl-pipeline"><img src="assets/card-etl.svg" width="100%" alt="Data engineering build. Retail Sales ETL and Data Quality Pipeline: which sales records can the business actually trust? 58 rows in, 2 duplicates removed, 53 accepted, 3 quarantined with a reason." /></a>

**What I built.** A batch ETL pipeline in Python, pandas and NumPy. It loads the CSV inside `try/except` with logging, profiles nulls and types, removes exact duplicates, converts types with `errors="coerce"` and a nullable `Int64`, labels every rejected row with a reason using `np.select`, exports both sets to CSV and JSON, then reads them back and checks the counts.

**The decision I'd defend.** Quarantine, don't impute. A missing quantity or price is never filled with zero, because that would quietly understate revenue. The counts reconcile: `58 = 2 duplicates + 53 accepted + 3 quarantined`.

[Repository](https://github.com/Ahmed-Al-Rafsan/retail-sales-etl-pipeline) &nbsp;|&nbsp; [Notebook](https://github.com/Ahmed-Al-Rafsan/retail-sales-etl-pipeline/blob/main/notebooks/retail_sales_ETL_pipeline.ipynb) &nbsp;|&nbsp; [Data quality rules](https://github.com/Ahmed-Al-Rafsan/retail-sales-etl-pipeline#-data-quality-rules)

*A learning build on a deliberately small, synthetic 58-row dataset. I wrote the pipeline; AI (ChatGPT) reviewed the code and helped with the documentation.*

<br />

<a href="https://github.com/Ahmed-Al-Rafsan/HR-Employee-Attrition-Predictor"><img src="assets/card-hr.svg" width="100%" alt="People analytics. Predicting Employee Attrition: who is likely to leave, and what is driving it? 1,470 records, 344 high risk, 11 SQL queries, 8 DAX measures." /></a>

**What I did.** Logistic Regression and Random Forest models with balanced class weights on the 1,470-row IBM HR attrition dataset, prioritising recall on the leaver class over raw accuracy. Eleven SQL business queries and a two-page Power BI dashboard with eight DAX measures connect the model to the people who would act on it.

[Repository](https://github.com/Ahmed-Al-Rafsan/HR-Employee-Attrition-Predictor) &nbsp;|&nbsp; [Notebook](https://github.com/Ahmed-Al-Rafsan/HR-Employee-Attrition-Predictor/blob/main/P4_HR_Attrition_Predictor.ipynb) &nbsp;|&nbsp; [Watch the walkthrough](https://youtu.be/V1bS9olSKx8)

*Scores are a demonstration on a public sample dataset, not a deployed decision system.*

<br />

<a href="https://github.com/Ahmed-Al-Rafsan/Customer-Segmentation-RFM-Analysis"><img src="assets/card-rfm.svg" width="100%" alt="Customer analytics. Customer Segmentation and RFM: which customers hold the value, and where does it leak? Over 1 million rows, 5,878 customers, 7 segments, a 177 times lifetime-value gap." /></a>

**What I did.** A seven-script Python pipeline cleaned 1,067,371 rows down to 805,549, scored 5,878 customers with RFM and grouped them into seven behavioural segments, with cohort retention and lifetime-value analysis alongside. **What it found:** 1,482 Champions, a quarter of customers, hold 69.3% of revenue, while 75 to 80% of new customers are lost within their first month.

[Repository](https://github.com/Ahmed-Al-Rafsan/Customer-Segmentation-RFM-Analysis) &nbsp;|&nbsp; [Python scripts](https://github.com/Ahmed-Al-Rafsan/Customer-Segmentation-RFM-Analysis/tree/main/python) &nbsp;|&nbsp; [Watch the walkthrough](https://youtu.be/27dancSDNOo)

<details>
<summary><strong>More projects, practice builds and job simulations</strong></summary>

<br />

| Project | Focus | Type |
| :--- | :--- | :--- |
| [Fashion Retail Intelligence](https://github.com/Ahmed-Al-Rafsan/Fashion-Retail-Intelligence) | Root cause of an 89% revenue decline, SQL and Power BI | Portfolio project |
| [Melbourne CBD Business Analysis](https://github.com/Ahmed-Al-Rafsan/melbourne-cbd-business-analysis) | 20+ years of Victorian Government open data, Python and Power BI | Portfolio project |
| [Auto Sales data cleaning](https://github.com/Ahmed-Al-Rafsan/Data-to-AI/tree/main/01-auto-sales-data-cleaning) | 2,723 order lines cleaned with quarantine instead of deletion, pandas | Practice build |
| [Quantium retail analytics](https://github.com/Ahmed-Al-Rafsan/quantium-retail-analytics) | Customer segments and trial-store uplift | Forage simulation |
| [Commonwealth Bank data science](https://github.com/Ahmed-Al-Rafsan/commbank-data-science-simulation) | Aggregation, anonymisation and 3NF schema design | Forage simulation |
| [Deloitte forensic analytics](https://github.com/Ahmed-Al-Rafsan/deloitte-forensic-analytics) | Tableau telemetry dashboard and pay-equity classification | Forage simulation |

The Forage projects are learning simulations, not employment with those organisations.

</details>

## Research

<a href="https://ahmed-al-rafsan.github.io/#research"><img src="assets/research-method.svg" width="100%" alt="How I work through a problem, in five steps: frame the question, model it, analyse, verify, report the limits. Below, my thesis sweep of 19 fibre angles from minus 45 to plus 45 degrees: deformation largest at minus 40, smallest at plus 5, stress lowest between minus 25 and minus 20." /></a>

My research experience comes from supervised engineering work: a finite-element thesis and two design projects in my aeronautical degree, and a client machine-learning project in my Master's. Each taught me the same discipline: frame a clear question, build a model of it, check the model before trusting it, and report what the result does not show.

<a href="https://ahmed-al-rafsan.github.io/#research"><img src="assets/research-interests.svg" width="100%" alt="Research interests. Aeronautical engineering: aerospace structures and composite materials, finite-element analysis and simulation, flight dynamics, aircraft design, maintenance and reliability. Where the two meet: machine-learning surrogate models, physics-informed machine learning, structural health monitoring and damage prediction, predictive maintenance from aviation data, AI agents for engineering workflows. AI engineering: machine learning and deep learning, LLM applications and retrieval, agentic AI, trustworthy and testable AI systems, data engineering." /></a>

**The idea I keep coming back to.** Engineering analysis is slow for good reasons: every result has to be checked. Machine learning trained on simulations, test data and maintenance records can make much of that work faster, and AI agents can take over the repetitive steps of design and analysis. Neither is worth much unless an engineer can trust it. That is where I want to build: AI that helps aviation move faster without lowering the standard of proof, and aviation problems that push AI engineering to be more rigorous.

## Skills

<img src="assets/toolkit.svg" width="100%" alt="Toolkit. Engineering: CATIA V5, AutoCAD, ANSYS Workbench, NumPy. Programming: Python, pandas, Jupyter, terminal, pip and venv, Git and GitHub. Data: MySQL, PostgreSQL, T-SQL, Excel, Power BI and DAX, Tableau. Machine learning: scikit-learn and model evaluation. Models I have used: logistic regression, random forest, K-Means, RFM scoring, modal analysis. My AI engineering path, in order: APIs, learning now; then services and testing, LLM applications, retrieval and evaluation, agents, deployment, deep learning." />

<img src="assets/approach.svg" width="100%" alt="How I check a dataset, PCUVCOD: profile, completeness, uniqueness, validity, consistency, outliers, document. The same seven checks, in the same order, on every dataset." />

## Videos

I present my projects the way I would to a manager or a review panel: the question, the data, the method, the dashboard and the decision.

<table>
<tr>
<td width="33%" valign="top"><a href="https://youtu.be/V1bS9olSKx8"><img src="https://img.youtube.com/vi/V1bS9olSKx8/hqdefault.jpg" width="100%" alt="Video: Employee attrition, the model, the dashboard and the decisions" /></a><br /><sub><b>Employee attrition:</b> the model, the dashboard and the decisions</sub></td>
<td width="33%" valign="top"><a href="https://youtu.be/27dancSDNOo"><img src="https://img.youtube.com/vi/27dancSDNOo/hqdefault.jpg" width="100%" alt="Video: RFM segmentation, from transactions to a retention strategy" /></a><br /><sub><b>RFM segmentation:</b> from transactions to a retention strategy</sub></td>
<td width="33%" valign="top"><a href="https://youtu.be/Y8TWx8vikOE"><img src="https://img.youtube.com/vi/Y8TWx8vikOE/hqdefault.jpg" width="100%" alt="Video: Investigating an 89 percent revenue decline with SQL and Power BI" /></a><br /><sub><b>An 89% revenue decline:</b> investigated with SQL and Power BI</sub></td>
</tr>
</table>

<a href="https://www.youtube.com/@AhmedAlRafsan"><img src="assets/btn-youtube.svg" height="40" alt="Visit my YouTube channel, Rafsan Data and AI Lab" /></a>

## Experience

| When | Role | What I did |
| :-- | :-- | :-- |
| Oct&nbsp;to&nbsp;Nov&nbsp;2026 | **Data analyst intern**, Powerdata Group Consulting, Melbourne | I cleaned Zoho CRM and Excel/CSV data and built Power BI reports. I delivered a demonstration analysis of 106 historical AusTender awards ($5.89M, 21 service categories) as an interactive dashboard and an executive brief, and recommended identity checks before any outreach. |
| Jun&nbsp;2026 | **Team lead and data analyst**, industry capstone, AIH | I led six people to a client handover: 9,855 school records and a Top 200 outreach list loaded into the client's CRM. |
| May&nbsp;2025 to&nbsp;now | **Pharmacy assistant**, Chemist Warehouse, Melbourne | I built an Excel task-tracking prototype for a six-person store team, with sign-off checks and a date-selectable management dashboard. |
| Sep&nbsp;2022 to Feb&nbsp;2024 | **HR Executive, Organisational Development**, Kazi Farms Group, Bangladesh | I ran KPI reporting and the performance-evaluation cycle for 500+ employees, reported to CEO and GM level. |
| 9&nbsp;to&nbsp;20&nbsp;Oct&nbsp;2017 | **Aviation maintenance intern**, HNA Aviation Technic, China | Twelve days of internship and training in aviation engineering and maintenance. |

## Honours and credentials

<img src="assets/honours.svg" width="100%" alt="Jiangxi Provincial Government Scholarship, awarded twice. In my second and third years I sat a competitive exam open to all international students at my university and was one of the two students selected. Each award was RMB 20,000, RMB 40,000 in total. Timeline: 2011, Golden A+ in my Secondary School Certificate with a gold medal; 2013, GPA 5.00 of 5.00 in my Higher Secondary Certificate; Year 2 and Year 3, the provincial scholarship; 2017, BEng completed." />

- **Bachelor of Engineering, Aircraft Design and Engineering**, Nanchang Hangkong University, China. February 2014 to December 2017.
- **Engineers Australia skills assessment**, 29 October 2026: Professional Engineer, Aeronautical Engineer (ANZSCO 233911).
- **Master of Business Information Systems (Data Analytics)**, Australian Institute of Higher Education, Melbourne. All course requirements completed, July 2026.
- **Master of Business Administration**, North South University, Dhaka. Completed April 2021.

<details>
<summary><strong>Professional certificates</strong></summary>

<br />

- **Google Advanced Data Analytics Professional Certificate**, Coursera, January 2026. [Verify](https://coursera.org/verify/professional-cert/QMLEPBEVKU9A)
- **IBM Data Analyst Professional Certificate**, Coursera, January 2026. [Verify](https://coursera.org/verify/professional-cert/9IOZYKAWYNQL)
- **Creative Designing in Power BI**, Microsoft through Coursera, January 2026. [Verify](https://coursera.org/verify/LPHLUJS5L5N1)
- Preparing now: Microsoft PL-300, Power BI Data Analyst. Not yet sat.

</details>

<br />

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Ahmed-Al-Rafsan/Ahmed-Al-Rafsan/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Ahmed-Al-Rafsan/Ahmed-Al-Rafsan/output/github-snake.svg" />
  <img alt="Animation of my GitHub contribution graph" src="https://raw.githubusercontent.com/Ahmed-Al-Rafsan/Ahmed-Al-Rafsan/output/github-snake.svg" width="100%" />
</picture>

<div align="center">

**Let's talk.** If my work connects with yours, whether that is a role, a project or a research question, I would be glad to hear from you.

[Website](https://ahmed-al-rafsan.github.io/) &nbsp;|&nbsp; [LinkedIn](https://www.linkedin.com/in/ahmed-al-rafsan-/) &nbsp;|&nbsp; [YouTube](https://www.youtube.com/@AhmedAlRafsan) &nbsp;|&nbsp; [ahmed.rafsan108@gmail.com](mailto:ahmed.rafsan108@gmail.com)

</div>
