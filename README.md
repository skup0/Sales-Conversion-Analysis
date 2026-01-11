Sales Conversion Analysis (SQL + Python)

OVERVIEW
This project is a case study completed as part of MATH 1130 and evaluates customer conversion
rates and sales agent performance for a simulated financial services firm. The analysis uses
SQL executed through an in-memory SQLite database, with Python used for data ingestion,
orchestration, and result inspection.

The primary objective is to test whether commonly assumed “high-value” customer cohorts
(e.g., engineers, customers aged 30+) actually convert at higher rates, and to summarize
agent-level performance using meaningful aggregate statistics.

--------------------------------------------------

KEY QUESTIONS
- Do engineers convert at higher rates than the overall customer population?
- Does age (30+) meaningfully affect conversion rates?
- How do sales agents differ in call volume, call duration, and sales outcomes?

--------------------------------------------------

DATA SOURCES
The analysis is based on three datasets:
- customer.csv: customer demographics and occupation
- agent.csv: sales agent identifiers
- call.csv: call-level data including duration, pickup status, and product sales

All data is loaded into an in-memory SQLite database to support SQL-based analysis.

--------------------------------------------------

DATA AVAILABILITY
The raw datasets used in this analysis are not included in the repository due to GitHub file
size constraints. The repository therefore contains the analysis notebook and a rendered HTML
version for full transparency and review of results.

All data processing steps, SQL queries, and analytical logic are fully documented in the
notebook.

--------------------------------------------------

TOOLS & TECHNOLOGIES
- Python
- SQLite
- SQLAlchemy
- Pandas

--------------------------------------------------

PROJECT STRUCTURE
.
├── sales_conversion_analysis_sql.ipynb
├── sales_conversion_analysis_sql.html
├── README.txt
└── requirements.txt

--------------------------------------------------

METHODOLOGY
1. Loaded CSV data into Pandas DataFrames and persisted them to SQLite tables.
2. Performed data sanity checks to confirm expected record counts and joins.
3. Computed conversion rates using SQL for:
   - Overall customer population
   - Engineers
   - Customers aged 30+
   - Engineers aged 30+
4. Aggregated call-level data to the agent level to compute:
   - Total calls answered
   - Call duration statistics (min, max, mean)
   - Total sales
   - Agent-level conversion rates
5. Restricted agent analysis to picked-up calls and removed invalid call durations.

--------------------------------------------------

KEY FINDINGS
- Engineers convert at approximately the same rate as the overall population (~21%).
- Customers aged 30+ show only a small increase relative to baseline conversion rates.
- Engineers aged 30+ slightly underperform the overall conversion rate.
- Agent conversion rates vary modestly, indicating differences in effectiveness.
- Agent-level aggregation provides clearer insights than raw call-level data.

--------------------------------------------------

LIMITATIONS
- The dataset is simulated and intended for instructional purposes.
- No statistical significance testing was performed.
- Conversion rates are observational and not causal.
- Agent performance metrics are conditional on picked-up calls only.

--------------------------------------------------

CONCLUSIONS
This case study demonstrates how SQL and Python can be used to validate business assumptions,
analyze customer cohorts, and summarize operational performance. The results highlight the
importance of data-driven validation when evaluating intuitive or “common-sense” hypotheses.

--------------------------------------------------

HOW TO RUN
1. Clone the repository.
2. Install dependencies:
   pip install -r requirements.txt
3. Open and run the notebook:
   jupyter notebook sales_conversion_analysis_sql.ipynb

--------------------------------------------------

NOTES
This project was completed as part of MATH 1130 coursework and refactored for portfolio and
resume presentation.
