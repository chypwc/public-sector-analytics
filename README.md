# Public Sector Analytics and Decision-Support Portfolio

This repository is the entry point for a portfolio of analytics, reporting, data engineering, and decision-support projects. It is not a duplicate implementation repository. Its purpose is to show what the portfolio demonstrates as a coherent body of work, then direct readers to the individual project repositories for code, data models, SQL, dashboards, reports, and documentation.

The central theme is practical analytics for public-sector and operational decision-making: controlled data pipelines, validated reporting layers, stakeholder-ready outputs, and evidence that can support planning, monitoring, governance, and service improvement.

## Overview

The portfolio brings together projects across education, public health, government revenue compliance, workplace health and safety assurance, workers compensation, hospital costing, labour-market analysis, and cloud data engineering. Across these projects, the work demonstrates the ability to:

- design reporting-ready data models from operational or administrative source data;
- build SQL validation, reconciliation, audit, and data-quality controls;
- create Power BI, Excel, and written reporting outputs for non-technical stakeholders;
- connect cloud data engineering patterns to analytics and decision-support use cases;
- document assumptions, limitations, caveats, and handover notes clearly;
- use synthetic or public data responsibly while preserving realistic public-sector reporting patterns.

## Core Capabilities

| Capability | Evidence across the portfolio |
| --- | --- |
| Public-sector reporting | Education monthly reporting, health surveillance dashboards, government revenue compliance reporting, WHS assurance dashboards, workers compensation financial/performance packs, ACT employment analysis |
| Decision support | Patient costing and ABF comparison, workforce planning insights, WHS follow-up and compliance monitoring, claims triage evidence, monthly education briefs |
| SQL analytics engineering | Star schemas, curated views, reporting marts, validation queries, reconciliation outputs, stored procedures |
| Data quality and governance | Failed-record handling, issue logs, source-to-reporting checks, reconciliation outputs, exception reporting, privacy-aware extracts, audit layers |
| Power BI and Excel reporting | Dashboards, semantic models, slicers, PivotTables, dashboard test notes, report screenshots |
| Cloud data platforms | Azure Data Factory, ADLS Gen2, Synapse serverless SQL, Databricks, Azure SQL, AWS DMS, EMR, Glue, S3, MWAA |
| Infrastructure and automation | Terraform, CloudFormation, GitHub Actions, event-driven pipelines, generated Airflow DAGs |
| Communication | Executive briefings, management summaries, analysis reports, user guides, runbooks, data dictionaries |

## Public-Sector Reporting and Decision-Support Case Studies

