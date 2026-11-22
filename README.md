# Insurance_Claims_Analytics
# Insurance Claims & Operations Analytics

## Project Overview

This project focuses on analysing simulated insurance claims data to evaluate claims performance, identify data-quality issues, monitor operational metrics, and generate meaningful business insights.

The project uses Python for data cleaning and exploratory data analysis, SQL for querying and reporting, and Power BI for interactive dashboard development.

**Project Type:** End-to-End Data Analytics Project

## Project Objectives

- Analyse insurance claims and operational performance.
- Clean and validate records to improve data quality.
- Identify missing values, duplicate records and invalid entries.
- Analyse claim status, claim amounts and processing times.
- Identify trends and patterns across insurance types and regions.
- Develop an interactive Power BI dashboard for business reporting.
- Provide data-driven recommendations to support operational decisions.

## Dataset Description

The project uses a simulated insurance claims dataset generated using Python.

The original dataset contains 1,000 unique claim records. Ten duplicate records and several data-quality issues were deliberately introduced to simulate real-world data challenges.

**Dataset features include:**

| Column | Description |
|---|---|
| claim_id | Unique insurance claim identifier |
| policy_id | Insurance policy identifier |
| customer_age | Customer age |
| claim_type | Health, Motor, Property or Travel |
| region | Customer or claim region |
| claim_amount | Total requested claim amount |
| status | Approved, Rejected or Pending |
| fraud_flag | Simulated fraud indicator |
| incident_date | Date of incident |
| reported_date | Date claim was reported |
| approved_amount | Approved claim amount |
| processing_days | Claim processing duration |

**Dataset note:** All records are simulated for educational and portfolio purposes. No real customer or insurance company data is used.

## Technologies Used

- **Python:** Data cleaning, manipulation and analysis.
- **Pandas:** Data processing and transformation.
- **NumPy:** Numerical operations.
- **Matplotlib:** Data visualization.
- **Seaborn:** Statistical visualization.
- **SQL (SQLite):** Database queries and reporting.
- **Power BI:** Interactive dashboards and KPI reporting.
- **Google Colab:** Python development environment.
- **GitHub:** Project documentation and version control.

## Project Workflow

1. Dataset generation using Python.
2. Data exploration and understanding.
3. Data cleaning and validation.
4. Exploratory Data Analysis (EDA).
5. SQL database creation and querying.
6. Business metrics calculation.
7. Power BI dashboard development.
8. Business insights and recommendations.

## Data Cleaning Methodology

The following data-quality checks were performed using Python and Pandas:

- Identified and removed duplicate claim records using claim IDs.
- Identified missing customer age and filled missing values using the median.
- Replaced missing region information with an "Unknown" category.
- Identified invalid customer ages.
- Detected negative claim amounts.
- Identified reporting dates earlier than incident dates.
- Created a data-quality issue column to flag invalid records.
- Separated records requiring investigation from the analysis-ready dataset.

The final analysis-ready dataset contains **985 valid unique claim records**.

Records with identified data-quality issues were preserved separately for investigation rather than silently deleted.

## SQL Analysis

SQLite was used to create a database and perform business-oriented queries.

The following SQL concepts were applied:

- SELECT
- WHERE
- ORDER BY
- COUNT
- SUM
- AVG
- GROUP BY
- Aggregate functions

**Example: Claims by Insurance Type**

```sql
SELECT
    claim_type,
    COUNT(*) AS total_claims,
    SUM(claim_amount) AS total_amount
FROM insurance_claims
GROUP BY claim_type;
```

**Example: Pending Claims by Region**

```sql
SELECT
    region,
    COUNT(*) AS pending_claims,
    SUM(claim_amount) AS pending_amount
FROM insurance_claims
WHERE status = 'Pending'
GROUP BY region
ORDER BY pending_claims DESC;
```

**Example: Average Processing Time**

```sql
SELECT
    status,
    ROUND(AVG(processing_days), 2)
        AS avg_processing_days
FROM insurance_claims
GROUP BY status;
```

## Key Performance Indicators (KPIs)

The Power BI dashboard includes the following metrics:

- Total Claims: 985
- Approved Claims: 574
- Rejected Claims: 218
- Pending Claims: 193
- Average Processing Days: 15.69

*These values reflect the current simulated dataset and dashboard. They are not actual insurance industry statistics.*

## Power BI Dashboard

The interactive dashboard provides an overview of insurance claims performance.

**Dashboard components:**

- KPI cards for total claims, approved claims, pending claims and average processing days.
- Donut chart showing claim distribution by status.
- Bar chart showing claims by insurance type.
- Regional claims analysis.
- Claim amount analysis by insurance type.
- Processing time analysis by claim status.
- Interactive filters for region, claim status and insurance type.

### Dashboard Screenshot

Add your Power BI dashboard screenshot here after completing the final formatting.

Example:

`![Insurance Claims Dashboard](screenshots/insurance_claims_dashboard.png)`

## Business Insights and Recommendations

The analysis is designed to help identify:

- Claim categories with higher claim volumes.
- Regions with larger pending claim volumes.
- Differences in claim amounts across insurance categories.
- Operational patterns in claim processing time.
- Data-quality issues that may affect reporting accuracy.

**Potential business recommendations:**

1. Monitor pending claims to identify operational bottlenecks.
2. Improve data-entry validation to reduce incorrect records.
3. Review regional claim patterns to support resource planning.
4. Monitor claim processing times to improve operational efficiency.
5. Maintain regular data-quality checks and reconciliation procedures.

Recommendations should be evaluated against actual business requirements before implementation.

## Project Structure

```text
Insurance_Claims_Analytics/
│
├── Insurance_Claims_Analysis.ipynb
│
├── clean_insurance_claims.csv
│
├── data_quality_issues.csv
│
├── claim_type_summary.csv
│
├── region_summary.csv
│
├── insurance_claims.db
│
├── Insurance_Claims_Analytics.pbix
│
├── screenshots/
│   └── insurance_claims_dashboard.png
│
└── README.md
```

## Learning Outcomes

Through this project, I developed practical experience in:

- Data cleaning and preprocessing.
- Data validation and quality assurance.
- Exploratory data analysis.
- SQL querying and aggregation.
- Business reporting and KPI development.
- Power BI dashboard creation.
- Identifying operational trends and discrepancies.
- Translating analytical results into business recommendations.

## Conclusion

This project demonstrates an end-to-end data analytics workflow, from generating and validating raw data to analysing business metrics and presenting findings through an interactive dashboard.

It helped strengthen my foundational skills in Python, SQL, data quality management, reporting and business intelligence.

---

**Author:** Nagaraj Asundi

**Project Domain:** Insurance Analytics | Data Analysis | Business Reporting

**Tools:** Python | SQL | Power BI | Excel
