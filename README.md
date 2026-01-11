Sales Conversion Analysis (SQL + Python)

OVERVIEW
This project is a case study completed as part of MATH 1130 and analyzes customer conversion
rates and sales agent performance for a simulated financial services firm. Using SQL executed
through an in-memory SQLite database and Python for orchestration, the analysis evaluates
whether commonly assumed “high-value” customer cohorts (e.g., engineers, customers aged 30+)
are more likely to purchase products.

The project emphasizes hypothesis testing, cohort analysis, and operational reporting using
SQL in a production-style workflow.

--------------------------------------------------

KEY QUESTIONS
- Do engineers convert at higher rates than the overall customer population?
- Does age (30+) affect conversion rate?
- How do sales agents differ in call volume, call duration, and sales outcomes?

--------------------------------------------------

DATA SOURCES
The analysis uses three CSV datasets:
- customer.csv: customer demographics and occupation
- agent.csv: sales agent identifiers
- call.csv: call-level data including duration, pickup status, and product sales

The data is loaded into an in-memory SQLite database for SQL-based analysis.

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
├── customer.csv
├── agent.csv
├── call.csv
├── README.txt
└── requirements.txt

--------------------------------------------------

METHODOLOGY
1. Loaded CSV data into Pandas DataFrames and persisted them to SQLite.
2. Performed data sanity checks to validate record counts and joins.
3. Computed conversion rates using SQL for:
   - Overall customer population
   - Engineers
   - Customers aged 30+
   - Engineers aged 30+
4. Aggregated call-level data to the agent level to evaluate call volume, duration
   statistics, total sales, and conversion rates.
5. Restricted agent analysis to picked-up calls and removed invalid call durations.

--------------------------------------------------

KEY FINDINGS
- Engineers convert at approximately the same rate as the overall population (~21%).
- Customers aged 30+ show only a small increase relative to baseline.
- Engineers aged 30+ slightly underperform the baseline conversion rate.
- Agent conversion rates vary moderately, indicating differences in effectiveness.
- Agent-level aggregation provides clearer insight than raw call logs.

--------------------------------------------------

LIMITATIONS
- The dataset is simulated and intended for instructional purposes.
- No statistical significance testing was performed.
- Conversion rates are observational and not causal.
- Agent conversion rates are conditional on picked-up calls only.

--------------------------------------------------

CONCLUSIONS
This case study demonstrates how SQL and Python can be used to validate business assumptions,
analyze customer cohorts, and summarize operational performance. The results highlight the
importance of testing intuitive hypotheses with data rather than relying on assumptions.

--------------------------------------------------

HOW TO RUN
1. Clone the repository.
2. Ensure customer.csv, agent.csv, and call.csv are in the project directory.
3. Install dependencies:
   pip install -r requirements.txt
4. Open and run the notebook:
   jupyter notebook sales_conversion_analysis_sql.ipynb

--------------------------------------------------

NOTES
This project was completed as part of MATH 1130 coursework and refactored for portfolio and
resume presentation.