| Project | Domain | Tools | Main Outputs | Link |
| --- | --- | --- | --- | --- |
| Education Azure Lakehouse Analytics | Education reporting and monthly insights | Azure Data Factory, ADLS Gen2, Synapse serverless SQL, Databricks, Delta Lake, Azure SQL, Power BI, SQL, Python | ADF/Synapse ingestion baseline, Databricks QA lakehouse, Azure SQL monthly reporting mart, Power BI dashboard, briefs, analysis report | [education_data_lakehouse](https://github.com/chypwc/education_data_lakehouse) |
| Public Health Surveillance Lakehouse | Public health surveillance and operational triage | ADLS Gen2, Azure Data Factory, Synapse serverless SQL, Power BI, SQL, Python | REDCap-style case and lab workflow, validation outputs, curated Parquet reporting layer, Power BI surveillance dashboard | [health-surveillance-lakehouse](https://github.com/chypwc/health-surveillance-lakehouse) |
| Revenue Compliance Reporting | Public-sector taxation, government revenue compliance, tax debt, and operational reporting | SQL Server, SSIS, SSRS, SSMS, Excel, CSV, T-SQL | Monthly taxation and revenue feed ingestion, validated staging tables, star-schema warehouse, data-quality and reconciliation controls, SSRS reports, letter templates, management KPIs | [revenue-compliance-reporting](https://github.com/chypwc/revenue-compliance-reporting) |
| Patient-Level Costing and ABF Decision Support | Hospital costing and service-line analysis | SQL Server, T-SQL, Excel, Power Query, Power Pivot, Python | Patient-level costing model, GL reconciliation, ABF-style comparison, management workbook, costing methodology, runbook | [patient-costing-abf](https://github.com/chypwc/patient-costing-abf) |
| Workers Compensation Reporting | Claims, finance, governance, FOI-style reporting | SQL Server, Power BI, Excel, Python, Dataflow Gen1, on-premises gateway | Curated reporting views, Excel financial/performance pack, Power BI dashboard, FOI-style extract, executive briefing, ML appendix | [workers-comp-reporting](https://github.com/chypwc/workers-comp-reporting) |
| WHS Reporting and Assurance Dashboard | Workplace health and safety reporting, compliance monitoring, and assurance | Power BI, Power Query, Excel | Repeatable reporting model from messy operational extracts, validation and reconciliation logic, exception reporting, leadership dashboard views, source-traceability documentation | [whs-reporting-powerbi](https://github.com/chypwc/whs-reporting-powerbi) |
| ACT Employment Analysis | Labour-market analysis and workforce policy | SQL Server, Power BI, DAX, ABS Labour Force data | Star schema over 500,000+ records, employment dashboard, gender equity and economic resilience policy analysis | [act_employment](https://github.com/chypwc/act_employment) |

## AWS and Cloud Data Engineering Projects

| Project | Focus | Tools | Main Outputs | Link |
| --- | --- | --- | --- | --- |
| InsightFlow | Commercial analytics and business decision support | AWS Lambda, AWS Glue, S3, Step Functions, SageMaker, Athena, Streamlit, FastAPI, Terraform | Customer transaction analytics over 3M+ records, automated SQL/AWS data pipelines, product and customer behaviour reporting, self-service analytics tools | [insightflow](https://github.com/InsightFlow8/insightflow) |
| AWS Spark and SQL Lakehouse | Batch ingestion, lakehouse transformation, orchestration | AWS DMS, PostgreSQL, S3, Glue Catalog, EMR Spark, Apache Iceberg, MWAA, Terraform, GitHub Actions | Secure PostgreSQL-to-S3-to-Iceberg pipeline, generated Airflow DAG, Terraform modules, automated deployment workflow | [aws-dms-emr-terraform](https://github.com/chypwc/aws-dms-emr-terraform) |
| Real-Time Inference | Serverless streaming and machine-learning inference | API Gateway, Lambda, SageMaker XGBoost, DynamoDB, Kinesis, Firehose, S3, Step Functions, CloudFront, Terraform | Real-time recommendation API, streaming analytics path, automated ML training/deployment pipeline, web app | [kinesis-webui](https://github.com/chypwc/kinesis-webui) |
| dbt-Glue ETL | Serverless data lake transformation | AWS Glue, dbt-glue, S3, Glue Crawler, Glue Data Catalog, CloudFormation, GitHub Actions, Snowflake | Snowflake-to-S3 ingestion, Glue cataloging, dbt transformations, feature-engineering models, CI/CD workflows | [aws-resources-exercises](https://github.com/chypwc/aws-resources-exercises) |

## Case Study Summaries

### Education Azure Lakehouse Analytics

This project demonstrates a three-pipeline Azure education analytics portfolio using synthetic school, student, attendance, assessment, and school event data. The pipelines show the same education reporting problem at increasing levels of maturity:

- Pipeline A builds an ADF and Synapse serverless SQL baseline for landing, querying, and shaping school operational data into reporting-ready views.
- Pipeline B extends the workflow into a Databricks QA lakehouse with Bronze, Silver, QA, and Gold layers, including failed-record handling, quality checks, and dashboard validation evidence.
- Pipeline C adds a monthly education insights workflow using Azure SQL Database, merge/upsert processing, a Power BI semantic model, dashboard pages, analysis reports, stakeholder briefs, and caveats for recurring management reporting.

The project is strong evidence for education analytics, data quality, reporting-layer design, and the ability to turn monthly operational data into clear insights and caveats.

### Public Health Surveillance Lakehouse

This project simulates a REDCap-style public health surveillance workflow for respiratory illness case monitoring. It lands daily case and lab exports in ADLS Gen2, moves data through ADF, queries and validates it in Synapse serverless SQL, creates curated reporting outputs, and presents operational surveillance views in Power BI.

The project is strong evidence for health data reporting, SQL validation, issue triage, dashboard ownership notes, and handover-ready public health analytics documentation.

### Revenue Compliance Reporting

This project demonstrates an end-to-end SQL Server public-sector taxation and government revenue compliance reporting workflow using synthetic operational data covering property rates, land tax, duties, and payroll tax. It integrates monthly Excel and CSV feeds through SSIS into validated staging tables and a star-schema warehouse, with SQL controls for file completeness, rejected records, audit outcomes, and reconciliation across liabilities, charge lines, payments, allocations, and debt balances.

The final outputs include SSRS operational reports, letter templates, exception monitoring, account-history investigation views, overdue-account prioritisation, and management KPIs covering assessed government revenue, collections, debt movement, arrears trends, revenue-type exposure, and account-level compliance risk.

The project is strong evidence for public-sector taxation reporting, revenue-office-style compliance analytics, ETL support, SQL Server data-quality controls, compliance follow-up workflows, and stakeholder-ready management reporting.

### Patient-Level Costing and ABF Decision Support

This project demonstrates a synthetic hospital costing workflow connecting general-ledger expenditure, clinical activity, resource use, and direct cost detail. It validates inputs, assigns and allocates cost to patient encounters, reconciles outputs to the general ledger, and publishes Excel-ready reporting views.

The Excel workbook supports service-line cost analysis, cost-driver review, high-cost encounter review, ABF-style comparison, reconciliation, and data-quality monitoring.

### Workers Compensation Reporting

This project demonstrates an end-to-end workers compensation reporting workflow using synthetic operational, financial, governance, and reporting extracts. It brings raw data under control through SQL Server staging, mapping, integration, reconciliation, curated views, and privacy-aware reporting rules.

The final outputs include an annual-report-style Excel pack, a Power BI report, FOI-style de-identified extract design, governance and reconciliation evidence, an executive briefing, and an optional high-cost claim machine-learning appendix.

### WHS Reporting and Assurance Dashboard

This project demonstrates a Power BI workplace health and safety reporting workflow that converts messy operational extracts from Safety Portal, SafetyCulture, training records, contractor certification registers, and corrective action logs into a repeatable reporting model for leadership and assurance use.

The workflow uses Power Query to clean, validate, reconcile, and document source data before it reaches the dashboard layer. It includes exception-reporting logic and source-traceability notes so recurring WHS outputs can show where safety follow-up is needed, whether compliance obligations are on track, and which data-quality or system-access issues affect reporting reliability.

The project is strong evidence for operational reporting, Power Query transformation, data-quality assurance, compliance monitoring, and stakeholder-ready dashboard documentation.

### ACT Employment Analysis

This project transforms ABS Labour Force data into a SQL Server star schema and Power BI dashboard focused on ACT employment trends. It analyses gender equity, full-time and part-time composition, industry concentration, public-sector dependency, volatility, and economic resilience.

The project is strong evidence for using public datasets to produce policy-oriented analysis, with clear analytical findings and workforce planning implications.

### InsightFlow

InsightFlow is an e-commerce data intelligence platform built around large-scale customer transaction analytics, AWS data pipelines, machine-learning recommendations, and self-service reporting. The project analyses more than 3 million customer order records to identify purchasing patterns, product-level trends, customer behaviour, and opportunities for business decision support.

The platform uses AWS Lambda, Glue, S3, Step Functions, SageMaker, Athena, Terraform, Streamlit, and FastAPI to support repeatable data processing, analytical datasets, customer segmentation, product recommendation workflows, and non-technical exploration of purchasing patterns without ad-hoc data requests.

### AWS Spark and SQL Lakehouse

This project demonstrates an AWS lakehouse pipeline that extracts PostgreSQL data through AWS DMS, lands Parquet data in S3, catalogs it with Glue, transforms it with EMR Spark, and stores analytics-ready outputs in Apache Iceberg format. MWAA orchestrates DMS and EMR work, while Terraform provisions the infrastructure and generates deployment-aware Airflow DAGs.

The project is strong evidence for cloud data engineering, infrastructure-as-code, orchestration, and analytics platform foundations.

### Real-Time Inference

This project demonstrates a serverless real-time recommendation pipeline. A web app sends events through API Gateway and Lambda, SageMaker serves XGBoost recommendations, DynamoDB stores feature data, and Kinesis/Firehose streams events to S3. Step Functions orchestrates the machine-learning pipeline from Glue processing through training and endpoint deployment.

The project is strong evidence for real-time data products, serverless design, machine-learning deployment, and API-backed analytics systems.

### dbt-Glue ETL

This project demonstrates a serverless data lake transformation workflow using Snowflake ingestion into S3, Glue Crawlers and Data Catalog metadata, and dbt-glue transformations on Glue Interactive Sessions. CloudFormation manages infrastructure and GitHub Actions orchestrates deployment, ingestion, catalog refresh, and dbt runs.

The project is strong evidence for SQL-based transformation, feature engineering, data lake automation, and CI/CD for analytics workflows.
